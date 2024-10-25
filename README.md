# Tines AI Efficiency Winner
## My six month journey with the Tines SOAR platform.

This past spring, I began my automation journey with the [Tines](https://tines.com) platform.  I have an System Administration background, with no formal training in coding. I work in Security Operations.  Our portfolio includes EDR, DNS Protection, & Threat Intelligence. 

As part of the Tines onboarding, the first automation project we tackled concerned shunning malicious IP addresses on the Cisco Next-Gen Firewall (NGFW) without any involvement from the Network Management team.  In the Firewall Management Center, we used the custom network security intelligence feed as a means to shun IPs at the border.  The NGFW consumes two text files via URLs, one containing the list of IPs to shun, and the other containing the MD5 hash of the IP shun list.  

We decided to host the files on an S3 bucket, since it contains only Indicators of Compromise (IOCs), therefore no PI data. By using AWS, we didn't have to maintain any internal infrastructure.

One of the biggest challenges facing the Security Operations Centre (SOC) is how to lifecycle or sunset IOCs, especially IP addresses since threat actors rapidly cycle through IPs during phishing campaigns.  It is easy to add IOCs to a security platform, but how do we track them and sunset them appropriately automatically.

Our Tines Customer Success Engineer recommeneded using [Tines Resources](https://www.tines.com/docs/resources/)  A Tines Resource allows the storage of information outside of a workflow, that can be consumed downstream in the same series of actions or by other workflows. Via a web form submission page, any IPs, submitted by the IR Team or SecOps, are written to a sunset list, a Tines Resource, along with the submission date.  Then, the workflow creates an IP shun list from the sunset list.  By a Tines AWS HTTP REST API call, the Tines workflow pushes the IP shun list to the S3 bucket.  Then, another action, calculates the MD5 hash of the IP shun file, which gets written to another Tines Resource.  The MD5 hash file is pushed to the S3 bucket.  Both the IP Shun List and MD5 hash files are consumed by the NGFW custom intelligence feed.  

For sunsetting IPs, we had another series of actions which filtered out stale IP addresses.  Then, the next series of actions created an updated IP shun list and MD5 hash files which were posted to the S3 bucket.   In a few weeks, we were able to submit 
