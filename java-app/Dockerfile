# Get a base image with JDK installed
FROM openjdk:11

# Create a working directory to compile, run java apps
WORKDIR /app

# Copy code from local machine to docker container
COPY hello.java .

# Compile the code
RUN javac hello.java

# Run the java app
CMD ["java","hello"]
