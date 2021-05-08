# Wyyder 

[![Twitter](https://img.shields.io/badge/twitter-@wyyder-green.svg)](https://twitter.com/wyyder)
<a href="https://www.youtube.com/channel/UCklWKcVOeAAV1SC1eQwnLNQ?sub_confirmation=1">
      <img alt="youtube subscribers" title="Please Subscribe..." src="https://freshidea.com/jonah/youtube-api/subscribers-badge.php?label=Subscribers&style=for-the-badge&color=red&labelColor=ce4630"/></a> 

## Question / Upwork Job
[Question](https://raw.githubusercontent.com/wyyder/upwork/master/dockerize-jenkins-with-deps/job_details.png)

## Youtube 
[Watch POC](https://www.youtube.com/watch?v=P7PAyegw8Ss)

## Jenkins Docker with below dependencies

```bash
curl
python3
php7
eyeD3 #(python)
atomicparsley
ffmpeg
ImageMagick
```

## Steps to Run jenkins container with customised dependencies

### clone this repository 
```bash
git clone https://github.com/wyyder/upwork.git
```
### Build image in local machine
```bash
docker build -t wyyder/jenkins-customised .
```

### Start jenkins using docker compose yml
```bash
docker-compose up -d
```

# Get the initial admin password
```bash
docker exec wyyder-jenkins cat /var/jenkins_home/secrets/initialAdminPassword
```

# Confirm the wyyder-jenkins container is running
```bash
docker container ls
```
# Check version
```bash
curl --version
python3 --version 
php --version
pip3 list | grep eyed3
AtomicParsley --version
ffmpeg -version
magick -version
```