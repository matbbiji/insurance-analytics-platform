An end-to-end Lakehouse platform that automates the car insurance claim process, cutting approval times from days to sub-second decisions.  

## The Problem:
Traditional claim processing relies on manual, human visual inspection to verify damage severity and policy limits—creating massive operational bottlenecks.  

## The Solution:
A full-stack architecture that unifies streaming enterprise data, machine learning, and an interactive web portal to automatically approve or flag claims the second they are submitted.  

### Architecture:
Synchronized 32,000+ Records: Engineered a streaming Medallion ETL pipeline using Databricks Lakeflow Connect to capture CDC updates from an AWS RDS SQL Server.  

Joined real-time AWS Kinesis vehicle telemetry with unstructured S3 crash images using Autoloader and PySpark.  



### AI / ML:
Fine-tuned a ResNet computer vision model to instantly classify vehicle damage severity.  

Tracked training experiments, logged parameters, and versioned the final model using MLflow.  

Real-Time AI Inference: Deployed the model via Mosaic AI Serving to generate sub-second predictive damage scores via API.  


### Full-Stack development:
Interactive Next.js Portal: Built a fast, responsive claims submission frontend for users and an administrative dashboard for edge-case review.  

Routed payloads to the Mosaic AI endpoint, ensuring lightweight network requests without bloating the app with external libraries
Synced Gold-tier analytics directly into a Lakebase PostgreSQL database to serve operational data to the frontend instantly.
