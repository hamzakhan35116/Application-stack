# Application-stack

Welcome to the Application Stack Development Task! This task involves creating a Docker container that integrates Php/Laravel, Node.js, Vue.js, and Python technologies. Additionally, you will configure Nginx to expose applications, set up database containers, create a Docker Compose configuration, and thoroughly document the process.

## Task Overview

This task comprises several steps, each contributing to the creation of a well-rounded development environment. You'll be using Docker to encapsulate the technologies, and Docker Compose to orchestrate the entire setup. By the end of this task, you'll have a functional multi-technology development environment that can be easily shared and replicated.

## Task Steps

### 1. Creating a Docker Container

- Create a Docker container that includes Php/Laravel, Node.js, Vue.js, and Python.
- Set up basic projects to showcase each technology, such as welcome pages.

### 2. Exposing Applications Through Nginx

- Configure the Docker container to expose all applications through an Nginx web server on port 100 (internet port).

### 3. Setting Up Database Containers

- Create separate database containers using standard images for Postgres, MongoDB, and Redis.
- Ensure each container exposes an external port for connectivity.

### 4. Docker Compose Configuration

- Package all components into a single Docker Compose file.
- Define a new Docker network within the Docker Compose configuration.

### 1. Node
		```WORKDIR /app
		```COPY package*.json ./
		```RUN npm install
### 2. Python
	```# Copy Flask application
	```COPY app.py /app/app.py
	```COPY templates /app/templates
	```# Install Python dependencies
	```RUN pip install flask
### 3. Vue.js
		npm install -g vue-cli
		vue init webpack my-vue-project
		cd vue-project
		npm install
		npm run dev
### 4. Laravel
	```# Configure PHP-FPM
	```RUN sed -i 's/;clear_env = no/clear_env = no/' /etc/php/7.4/fpm/pool.d/www.conf
	```# Create Laravel project directory
	```RUN composer create-project --prefer-dist laravel/laravel /var/www/laravel


### 5. See the localhost

- To see your Laravel app, open web browser(firefox) and go to http://172.18.0.5:100/php.

- For your Vue.js app, go to http://172.18.0.5:100/vue.

- For your node.js app, go to http://172.18.0.5:100/node.

- For your python.py app, go to http://172.18.0.5:100/python.

### 6. Creating a New Git Repository

- Create a new Git repository to host your code and Docker configuration.

### 7. Comprehensive Documentation

- Create a detailed README file within the repository.
- Document each step of the process with clear headings, paragraphs, and explanations.
- Include code snippets, configurations, and explanations for clarity.

## Getting Started

Follow these steps to complete the task:

1. Clone this repository to your local machine:

2. Complete each step as outlined in the task description.

3. Document your progress in the README.md file within the repository.
