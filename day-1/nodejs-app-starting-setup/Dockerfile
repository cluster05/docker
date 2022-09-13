# image buidling 

# pull the node image
FROM node

WORKDIR /app

# source . same folder
# destination . path inside of image | image container contain own file system
#   don't use main root folder 
#   /app > create app folder (if not exists)

# it is create the copy of file into the images it self
COPY . /app

# by default docker run all command on root directory 
# use WORKDIR /app the copy with relative path ./
#                            or absolute path  /app
RUN npm install

# docker application isolated in it's env
# so we have to expose the port to outside word
EXPOSE 80

# RUN command run when image is created
# CMD command run when container is started based on images
CMD ["node","server.js"]

# docker build [path] to build the image specify on dockerfile

# docker run [containerId] [container_name]
#   external port:internal port
#   -p 3000:3000 

# docker stop [containerId] [container_name]

# ---------------------------------------------------------------------

# images are layer based (use cached memery)    
#  when one layer changed all the sub-suquence layer all buid newly

# COPY package.json /app // optimized
# RUN npm install
# COPY . /app