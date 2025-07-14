VisionPipe is a cloud-native image classification service designed to handle high-throughput inference with auto-scaling capabilities. Built with Flask and AWS, it supports real-time image uploads and classification using a pre-trained deep learning model.

🚀 Features
 - Auto-scaling infrastructure using AWS EC2, S3, and CloudWatch
 - Asynchronous request handling with AWS SQS
 - Real-time image upload and classification via REST API
 - Processes 500+ images/sec with <1s latency at scale
 - Easily deployable using Docker

🛠️ Tech Stack
- Backend: Python, Flask
- Cloud: AWS EC2, S3, SQS, CloudWatch
- Containerization: Docker
- Model: Pre-trained CNN (e.g., ResNet50)

📦 Setup Instructions
# Clone the repo
- git clone https://github.com/yourusername/visionpipe.git
- cd visionpipe

# Build Docker image
- docker build -t visionpipe .

# Run the app
- docker run -p 5000:5000 visionpipe

# API Usage
- POST /predict
- Form-data: file: <your_image.jpg>
- Response: { "prediction": "cat", "confidence": 0.92 }

# Performance
- Cold start: ~800ms
- Scales up to 15 instances under load
- Tested with 1000 concurrent image requests
