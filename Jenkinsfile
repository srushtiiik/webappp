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
   s
   stage('deploy'){
     steps{
       sh 'mvn clean package'
       sh 'ansible-playbook ansible/playbook.yml -i ansible/hosts.ini'
       }
       }
  }
}
