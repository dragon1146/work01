# this line of code will get the latest images of "ubuntu" from docker hub
# to be used as the base image for the creation of the app image
FROM ubuntu:18.04

# the line of code will run the command 
RUN apt update && \
    apt install python3 -y && \
    apt install python3-pip -y && \
    adduser adhoc-user

# this line of code will config the working dir of the container to be "/app/scr/"
WORKDIR /app/src/

# this line of code will copy the contents of the PWD to the dir in the container
# called "/app/scr" which is the container's working dir
COPY ./src/requirements.txt /app/src/

COPY ./src/server.py /app/src/

# this line of code will install all the python modules listed in the file 
# "requirements.txt"
RUN pip3 --no-cache-dir install -r requirements.txt

# this line of code will expose port "8000" on the container
EXPOSE 8000

# this line of code will cause the container to enter into the python interpreter
# by executing the command "python3"

# this line of code also allows the container to run after it is created because it
# will have the "python3" program running in the background

# this line of code also makes the app on the container executable once the container
# is launch

# this line of code will run the container with the user adhoc-user
USER adhoc-user

# this line of code with start the container with the python3 interpreter
ENTRYPOINT ["python3"]

# this line of code will run the command "server.py" while the container is in the 
# python interpreter

# this line of code is also an argument to the "ENTRYPOINT" command
CMD ["server.py",  "debug=True", "port=8000", "host='0.0.0.0'"]
