# Containerize an application with Docker

Containerizing an application with Docker is a great way to package your software along with its dependencies, making it easy to deploy and run consistently across different environments.

## OVERVIEW

This application was developed to provide detailed local forecasts and weather forecasts for the entire world, as well as the current temperatures in Celsius as well as sunrise and sunset times based on the time zone of the city.

## FEATURES

In the Zeus app, you will find the following features;

- Getting and displaying the users' nickname
- Updates the UI to reflect if the weather condition is sunny or it's about to rain.
- Displays the users' current location.
- Display the users'current time.
- Display the users' current day of the week.
- Displays users' current location temperature in celcius.
- Displays the users wind and sunrise details
- Allow user to query for another location
- Display weather details of any location queried by the user(wind, sunrise and temperature)

## HOW TO SETUP

Here's a step-by-step tutorial to help you containerize this application:

### Step 1: Install Docker

If you haven't already, install Docker on your system. You can find installation instructions for various platforms on the Docker website: [Install Docker](https://docs.docker.com/get-docker/)

### Step 2: Dockerfile

Create a `Dockerfile` in the root directory of the application. The `Dockerfile` contains instructions for building your Docker image.

```Dockerfile
# Base image
FROM httpd:2.4-alpine

# Copy the application files into the container
COPY . /usr/local/apache2/htdocs/

# Expose port 80
EXPOSE 80
```

### Step 3: Build the Docker Image

Open a terminal, navigate to the directory containing your `Dockerfile`, and run the following command to build your Docker image:

```bash
docker build -t zeus .
```

### Step 4: Run the Docker Container

Once the image is built, you can run a container based on that image using the following command:

```bash
docker run -d -p 80:80 zeus:latest
```

### Step 5: Access Your Application

Once the container is running, you should be able to access your application through a web browser or any other client using the URL `http://localhost`.

### Step 6: Manage Your Docker Container

You can manage your Docker container using various Docker commands such as `docker stop`, `docker start`, `docker restart`, etc. For example, to stop the container, you can run:

```bash
docker stop zeus
```

## SCREENSHOTS

![login](https://user-images.githubusercontent.com/63567230/183277770-f8998557-dfcb-48c9-a43c-9e6e4a24c8c9.JPG)
![weather App](https://user-images.githubusercontent.com/63567230/183277775-ef71ae62-6489-4041-8c1b-aef0c87b1cf1.JPG)

## Links: `https://zeusweather.netlify.app/`

## REPORT A VULUNERABILITY

To report a vulnerability please send an email with the details to `onyeanunaprince@gmail.com`. This will help me to access the risk and start necessary steps.

Thanks for helping 😊

## Author

- Twitter - [@OnyeanunaE](https://twitter.com/OnyeanunaE)
- Linkedin - [Onyeanuna](https://www.linkedin.com/in/prince-onyeanuna-607352246/)
