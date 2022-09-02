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
states of versioning:
- Default versioning not enabled
- Versioning