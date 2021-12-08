---
title: Assignment 1
subtitle: Computer performance, reliability, and scalability calculation
author: Arindam Samanta
---

## 1.2 

#### a. Data Sizes
```
- 1 Character = 1Byte Ref -> https://www.unitconverters.net/data-storage/character-to-byte.htm
- Compressed PNG losless 24bit/pixel (Ref -> https://toolstud.io/photo/filesize.php?imagewidth=1024&imageheight=768)
- Uncompressed 16bit monochrome (RAW) (Ref -> https://toolstud.io/photo/filesize.php?imagewidth=1024&imageheight=768)
- https://www.digitalrebellion.com/webapps/videocalc (Uncompressed 8-bit)
- (https://medium.com/precision-medicine/how-big-is-the-human-genome-e90caa3409b0)
- Considering a 3B letters human genome length with avg coverage of 30X will have 90B letters roughly occupying 90GB of disk space. Mapping 1 character to 1 Byte.So it would be  typically 180GB as a FASTQ file format. It could roughly be 200GBs to be precise
```

| Data Item                                  | Size per Item | 
|--------------------------------------------|--------------:|
| 128 character message.                     | 128 Bytes     |
| 1024x768 PNG image                         | 457.04KB      |
| 1024x768 RAW image                         | 1.57 MB       |
| HD (1080p) HEVC Video (15 minutes)         | ? MB          |
| HD (1080p) Uncompressed Video (15 minutes) | 156.43 GB     |
| 4K UHD HEVC Video (15 minutes)             | ? MB          |
| 4k UHD Uncompressed Video (15 minutes)     | ? MB          |
| Human Genome (Uncompressed)                | 200GB         | 
#### b. Scaling
```
- Refer back to data sizes for the daily Instagram photos
	- 1 1024x768 PNG image is roughly 457.04 KB
	- If roughly 100 million videos and photos are uploaded every day, and 75% are PNG photos, that means 75M are photos.
	- 75,000,000 x 457.04 KB = 34,278,000,000 KB ~ 34,278,000 MB  to store daily insta photos
	- 34,278,000 MB X 3 (To account for HDFS) = 102,834,000 MB
	- 102,834,000 MB = 98.0701 TB
	- You would need about 10 10TB HD to store this data
- Daily Twitter Tweets (Uncompressed)
	-size of One tweet of 128 characters(on avg) is 128 Bytes
	-500,000,000 * 128 B=	
- Yearly 
```

|                                           | Size     | # HD |
|-------------------------------------------|---------:|-----:|
| Daily Twitter Tweets (Uncompressed)       | 62 GB    |      | # 500 million * 128 B ~ 62GB
| Daily Twitter Tweets (Snappy Compressed)  | ??       |      |
| Daily Instagram Photos                    | 34 TB    |10    | # assuming 75M(75*457KB) photos and 25M() videos
| Daily YouTube Videos                      | 4300 TB  |430   |
| Yearly Twitter Tweets (Uncompressed)      | 23 TB    |3     | 365 * 62
| Yearly Twitter Tweets (Snappy Compressed) | ??       |      |
| Yearly Instagram Photos                   | ??       |      |
| Yearly YouTube Videos                     | ??       |      |

#### c. Reliability
```
Using the yearly estimates from the previous part, estimate the number of hard drive failures per year using data from Backblaze’s hard drive statistics.
```
|                                    | # HD | # Failures |
|------------------------------------|-----:|-----------:|
| Twitter Tweets (Uncompressed)      | ??   |            |
| Twitter Tweets (Snappy Compressed) | ??   |            |
| Instagram Photos                   | ??   |            |
| YouTube Videos                     | ??   |            |

#### d. Latency

|                           | One Way Latency      |
|---------------------------|---------------------:|
| Los Angeles to Amsterdam  | 141.521 ms           |Ref -> https://wondernetwork.com/pings/Los%20Angeles/Amsterdam
| Low Earth Orbit Satellite | ? ms                 |
| Geostationary Satellite   | ? ms                 |
| Earth to the Moon         | ? ms                 |
| Earth to Mars             | ? minutes            | 
