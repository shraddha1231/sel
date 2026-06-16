pipeline{
agent any
 tools{
  maven 'Maven'
  }
  stages{
  stage('Checkout'){
  steps{
   git branch : 'master',url:'https://github.com/shraddha1231/sel.git'
   }
   }
 
 stage('Build'){
  steps{
   sh 'mvn clean package'
   }
   }
 stage('Test'){
  steps{
   sh 'mvn test'
   }
   }
  stage('Run Application'){
  steps{
   sh 'mvn exxec:java -Dexec.mainClass=com.example.App'
   }
   }
   }
   post{
   success{
   echo "yes"
   }
   failure{
   echo "fail"
   }
   }
   }
