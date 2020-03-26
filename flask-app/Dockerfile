# escape=`
FROM alpine:3.5
#specifies base image as alpine 3.5 
#also makes the escape character the backtick instead of the backslash

RUN apk add --update py2-pip
#Run on the host image
#apk = tool used to upgrade/install or delete
#add = add new pages
#updates the py2-pip package 

COPY requirements.txt /usr/src/app/
#copying the requirements into the dockerfile from current directory


RUN pip install --no-cache-dir -r /usr/src/app/requirements.txt

#RUN is typically used for installing packages
#CMD specifies what command to run within the container, this can be modified

#for reference ENV will se the same value for each variable 

COPY app.py /usr/src/app/
COPY templates/index.html /usr/src/app/templates/

#tell what port number the container should expose
EXPOSE 5000

#run the application
CMD ["python","/usr/src/app/app.py"]
