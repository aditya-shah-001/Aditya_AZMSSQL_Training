# Use an official Python runtime as a parent image
FROM python:3.9

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV NAME World
ENV PYTHONUNBUFFERED 1
ENV DJANGO_SETTINGS_MODULE=HelloWorldProject.settings

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy the current directory contents into the container at /code
COPY requirements.txt /usr/src/app/

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy project
COPY . /usr/src/app/

# Make port 8000 available to the world outside this container
EXPOSE 8000

# Run app.py when the container launches
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
