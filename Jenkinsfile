pipeline{
  agent any
  tools{
    maven 'Maven'
    }
  stages{
    stage('checkout'){
      steps{
        git branch:'master',url:'https://github.com/srushtiiik/webappp.git'
        }
        }
   stage('build'){
     steps{
       sh 'mvn clean package'
       }
       }
   
   
  }
}
