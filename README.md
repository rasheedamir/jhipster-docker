Step 1 - Build docker image: 

`sudo docker build -t jhipster_img .`

Step 2 - Create a docker container: 

e.g.

`sudo docker run --name jhipster -d -v /home/rasheed/Projects/jhipster/ams:/home/jhipster -p 8080:8080 -p 9000:9000 -p 35729:35729 -p 4022:22 -t jhipster_img`

NOTE: please change the path to project in your directory structure! i.e. `/home/rasheed/Projects/jhipster/ams`

Step 3 - Get into docker container: 

`ssh -p 4022 jhipster@localhost`
pwd: `jhipster`

Step 4 - Build the app

this will ignore the tests and build a package:
`gradle build -x test`

this will run the app:
`gradle run -x test`