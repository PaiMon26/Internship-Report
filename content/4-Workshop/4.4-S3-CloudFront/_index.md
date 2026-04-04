---
title: "S3 and CloudFront"
date: 2026-04-04
weight: 4
chapter: false
pre: " <b> 4.4. </b> "
---

#### Overview

This section presents the configuration steps for **S3**, **Origin Access Control**, and **CloudFront** for the static frontend.

#### Implementation steps

1. Open **Amazon S3** and start creating a new bucket for the LunchSync frontend.

![S3 step 1](s3.1.jpg)

2. Set the bucket prefix to `lunchsync-project`, choose region `ap-southeast-1`, let S3 generate the full bucket name, and keep the bucket private.

![S3 step 2](s3.2.jpg)

3. Keep `ACLs disabled`, enable **Block all public access**, and continue with a private bucket.

![S3 step 3](s3.3.jpg)

4. Keep the default `SSE-S3` encryption, create the bucket, and upload the frontend content into folders such as `frontend/` and `media/`.

![S3 step 4](s3.4.jpg)

5. After the bucket is attached to CloudFront, review the **bucket policy** to make sure only `cloudfront.amazonaws.com` for this distribution can read objects.

![S3 step 5](s3.5.jpg)

6. Move to **CloudFront > Origin access** and start creating a new **Origin Access Control** for the S3 bucket.

![OAC step 1](oac.1.jpg)

7. Name it `lunchsync-oac`, describe it clearly for the LunchSync bucket, and keep **Sign requests** enabled.

![OAC step 2](oac.2.jpg)

8. Review the OAC list to confirm `lunchsync-oac` is ready before building the distribution.

![OAC step 3](oac.3.jpg)

9. Open **CloudFront > Distributions** and start creating a new distribution.

![CloudFront step 1](cf.1.jpg)

10. Choose a plan and continue through the distribution wizard.

![CloudFront step 2](cf.2.jpg)

11. Name the distribution `S3-Frontend`, use **Single website or app**, and skip attaching the Route 53 domain during the initial wizard.

![CloudFront step 3](cf.3.jpg)

12. In **Specify origin**, choose **Amazon S3** as the origin type.

![CloudFront step 4](cf.4.jpg)

13. Select the project S3 bucket as the origin, set **Origin path** to `/frontend`, and allow CloudFront to access the private bucket.

![CloudFront step 5](cf.5.jpg)

14. Keep the AWS-recommended origin and cache settings for static content from S3.

![CloudFront step 6](cf.6.jpg)

15. In **Enable security**, keep the default CloudFront/WAF protections included by the wizard.

![CloudFront step 7](cf.7.jpg)

16. Review the wizard summary, confirm the S3 origin and `Origin path = /frontend`, then create the distribution.

![CloudFront step 8](cf.8.jpg)

17. After the distribution is created, open **Origins** and confirm that the first S3 origin was created with the expected origin path and OAC.

![CloudFront step 9](cf.9.jpg)

18. If needed, use **Edit origin** to reattach `lunchsync-oac` and copy the generated policy into the S3 bucket policy.

![CloudFront step 10](cf.10.jpg)

19. Open **Behaviors** and start adjusting the default behavior for the frontend.

![CloudFront step 11](cf.11.jpg)

20. For the default behavior, set **Viewer protocol policy = Redirect HTTP to HTTPS**.

![CloudFront step 12](cf.12.jpg)

21. Keep an S3-friendly cache policy such as `CachingOptimized` together with an origin request policy like `CORS-S3Origin`.

![CloudFront step 13](cf.13.jpg)

22. Open **Error pages** and start adding a custom error response for the SPA.

![CloudFront step 14](cf.14.jpg)

23. Create a rule so when the origin returns `403`, CloudFront responds with `/index.html` and HTTP `200` for frontend routes.

![CloudFront step 15](cf.15.jpg)

24. Review the error page list to confirm that the SPA fallback rule was saved.

![CloudFront step 16](cf.16.jpg)

25. Return to **Origins** and create a second origin for the backend **ALB**.

![CloudFront step 17](cf.17.jpg)

26. For the ALB origin, enter the ALB DNS name and use **HTTPS only** so CloudFront talks to the backend securely.

![CloudFront step 18](cf.18.jpg)

27. Create a third S3 origin for the media folder, reuse the same bucket, set **Origin path = /media**, and attach `lunchsync-oac`.

![CloudFront step 19](cf.19.jpg)

28. Review **Origins** again and confirm the distribution now has 3 origins: `frontend`, `ALB backend`, and `media`.

![CloudFront step 20](cf.20.jpg)

29. Create a new behavior for `media/*`, route it to the media S3 origin, and continue redirecting viewers to HTTPS.

![CloudFront step 21](cf.21.jpg)

30. For `media/*`, keep a static-content cache policy and avoid attaching extra functions.

![CloudFront step 22](cf.22.jpg)

31. Create the **CloudFront Function** `api-for-alb` to normalize request URIs before forwarding to the backend.

![CloudFront step 23](cf.23.jpg)

32. Create or edit a dynamic behavior such as `sessions/*` so it routes to the ALB origin, uses HTTPS only, and forwards the full viewer request.

![CloudFront step 24](cf.24.jpg)

33. For dynamic ALB behaviors, use `CachingDisabled`, `AllViewer`, and attach `api-for-alb` on the **Viewer request** event.

![CloudFront step 25](cf.25.jpg)

34. Review the full behavior list and confirm paths such as `/sessions/*`, `/auth/*`, `/restaurants/*`, `/collections/*`, and `/dishes/*` go to the ALB, while `Default` and `media/*` stay on S3.

![CloudFront step 26](cf.26.jpg)

35. Switch to **Route 53**, open the `lunchsync.space` hosted zone, and prepare to add the CloudFront alias record.

![CloudFront step 27](cf.27.jpg)

36. Create an alias record at the root domain `lunchsync.space` that points to the CloudFront distribution.

![CloudFront step 28](cf.28.jpg)

37. Review the hosted zone again and confirm the alias record to CloudFront is present.

![CloudFront step 29](cf.29.jpg)

38. Go back to **CloudFront > Edit settings**, add the **Alternate domain name (CNAME)** `lunchsync.space`, and select the ACM certificate from `us-east-1`.

![CloudFront step 30](cf.30.jpg)

39. In the same settings page, set **Default root object = index.html** and enable the supported HTTP versions such as `HTTP/2` and `HTTP/3`.

![CloudFront step 31](cf.31.jpg)

40. Save the settings and confirm on the distribution overview page that the alias, certificate, and `index.html` default root object are applied.

![CloudFront step 32](cf.32.jpg)

41. Open `https://lunchsync.space` and confirm that the frontend is served through CloudFront with the custom domain.

![CloudFront step 33](cf.33.jpg)

42. Test an additional asset such as `https://lunchsync.space/media/lunchsync.png` to confirm that the `media/*` behavior is also working correctly.

![CloudFront step 34](cf.34.jpg)
