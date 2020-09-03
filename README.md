# Flask Passport Text Extraction API

A Python Flask based API that can take in non text based documents such as a PDF of a scanned doc and a passport correctly extract the text from those images.
A Angular application to interact with said API for UI based tools such as the upload feature and visualize back results.
A Flask API for performing initial basic NLP on the processed text such as structure analysis or classification of document types.

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


6. In Postman, run a post command on http://localhost:5000/passport
Go to body set imagefile as the key - set the body to choose file OR:


`curl -F "imagefile=@<filepath>" http://localhost:5000/passport`


The response should convert text in a passport image to JSON format.




