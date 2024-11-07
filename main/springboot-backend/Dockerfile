# Use OpenJDK 17 as the base image
FROM openjdk:17 
LABEL "Project"="Java Application"

# Set the working directory
WORKDIR /app

# Copy the WAR file from the target directory
COPY target/HostBuddy-RESTapi-CRUD-0.0.1-SNAPSHOT.war .

# Expose the application port
EXPOSE 8085

# Command to run the application
CMD ["java", "-jar", "HostBuddy-RESTapi-CRUD-0.0.1-SNAPSHOT.war"]
