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
       sh 'mvn clear package'
       }
       }
   stage('Archive'){
     steps{
       archetypeArtifacts artifacts: 'target/*.war',fingerprint:true
       }
       }
   stage('deploy'){
     steps{
       sh 'mvn clean package'
       sh 'ansible-playbook ansible/playbook.yml -i ansible/hosts.ini'
       }
       }
  }
}
