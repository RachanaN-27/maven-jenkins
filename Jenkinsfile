pipeline {
  agent any
  tools {
    maven 'Maven'
    jdk 'JDK'
  }
  stages{
  stage('Checkout'){
    steps {
  branch:'master' url:'https://github.com/RachanaN-27/maven-jenkins.git'
  }
  }
stage('Build'){
  steps{
sh 'mvn clean package'
  }
}
stage('Test'){
  steps {
sh 'mvn test'
  }
}
stage('run Application'){
  steps {
sh 'java -jar target/mavne-jenkins-1.0-SNAPSHOT.jar'
  }
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
