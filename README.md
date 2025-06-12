# 📊 Big Data Cluster Performance Analysis with Apache Spark on Google Cloud

This project explores the performance of parallel image preprocessing workloads on Google Cloud Dataproc using Apache Spark. The experiments focus on evaluating and optimizing cluster configurations, partition strategies, and file formats (JPEG vs. TFRecord) to analyze throughput, scalability, and efficiency.

## 🚀 Project Goals

- Analyze the impact of different **cluster topologies** (e.g., 8x1, 4x2, 1x8) on processing time and resource utilization
- Evaluate the effect of **Spark partitioning** strategies on job performance
- Compare **JPEG and TFRecord** image formats in terms of throughput and latency
- Use **regression analysis** to understand the effect of batch size and dataset size on performance
- Simulate CherryPick-like behavior by building lightweight models for predicting optimal configurations

## ⚙️ Technologies Used

- **Apache Spark (PySpark)** for distributed processing
- **Google Cloud Platform (Dataproc, GCS)** for scalable compute and storage
- **Google Colab** for interactive development
- **Python (NumPy, Pandas, Matplotlib, Scikit-learn)** for data analysis and regression
- **TFRecord & JPEG** file formats for image preprocessing tasks

## 📈 Key Tasks

- Set up Dataproc clusters with various CPU configurations (e.g., 8x1, 4x2, 1x8)
- Parallelized image processing workloads using `sc.parallelize` with custom partition counts
- Cached expensive RDD operations for performance gains
- Performed regression to quantify the effect of `batch_size × dataset_size` on throughput
- Interpreted performance metrics including CPU usage, disk I/O, and network bandwidth
- Related findings to **CherryPick**, an ML-based cloud configuration optimizer

## 📊 Highlights

- TFRecord format yielded **significantly higher throughput** than JPEG (~265 vs ~10 images/sec)
- Larger batch sizes and more partitions generally improved performance
- Caching reduced processing time by ~1.1x
- 8x1 cluster delivered the highest I/O throughput and parallelism

## 📎 Resources
- 📄 Report Summary: see [`Big Data Report.pdf`](https://github.com/zeynepdagci/Big-Data/blob/main/Big%20Data%20Report.pdf)

---

**Disclaimer**: This project is shared for educational and demonstration purposes only. Please do not submit this work for academic credit.
