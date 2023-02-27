# Whisper Docker API

## How to run the container?

Open a terminal and navigate to the folder where you created the files.

Run the following command to build the container:

    docker build -t whisper-api .

Run the following command to run the container:

    docker run -p 5000:5000 whisper-api

##  How to request from the API?

You can test the API by sending a POST request to the route http://localhost:5000/whisper with a file in it. Body should be form-data.

### You can use the following curl command to test the API:

    curl -F "file=@/path/to/file" http://localhost:5000/whisper

In result you should get a JSON object with the transcript in it.