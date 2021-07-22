# 389ds

1. Docker pull

sudo docker pull fabric8/389ds:latest
  

3. Docker Run 
 sudo docker run -d --name my-389ds -e "DIRSRV_ADMIN_USERNAME=admin,DIRSRV_ADMIN_PASSWORD=12345, DIRSRV_MANAGER_PASSWORD=12345,DIRSRV_SUFFIX=dc=example,dc=com" -p 0.0.0.0:389:389 fabric8/389ds:latest
