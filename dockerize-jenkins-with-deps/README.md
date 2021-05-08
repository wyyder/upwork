# Dockerize Jenkins with dependencies

<a href="https://twitter.com/wyyder">
      <img alt="Twitter - Follow..." title="Please Follow..." 
src="https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white"/>
</a>
<a href="https://www.youtube.com/channel/UCklWKcVOeAAV1SC1eQwnLNQ?sub_confirmation=1">
      <img alt="Youtube - Please Subscribe..." title="Please Subscribe..." src="https://img.shields.io/badge/-Subscribe-red?style=for-the-badge&logo=youtube&logoColor=white"/>
</a>
<a href="https://www.youtube.com/watch?v=P7PAyegw8Ss">
      <img alt="Youtube - Please Subscribe..." title="Please Subscribe..." src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white"/>
</a>

## Question / Upwork Job

![Question](https://raw.githubusercontent.com/wyyder/upwork/master/dockerize-jenkins-with-deps/job_details.png?raw=true)

## Docker file & Docker compose yml

[Docker File](./Dockerfile)

[Docker Compose yml](./docker-compose.yml)

```bash
# clone repository
git clone https://github.com/wyyder/upwork.git
cd upwork/dockerize-jenkins-with-deps

# Build image in local
docker build -t wyyder/jenkins-customised .

# Verify image 
docker images

# Start jenkins using docker compose yml
docker-compose up -d

# Confirm the wyyder-jenkins container is running
docker container ls

# Get the initial admin password
docker exec wyyder-jenkins cat /var/jenkins_home/secrets/initialAdminPassword

# Launch jenkins in browser http:localhost:8080 & verify

# Stop container 
docker container stop wyyder-jenkins

# Remove container 
docker container rm wyyder-jenkin

# Remove image 
docker image rm wyyder/jenkins-customised

# In Jenkins job use to verify the version of dependencies
curl --version
python3 --version 
php --version
pip3 list | grep eyed3
AtomicParsley --version
ffmpeg -version
magick -version
```