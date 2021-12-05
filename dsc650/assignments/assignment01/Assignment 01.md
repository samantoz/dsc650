---
title: Assignment 1
subtitle: Computer performance, reliability, and scalability calculation
author: Arindam Samanta
---

## 1.2 

#### a. Data Sizes
| Data Item                                  | Size per Item | 
|--------------------------------------------|--------------:|
| 128 character message.                     | 128 Bytes     | (Ref -> https://www.unitconverters.net/data-storage/character-to-byte.htm)
| 1024x768 PNG image                         | 457.04KB      | Compressed PNG losless 24bit/pixel (Ref -> https://toolstud.io/photo/filesize.php?imagewidth=1024&imageheight=768)
| 1024x768 RAW image                         | 1.57 MB       | Uncompressed 16bit monochrome (RAW) (Ref -> https://toolstud.io/photo/filesize.php?imagewidth=1024&imageheight=768)
| HD (1080p) HEVC Video (15 minutes)         | ? MB          |
| HD (1080p) Uncompressed Video (15 minutes) | 156.43 GB     |https://www.digitalrebellion.com/webapps/videocalc (Uncompressed 8-bit)
| 4K UHD HEVC Video (15 minutes)             | ? MB          |
| 4k UHD Uncompressed Video (15 minutes)     | ? MB          |
| Human Genome (Uncompressed)                | ? GB          |

#### b. Scaling

|                                           | Size     | # HD | 
|-------------------------------------------|---------:|-----:|
| Daily Twitter Tweets (Uncompressed)       | 62 GB    |      | # 500 million * 128 B ~ 62GB
| Daily Twitter Tweets (Snappy Compressed)  | ??       |      |
| Daily Instagram Photos                    | ??       |      | # 
| Daily YouTube Videos                      | ??       |      |
| Yearly Twitter Tweets (Uncompressed)      | 22,630 GB|      | 365 * 62
| Yearly Twitter Tweets (Snappy Compressed) | ??       |      |
| Yearly Instagram Photos                   | ??       |      |
| Yearly YouTube Videos                     | ??       |      |

#### c. Reliability
|                                    | # HD | # Failures |
|------------------------------------|-----:|-----------:|
| Twitter Tweets (Uncompressed)      | ??   |            |
| Twitter Tweets (Snappy Compressed) | ??   |            |
| Instagram Photos                   | ??   |            |
| YouTube Videos                     | ??   |            |

#### d. Latency

|                           | One Way Latency      |
|---------------------------|---------------------:|
| Los Angeles to Amsterdam  | 141.521 ms                 |Ref -> https://wondernetwork.com/pings/Los%20Angeles/Amsterdam
| Low Earth Orbit Satellite | ? ms                 |
| Geostationary Satellite   | ? ms                 |
| Earth to the Moon         | ? ms                 |
| Earth to Mars             | ? minutes            | 
