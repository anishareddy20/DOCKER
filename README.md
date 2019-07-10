# DOCKER
CONTAINERIZING PYTHON FLASK APPLICATION INTO DOCKER:

In this we are containerizing Restful web service and UI of this web service using docker. Docker is a light weight application to host web application. Here we need to pull the docker image containing the web service and run using the docker name and image name. The docker image pushed into cloud is pulled using command docker pull bommaraa/ccproject

After the image is downloaded we have run image using command docker run -d -p 8081:80 bommaraa/ccproject

The application is then hosted localhost:8081 on web browser After hosting we can see both the web application of HW3 and Restful web service of HW2.

GET: http://localhost:8081/historical/ - Retrieves the list of all the dates in JSON array GET DATE: http://localhost:8081/historical/dateYYYYMMDD - Retrieves the DATE, TMAX,TMIN of date passed FORECAST: http://localhost:8081/forecast/20140912 - Retrieves the TMax and TMin temperature for next & days from given date POST: http://localhost:8081/historical/ - To add weather information for a particular day

DELETE: http://localhost:8081/historical/ - Delete method to delete the temperature information for a particular day

Here we have four required files main.py which contains our python file of flask application, requirements.txt which contains all requirements to run flask application in docker and uwsgi file, a Dockerfile.

To run web application in docker we need to have an account in hub.docker.com To save image of docker:docker save | gzip > containername.tgz

References to install docker and push image into docker: https://medium.com/@cjus/installing-docker-ce-on-an-aws-ec2-instance-running-ubuntu-16-04-f42fe7e80869?fbclid=IwAR0LTCVhyXiDLpF7gsNtoB1yU99a2U52XP78LpxPwWFAbyoNYY-ZW3gwpnk https://docs.docker.com/v17.12/docker-cloud/builds/push-images/?fbclid=IwAR0-lPKNRh3nDFaGKQLXSlxJuDDFkX5twzc0QoNXw6sX_sSVuLoQsZfw6bo https://docker.github.io/engine/getstarted/
