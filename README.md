# Django-Docker-EC2

# Django Docker EC2 Example

This repository contains a basic Django project that is Dockerized and can be deployed on an AWS EC2 instance.

## Getting Started

Follow these steps to get the project up and running on your local machine:

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/django-docker-ec2.git
   cd django-docker-ec2
   ```
2. Build the Docker image:
   ```bash
   docker build -t django-docker-app .
   ```
3. Run the Docker container:
   ```bash
   docker run -d -p 8000:8000 django-docker-app
   ```

4. Access the Django app:
Open your web browser and navigate to http://localhost:8000

## Deploying the Django App on AWS EC2

Follow these steps to deploy the Django app on an AWS EC2 instance:

1. **Launch an EC2 Instance:**

   - Choose an instance type (e.g., t2.micro).
   - Configure security groups to allow incoming traffic on port 80.
   - Download the key pair for SSH access.

2. **SSH into the EC2 Instance:**

   ```bash
   ssh -i /path/to/your/key.pem ec2-user@your-instance-ip
   ```
3. Access the Django app:
Open your web browser and navigate to http://localhost:8000

## Deployment on AWS EC2

To deploy the Django app on an AWS EC2 instance, follow these steps:

1. **Launch an EC2 instance:**

    - Choose an instance type (e.g., t2.micro).
    - Configure security groups to allow incoming traffic on port 80.
    - Download the key pair for SSH access.

2. **SSH into the EC2 instance:**

    ```bash
    ssh -i /path/to/your/key.pem ec2-user@your-instance-ip
    ```

3. **Pull the Docker image:**

    ```bash
    docker pull your-docker-image
    ```

4. **Run the Docker container:**

    ```bash
    docker run -d -p 80:8000 your-docker-image
    ```

5. **Configure Nginx:**

    - Install Nginx and set up a reverse proxy to forward requests to the Docker container.

6. **Access the deployed app:**

    Open your web browser and navigate to your EC2 instance's IP address.
