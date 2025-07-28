# No-rate-limit
 Bug Report: Missing Rate Limiting on Newsletter Endpoint
Subject: Bug Report: Missing Rate Limiting on Newsletter Endpoint
Dear Security team,
I hope this message finds you well. I’m writing to report a potential issue concerning the newsletter endpoint in your application.
While testing, I observed that the /newsletter endpoint does not appear to enforce any rate limiting. This could potentially allow automated or excessive requests, leading to system strain or misuse. According to the Common Weakness Enumeration (CWE), this falls under CWE-770: Allocation of Resources Without Limits or Throttling, which outlines the risk of failing to control resource usage in networked applications.
Steps to reproduce
Visit the urlhttps://snyk.io/and scroll down .
You'll see a option to subscribe the newsletter and the input a email and click get notified .
Capture the request of subscription in burpsuite and send it to intruder.
Generate 50 null payloads and start the attack .
We can see that 50 requests for subscription has went to the server and its accepted by the sever witn 200 OK status code.
After we turn off the proxy and back to the page we can the subscription process is completed.


Details:
- Endpoint: /newsletter
- Issue: No rate limiting or throttling detected
- Risk Level: Potential for abuse via automation or denial-of-service
- Suggested Fix: Implement rate limiting (e.g. token bucket, leaky bucket, or fixed window strategies) and monitor request patterns
Please let me know if you need any further information or replication steps. I appreciate your attention to this matter and your continued commitment to application security.
Warm regards,
Vedant tanaji vhatkar
vedantvhatkar5@gamil.com
video poc:https://drive.google.com/file/d/1bGC2hFwhablne9OlbY3_flq1pBDOkDxD/view?usp=drive_link
