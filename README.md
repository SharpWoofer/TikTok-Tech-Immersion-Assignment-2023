![image](https://github.com/SharpWoofer/TikTok-Tech-Immersion-Assignment-2023/assets/127273523/7668d883-03dc-4cd3-b097-17704da9dd4a)

![Tests](https://github.com/TikTokTechImmersion/assignment_demo_2023/actions/workflows/test.yml/badge.svg)

# Instant Messaging System (Backend)

This is a backend implementation of an Instant Messaging (IM) system, developed as part of the [TikTok Tech Immersion Server (Backend) Assignment](https://bytedance.sg.feishu.cn/docx/P9kQdDkh5oqG37xVm5slN1Mrgle). The purpose of this project is to provide core message features for an IM system, without including the front-end and account/authentication components.

## Features

- Two Services: The system consists of an HTTP server and an RPC server to handle different aspects of the IM functionality.
- APIs: Specific APIs have been implemented using Golang to enable communication and message handling.
- Data Storage: The system securely stores message data, allowing receivers to access it at any time. [Redis](https://hub.docker.com/r/bitnami/redis/) has been used for efficient data management.
- Message Delivery: Messages are delivered to the intended recipients in a timely and consistent manner through a pull-based approach. This means that receivers can fetch messages as needed without the need for real-time push notifications.
- Performance and Scalability: The system has been designed to handle a large number of users and messages, supporting over 20 concurrent connections during testing.

## Usage

1. Make sure docker is up and running, and the selected ports are not currently in use to avoid conflict.
2. Start the HTTP server and RPC server by running the [Docker Compose file](docker-compose.yml).
3. Interact with the system by using the provided APIs for sending and receiving messages.
4. Explore the data storage mechanism to access and manage stored messages.

Please refer to the [HTTP API](https://github.com/TikTokTechImmersion/assignment_demo_2023/blob/main/idl_http.proto) for more information on send and pull requests.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to use, modify, and distribute it as per the terms of the license.

## Acknowledgements

I would like to express my gratitude to the TikTok Tech Immersion team for the opportunity to work on this project.
