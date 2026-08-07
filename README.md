# Kafka Docker Compose 🐳

![Kafka](https://img.shields.io/badge/Kafka-Streaming-orange?style=flat-square) ![Docker](https://img.shields.io/badge/Docker-Container-blue?style=flat-square) ![ExpressJS](https://img.shields.io/badge/ExpressJS-Web%20Framework-green?style=flat-square)

Welcome to the **Kafka Docker Compose** repository! This project provides a simple way to set up Apache Kafka using Docker and Docker Compose. It also includes a test application built with Express.js to demonstrate how to interact with Kafka. 

## Table of Contents

- [Introduction](#introduction)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Testing with Express.js](#testing-with-expressjs)
- [Contributing](#contributing)
- [License](#license)
- [Links](#links)

## Introduction

Apache Kafka is a powerful message broker designed for high-throughput and low-latency data streaming. It allows you to build real-time data pipelines and streaming applications. With Docker Compose, you can easily manage and deploy Kafka and its dependencies.

This repository aims to simplify the setup process. It provides a Docker Compose file that defines all necessary services, making it easy to get started with Kafka.

## Getting Started

To use this project, follow these steps:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/poyraztuzcu/kafka-docker-compose.git
   cd kafka-docker-compose
   ```

2. **Download and execute the Docker Compose file:**

   You can find the latest release [here](https://github.com/poyraztuzcu/kafka-docker-compose/releases). Download the relevant files and execute them.

3. **Start the services:**

   Run the following command to start Kafka and its dependencies:

   ```bash
   docker-compose up
   ```

   This command will set up the entire environment, including Zookeeper, Kafka, and any other necessary services.

## Project Structure

Here’s a brief overview of the project structure:

```
kafka-docker-compose/
│
├── docker-compose.yml      # Main Docker Compose file
├── express-app/            # Directory for the Express.js application
│   ├── app.js              # Main application file
│   ├── package.json        # Node.js dependencies
│   └── ...                 # Other application files
└── README.md               # Project documentation
```

- **docker-compose.yml:** This file defines the services, networks, and volumes for the Docker containers.
- **express-app/:** This directory contains the Express.js application, which will be used to interact with Kafka.

## Usage

After starting the services, you can access Kafka and Zookeeper through their respective ports. By default:

- Zookeeper runs on `localhost:2181`
- Kafka runs on `localhost:9092`

You can configure these ports in the `docker-compose.yml` file if needed.

To interact with Kafka, you can use various tools, such as:

- Kafka CLI tools
- Kafka clients in different programming languages
- The Express.js application provided in this repository

## Testing with Express.js

The Express.js application in this repository allows you to test Kafka by sending and receiving messages. Here’s how to set it up:

1. **Navigate to the Express app directory:**

   ```bash
   cd express-app
   ```

2. **Install dependencies:**

   Run the following command to install the necessary Node.js packages:

   ```bash
   npm install
   ```

3. **Start the Express server:**

   Run the application with:

   ```bash
   node app.js
   ```

   The server will start, and you can access it at `http://localhost:3000`.

4. **Send a test message:**

   You can use a tool like Postman or curl to send a POST request to the Express app:

   ```bash
   curl -X POST http://localhost:3000/send -d '{"message": "Hello, Kafka!"}'
   ```

   This will send a message to Kafka, and you should see a response confirming the message was sent.

## Contributing

Contributions are welcome! If you have suggestions or improvements, feel free to create a pull request. Please follow these guidelines:

1. Fork the repository.
2. Create a new branch for your feature or fix.
3. Make your changes.
4. Commit your changes with clear messages.
5. Push to your branch.
6. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Links

For the latest releases, please visit [this link](https://github.com/poyraztuzcu/kafka-docker-compose/releases). Download the necessary files and execute them to set up your environment.

If you have any questions or need assistance, check the "Releases" section for updates and documentation.

---

This repository aims to make working with Kafka simpler and more accessible. Whether you're building a new application or just exploring Kafka's capabilities, this setup will help you get started quickly. Enjoy coding!