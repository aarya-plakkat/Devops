# Setting base image
FROM ubuntu:latest

#Information about maintainer, version and date
LABEL maintainer = aarya
LABEL version = 1.0
LABEL date=29/10/25

#Setting work directory
WORKDIR /app

#Copying sample.txt
COPY sample.txt ./

#Setting up container environment
ENV ENVIRONMENT=developer

#Updating and installing curl
# RUN apk update && apk add --no-cache curl
RUN apt update && apt install -y curl

#Exposing port
EXPOSE 3000

#Command
CMD ["echo","Container built"]
