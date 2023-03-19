FROM python:3.9

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Set work directory
WORKDIR /home/ubuntu/blog-app
# Install dependencies
COPY requirements.txt /home/ubuntu/blog-app
RUN pip install --no-cache-dir -r requirements.txt

# Copy project
COPY . /home/ubuntu/blog-app