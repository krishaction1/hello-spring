# hello-spring

docker kill `docker ps -q`
docker system prune --all

sudo apt update
sudo apt-get install -y openjdk-17-jdk maven git

git clone https://github.com/Jaibw/hello-spring.git
cd hello-spring/

mvn clean install
docker build --tag hellospring .
docker run -it -p 80:8080 -d hellospring


sudo apt install docker-compose
docker kill `docker ps -q`
docker system prune --all
cd ~/hello-spring/
git pull
docker-compose up

# Try to access http://PublicIP/hello like http://ec2-18-182-66-63.ap-northeast-1.compute.amazonaws.com/hello
