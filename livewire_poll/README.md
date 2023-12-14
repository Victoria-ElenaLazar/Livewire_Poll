# Livewire Poll Application

This is a simple poll application built with Laravel and Livewire, allowing users to create polls, add options, and vote. The application is designed to run in a Docker environment for easy setup.

## Table of Contents
- [Features](#features)
- [Requirements](#requirements)
- [Getting Started](#getting-started)
    - [Docker Setup](#docker-setup)
    - [Configuration](#configuration)
    - [Running the Application](#running-the-application)
- [Usage](#usage)
- [Security Practices](#security-practices)

## Features

- Create polls with customizable options.
- Vote on poll options.

## Requirements

- [Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/)
- PHP 8.0 and above

## Getting Started

### Docker Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/Victoria-ElenaLazar/Livewire_Poll/tree/main
2. Navigate to the project directory:
   ```bash
   cd livewire_poll
3. Copy ".env.example" file, rename it to ".env" and configure the database and other settings you might need.

### Configuration

1. Install dependencies:

   ```bash
   composer install

2. Generate application key:
   ```bash
   php artisan key:generate

### Running the application

1. Start Docker containers:
   ```bash
   docker-compose up -d

2. Run the migration:
   ```bash
   php artisan migrate
3. Start the server:
   ```bash
   php artisan serve

## Usage

**Creating a Poll**

Navigate to the home page.

Fill the title

Click on the "Add option" button.

Click "Create poll."

**Voting**

View a poll with options.

Click on the "Vote" button next to the desired option.

## Security Practices

**Validation**

All input data is validated to ensure it meets the required criteria. Poll titles and options texts are sanitized and validated to prevent malicious input.

**User-Friendly Errors**

User-friendly error messages are provided in case of validation failures or any other errors. This ensures that users receive clear feedback on what went wrong during interactions with the application.
