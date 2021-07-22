# 389ds

1. Docker pull

sudo docker pull fabric8/389ds:latest
  

2. Docker Run 
 sudo docker run -d --name my-389ds -e "DIRSRV_ADMIN_USERNAME=admin,DIRSRV_ADMIN_PASSWORD=12345, DIRSRV_MANAGER_PASSWORD=12345,DIRSRV_SUFFIX=dc=example,dc=com" -p 0.0.0.0:389:389 fabric8/389ds:latest


3. git clone this repo code and copy into container
  dcoker cp dsuser.ldif containerid:/tmp/
  
5. Create user password 
6. slappasswd -h {SSHA} -s user@123
{SSHA}GGcZ8O1vCFWnRE3QsyquKVcll+JKbVqi

6. Add into user schema
7. userPassword: {SSHA}GGcZ8O1vCFWnRE3QsyquKVcll+JKbVqi

Ldapadd the schema into docker image.


ldapadd -f user.ldif -D "cn=directory manager" -w admin@123
ldapadd -f schema.ldif -D "cn=directory manager" -w admin@123


