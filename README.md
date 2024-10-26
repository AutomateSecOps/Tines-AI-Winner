# Tines AI Efficiency Winner
## My six month journey with the Tines SOAR platform.

This past spring, I began my automation journey with the [Tines](https://tines.com) platform.  I have an System Administration background, with no formal training in coding. I work in Security Operations.  Our portfolio includes EDR, DNS Protection, & Threat Intelligence. Recently, our team adopted Tines as our automation platform.

Prior to adopting Tines, the process of shunning IPs on the border firewall, was a time-consuming manual process which involved multiple teams along with our incident ticketing system.  With the Tines Customer Success Team, we created a [Tines Story](https://www.tines.com/docs/stories/), aka worfklow, where a security analyst can submit malicious IP addresses in a webform.  In less than a minute, the Tines story logged the IP addresses for sunsetting purposes, created the IP shun list and MD5 hash files, and posted these files to an AWS S3 bucket, so the border firewall can consume the IP shun list as a URL feed.

Wow! I was amazed.

This month long process of co-building the IP shun workflow, with the Tines Customer Success Team, made me realize the power of automation. 

I learned a lot from our Tines Success Engineer, which enabled me to start my learning in earnst.  During the onboarding process, I used the [Tines University](https://www.tines.com/university/) as a training resource.  After graduating from Tines Uni, I started the [Tines Core & Advanced certification](https://www.tines.com/get-certified/).

The certification courses and training provided a solid foundation of knowledge and comfort with the Tines platform. This past June, I started automating some internal SecOps reporting we did in regards to our Endpoint, Detection, & Response (EDR) platforms. The CrowdStrike Falcon sensor goes into Reduced Functionality Mode (RFM), usually because the operating system or kernel version is too old or too new for the sensor to support in kernel mode.

Every week, SecOps would log into the Falcon console, and filter the host management console for endpoints in RFM for the last week.  We would generate the report and download it.  This report provided data on what kernel update is causing the Falcon s
