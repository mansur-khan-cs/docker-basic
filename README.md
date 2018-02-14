
### Topics :
	1. What is Docker
	2. Virtual Machines vs. Docker
	3. Introduction to Dockerfiles, images and containers
	4. The Docker Hub
	5. Writing a Dockerfile
	6. Building an image
	7. Running a container
	8. Mounting volumes
	9. One process per container

### build/run flow :
	- docker file ----build---->> docker image(like class) -----run---->> container(likeobject/instance)

### Dockerfile:
	- FROM keyword to specify the "base image"
	- FOR keyword to copy the source code into the image
	- "/var/www/html/" is location where apache looks for it's own file system 
	- '.' means current folder
	- EXPOSE keyword to expose port 80(localhost). container will listen at port 80

### build docker file:
	- docker build -t hello-world .
### run docker image :
	- docker run -p 80:80  hello-world
	- docker run -p 80:80 -v /Users/maksud/Desktop/:/var/www/html/ hello-world