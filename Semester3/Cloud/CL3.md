# AWS Storage Layer

S3 bisa hosting website

Setiap objek 

mendukung versioning

Durability
- 11 9s SLA (99.999999999%)
- Ensure no lost

Availability
- You can access your data when needed
- S3 standard storage class is designed for four 9s (99.99%)

Scalability
- Virtually unlimited capacity
- One file limited to 5TB.


apa?

URL based: `https://<bucket-name>.s3.amazonaws.com/video.mp4`. Kemudian S3 dapat mendukung caching.

Stored in beckets and objects are private and protected by default until you set it to public.

When sharing
- manage and control the data access.
- Follow the principle of least privileges.

Controlling access to Amazon S3
- 
apa?


Encryption in S3
- Using secret key
	- Only users who have the secret key can decode the data
	- Optionally, you can use Amazon KMS (Key Management Services)
apa?


Support static site including HTML files, images, videos and client side scripts. Opsi paling murah di AWS untuk hosting website. 

S3 supports versioning
enables easy retrieval of deleted objects or rollback to previous versions.
states of versioning:
- Default versioning not enabled
- Versioning-enabled
- Versioning-suspended (old version still available)

Layanan S3 handled by global AWS. So if you define a bucket, it must be globally unique. 

Support CORS (Cross-Origin Resource Sharing) in the configuration for Machine-to-Machine communication using web.

For analytics
QuickSight (PowerBI nya AWS) dan Athena


Amazon S3 Tiering
- S3 Standard: Frequently Accessed Data
- S3 Standard IA (infrequently Access) : Long-lived, infrequently accessed data
- S3 One Zone IA : Long-lived infrequently accessed, non-critical data (data only resided in only one AZ (Availability Zone))
- S3 Glacier (Archiving rarely accessed data) - 
	- Glacier deep archive: data backup only accessed once or twice or years -> waiting 12 hours to access.
- S3 Outpost
Intelligence Tiering -> look for how frequently data is accessed, AWS can automatically assign the suitable tier for certain data. It can be configured by admin related to file type, frequency of access, etc.

Lifecycle policy -> apa?

Pricing. Apa?

Multipart upload, apa?

Transfer acceleration, apa? -> ke cloudfront dulu





In the end of the day it is the matter of investment.

## Research Later
Elastic bean-stalk
amazon workdocs (SAAS)
amazon drive
Region Table