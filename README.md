<img width="280" height="399" alt="docker_webapp_evidence" src="https://github.com/user-attachments/assets/1f8a7e2a-69c8-43e4-b877-c2a2acfd1137" />

# Hotel Booking

A multithreaded Spring web application for checking hotel room availability and making reservations. This is coursework for Advanced Java course, built by extending a starter application provided by the course.

## My Work

The starter app was provided by the course. I extended it with:

- **Multithreaded language translation:** Added French Translation
- **Time-zone message:** Added Different Zone Options
- **Currency exchange:**
- **Containerization:** a Docker image of the full application
- **Booking:** Added the ability to Book Available Rooms.

## Tech Stack

- Java, Spring [Spring Boot]
- Docker

## Concurrency

[TODO]

## Running with Docker

```bash
docker build -t hotel-booking .
docker run -p 8080:8080 hotel-booking
```

Then open http://localhost:8080.


## Cloud Deployment Plan (AWS)

> This describes how I would deploy the application. I have not deployed it to AWS.

1. **Create an ECR repository** to store the Docker image.
2. **Build and tag the image** locally, with `latest` or a version tag.
3. **Push the image to ECR** after authenticating with the AWS CLI.
4. **Run it on ECS:** create a task definition (image, CPU, memory), then launch a service or standalone task that pulls the image from ECR.
5. **Expose it:** put a load balancer in front of the service to spread traffic and improve availability, then map a public DNS name to it.
