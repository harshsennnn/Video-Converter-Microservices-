# Video-Converter-(Python Microservices) Devops Project
#### This project implements a microservices-based architecture for converting video files into audio (MP3) format. It leverages modern DevOps practices with containerized services, message queues, and distributed data storage for efficient processing. The solution is designed to handle video uploads, convert them asynchronously to audio, and enable users to download the converted files.

## Key Features
<b>User Authentication: </b>
/login endpoint handles user authentication and generates JWT tokens for secure communication.
User data is stored in PostgreSQL.

<b>Video Upload:</b> /upload endpoint allows users to upload video files.
Uploaded videos are temporarily stored as binary data and sent to a RabbitMQ video queue for processing.

<b>Audio Conversion:</b> A dedicated converter service retrieves video files from the video queue, processes them, and stores the resulting MP3 data.
Processed MP3 files are stored in MongoDB for retrieval.

<b>File Download:</b> /download endpoint allows users to fetch converted audio files from MongoDB for playback or download.

<b>Notifications:</b> Notifications (e.g., completion of audio conversion) are sent to users via email or push notifications, providing real-time updates.

## Tech Stack
<b>Backend Framework:</b> RESTful APIs developed with [language/framework choice, e.g., Node.js, Flask, or Spring Boot].

<b>Database:</b> PostgreSQL (user data), MongoDB (MP3 file storage).

<b>Message Queue:</b> RabbitMQ for asynchronous video and MP3 processing.

<b>Notifications:</b> Email or push notifications for updates.

<b>Authentication:</b> JWT for secure user sessions.

<b>Containerization:</b> Docker for deploying all microservices as independent containers.
