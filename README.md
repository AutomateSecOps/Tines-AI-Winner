# Tines AI Efficiency Winner
## My six month journey with the Tines SOAR platform.

This past spring, I began my automation journey with the [Tines](https://tines.com) platform.  I have an System Administration background, with no formal training in coding. I work in Security Operations.  Our portfolio includes EDR, DNS Protection, & Threat Intelligence. Recently, our team adopted Tines as our automation platform.

Prior to adopting Tines, the process of shunning IPs on the border firewall, was a time-consuming manual process which involved multiple teams along with our incident ticketing system.  With the Tines Customer Success Team, we created a [Tines Story](https://www.tines.com/docs/stories/), aka worfklow, where a security analyst can submit malicious IP addresses in a webform.  In less than a minute, the Tines story logged the IP addresses for sunsetting purposes, created an IP shun list and MD5 hash files, and posted these files to an AWS S3 bucket so the border firewall can consume the IP shun list as a URL feed.

Wow! I was amazed.

This month long process of co-building the IP shun workflow, with the Tines Customer Success Team, made me realize the power of automation. I learned a lot from our Tines Success Engineer.  During the onboarding process, I used the [Tines University](https://www.tines.com/university/) as a training resource.  After that, I started the Tines intro certification.
