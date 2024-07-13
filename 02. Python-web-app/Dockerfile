FROM ubuntu

# Set the working directory
WORKDIR /app

# Copy the requirements file and application code
COPY requirements.txt /app
COPY devops /app/devops

# Install Python and pip
RUN apt-get update && \
    apt-get install -y python3 python3-venv python3-pip && \
    python3 -m venv /app/venv && \
    /app/venv/bin/pip install --upgrade pip && \
    /app/venv/bin/pip install -r requirements.txt

# Activate the virtual environment and set the entrypoint and default command
ENTRYPOINT ["/app/venv/bin/python"]
CMD ["devops/manage.py", "runserver", "0.0.0.0:8000"]
