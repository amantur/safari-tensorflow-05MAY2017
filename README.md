#THIS REPOSITORY IS ARCHIVED

# safari-tensorflow-05MAY2017

Dockerfile file for Tensorflow Course (15 May 2017)

Use this Dockerfile to build a container with course material and required libraries installed. 

Following are the steps to build and use the container.

1. Clone this repo
2. CD into the cloned folder
3. Run `docker build -t <your tag> .`
4. Once successfully built you can run container with this command:

   `docker run -p 127.0.0.1:88:8888 -d --name tensorflow <your tag>`

We now need the security/login key from **jupyter notebook** to start using it. To get the key run this command:

 `docker logs tensorflow`
 
This will print the log output from machine like:

    [C 01:57:48.215 Tensorflow]
    Copy/paste this URL into your browser when you connect for the first time,
    to login with a token: http://localhost:8888/?token=2bc2971f5327aa018bf591621e5b97cd98b741ce2c6b5743
   
Now navigate to http://127.0.0.1:88 You will be asked for the token. Copy the string after *token=* from the log output above and paste into the textbox, click on the <kbd>Login</kbd> button and you are good to go.

_**Note:-**_ If you do not specify a tag (_&lt;your tag&gt;_) in **step 3**, you will need to note/copy the id of the image created and pass it in place of the tag later.

##Alternate

If you don't want to build the image, you can pull the one I pushed to the docker hub. Use this command to get image from the hub:

`docker pull amantur/safari-tensorflow-15may2017:v1`

Once image is downloaded you can follow the directions above from step 4 onwards.
