
FROM: ubuntu:latest

#Setting up working directory
WORKDIR /app

#Copy the files from host file system to image file system
COPY ./app

#Installing necessary packages
RUN apt=get update && apt-get install python3 python3-pip

#Environment name
ENV NAME world

#Default Entrypoint (can be overriden by docker run --entrypoint commandtorun ) 
CMD ["python3", "app.py"]