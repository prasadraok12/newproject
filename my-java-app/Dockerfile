# Use a Maven image with OpenJDK
FROM maven:3.8.1-openjdk-17-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the pom.xml and source code to the container
COPY pom.xml .
COPY src/ ./src/

# Install dependencies and compile the code, run tests
RUN mvn clean install

# Run JUnit tests
CMD ["mvn", "test"]
