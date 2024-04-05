# MERN Forum App

This is a simple forum app built using the MERN (MongoDB, Express.js, React.js, Node.js) stack.

## Table of Contents

- [Introduction](#introduction)
- [Schema](#schema)
- [Models](#models)
- [Routes](#routes)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The MERN Forum App allows users to start discussions, ask questions, and engage with other users on various topics.

## Schema

### Topic
- **title**: String
- **description**: String
- **createdAt**: Date
- **updatedAt**: Date

### Discussion
- **topicId**: ObjectId (ref: Topic)
- **userId**: ObjectId (ref: User)
- **content**: String
- **type**: Enum (opinion, interpretation, debate)
- **createdAt**: Date
- **updatedAt**: Date

### User
- **username**: String
- **email**: String
- **password**: String (hashed)
- **createdAt**: Date
- **updatedAt**: Date

## Models

### Topic
- **createTopic(title, description)**: Create a new topic.
- **getTopics()**: Retrieve all topics.
- **getTopicById(id)**: Retrieve a topic by ID.
- **updateTopic(id, data)**: Update a topic.
- **deleteTopic(id)**: Delete a topic.

### Discussion
- **createDiscussion(topicId, userId, content, type)**: Create a new discussion under a topic.
- **getDiscussionsByTopic(topicId)**: Retrieve discussions under a topic.
- **getDiscussionById(id)**: Retrieve a discussion by ID.
- **updateDiscussion(id, data)**: Update a discussion.
- **deleteDiscussion(id)**: Delete a discussion.

### User
- **register(username, email, password)**: Register a new user.
- **login(email, password)**: Log in an existing user.
- **getUserById(id)**: Retrieve a user by ID.
- **updateUser(id, data)**: Update user information.
- **deleteUser(id)**: Delete a user.

## Routes

### Topic Routes

- **GET /topics**: Retrieve all topics.
- **GET /topics/:id**: Retrieve a topic by ID.
- **POST /topics**: Create a new topic.
- **PUT /topics/:id**: Update a topic.
- **DELETE /topics/:id**: Delete a topic.

### Discussion Routes

- **GET /discussions/:topicId**: Retrieve discussions under a topic.
- **GET /discussions/:id**: Retrieve a discussion by ID.
- **POST /discussions**: Create a new discussion under a topic.
- **PUT /discussions/:id**: Update a discussion.
- **DELETE /discussions/:id**: Delete a discussion.

### User Routes

- **POST /register**: Register a new user.
- **POST /login**: Log in an existing user.
- **GET /users/:id**: Retrieve a user by ID.
- **PUT /users/:id**: Update user information.
- **DELETE /users/:id**: Delete a user.

## Installation

To run the MERN Forum App locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone <repository-url>

