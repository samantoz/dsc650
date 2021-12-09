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
| HD (1080p) HEVC Video (15 minutes)         | 2949          |
| HD (1080p) Uncompressed Video (15 minutes) | 209.95 GB     |
| 4K UHD HEVC Video (15 minutes)             | 6750 MB       |
| 4k UHD Uncompressed Video (15 minutes)     | 680 GB        |
| Human Genome (Uncompressed)                | 200GB         | 
#### b. Scaling
```
- Snappy compression site (1.5x) https://www.infoq.com/news/2011/04/Snappy/
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
| Daily Twitter Tweets (Uncompressed)       | 178.81 GB|1     | # 500 million * 128 B ~ 62GB
| Daily Twitter Tweets (Snappy Compressed)  | 119.21   |      |
| Daily Instagram Photos                    | 98 TB    |10    | # assuming 75M(75*457KB) photos and 25M() videos
| Daily YouTube Videos                      | 28 PB    |2500  |
| Yearly Twitter Tweets (Uncompressed)      | 65 TB    |7     | 365 * 178.81
| Yearly Twitter Tweets (Snappy Compressed) | 43 TB    |5     |
| Yearly Instagram Photos                   | 36 PB    |3600  |
| Yearly YouTube Videos                     | 9,081,998 PB |1M| -- 1 Million HD

#### c. Reliability
```
Using the yearly estimates from the previous part, estimate the number of hard drive failures per year using data from Backblaze’s hard drive statistics.
I used this site for the reliability score https://www.backblaze.com/blog/hard-drive-reliability-update-september-2014/
Roughly failure was 3% annual failure rate for seagate HDD
```
|                                    | # HD     | # Failures |
|------------------------------------|---------:|-----------:|
| Twitter Tweets (Uncompressed)      | 7        |7*.03=0.21  |
| Twitter Tweets (Snappy Compressed) | 5        |0.15        |
| Instagram Photos                   | 3600     |107.37      |
| YouTube Videos                     | 1,000,000|30,000      |

#### d. Latency
```
1 hop from earth equator to geo stationary satellite is 36K*2=72K kms approx. Latency for radio waves would be 240ms
https://www.satsig.net/latency.htm

```

|                           | One Way Latency      |
|---------------------------|---------------------:|
| Los Angeles to Amsterdam  | 141.521 ms           |Ref -> https://wondernetwork.com/pings/Los%20Angeles/Amsterdam
| Low Earth Orbit Satellite | 10ms                 |
| Geostationary Satellite   | 240 ms               |
| Earth to the Moon         | 2.6s                 |
| Earth to Mars             | 40 minutes           | 
