pipeline {
  agent any
  tools {
    maven 'Maven'
    jdk 'JDK'
  }
  stages{
  stage('Checkout'){
  branch:'master' url:'https://github.com/RachanaN-27/maven-jenkins.git'
  }
stage('Build'){
sh 'mvn clean package'
}
stage('Test'){
sh 'mvn test'
}
stage('run Application'){
sh 'java -jar target/mavne-jenkins-1.0-SNAPSHOT.jar'
}
}
post{
success{
echo "Build Successful"
}
failure{
echo "Build failure"
}
}
}
