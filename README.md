# jenkins
Jenkins 설치 및 구성 가이드


## Install Guide


- Docker 실행
```bash
docker run --name jenkins -p 8080:8080 -p 50000:50000 -d -v /var/run/docker.sock:/var/run/docker.sock -v jenkins_home:/var/jenkins_home -u root -e JAVA_OPTS='-Duser.timezone=Asia/Seoul -Dfile.encoding=UTF-8 -Dsun.jnu.encoding=UTF-8' jenkins/jenkins:lts
```

```bash
docker exec -it jenkins bash
curl https://get.docker.com/ > dockerinstall && chmod 777 dockerinstall && ./dockerinstall
```

```bash
sudo chmod 666 /var/run/docker.sock

docker exec -it <container id> bash
cat var/jenkins_home/secrets/initialAdminPassword
```