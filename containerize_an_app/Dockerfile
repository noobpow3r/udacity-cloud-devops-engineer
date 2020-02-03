FROM python:3.8.1-buster

## Complete Step 1:
# Create a Working Directory
WORKDIR /app

## Complete Step 2:
# Copy source code to working directory
COPY . flask_app/web.py /app/

## Complete Step 3:
# Install packages from requirements.txt
# hadolint ignore=DL3013
RUN pip install --upgrade pip &&\
    pip install --trusted-host pypi.python.org -r requirements.txt

## Complete Step 4:
EXPOSE 5000

## Complete Step 5:
# Run app.py at container launch
CMD ["env", "FLASK_APP=web.py", "flask", "run"]
