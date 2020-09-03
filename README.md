# Docker Flask Passport Text Extraction API

A Docker and Python Flask based API that can extract text from passports, and a second endpoint that extracts text generally from images.

## Instructions

1. Clone this repo and cd into the created directory.

2. Run the following 2 commands in terminal: 
```
docker-compose build
docker-compose up
```

3. Use Postman or curl to test the API!  The curl command is:

`curl -F "imagefile=@<filepath>" http://localhost:5000/<route>`

4. In Postman, run a GET command on http://localhost:5000. This will show you it is working.

5. In Postman, run a POST command on http://localhost:5000/image. Go to body set imagefile as the key - set the body to choose file OR:


`curl -F "imagefile=@<filepath>" http://localhost:5000/image`


The response should extract text from the image (it works best on images of documents).


6. In Postman, run a post command on http://localhost:5000/passport. Go to body set imagefile as the key - set the body to choose file OR:


`curl -F "imagefile=@<filepath>" http://localhost:5000/passport`


The response should convert text in a passport image to JSON format.




