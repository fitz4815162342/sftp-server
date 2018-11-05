# sftp-server
SFTP server hosted in docker container

docker run \
    --name sftp-server \
    --restart always \
    -h sftp-server \
    --cap-add=SYS_ADMIN \
    --privileged \
    -v $(pwd)/Share:/home/me/upload \
    -p 2222:22 -d fitz4815162342/sftp-server \
    me:4815162342:1000
