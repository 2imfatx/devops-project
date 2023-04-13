pipeline {
  agent {
    node{
     label 'docker-agent-alpine'
    }
  }
  triger {
    pollSCM '* * * * *'
  }
  stages{
    stage('Build'){
      steps{
       echo 'Building..' 
      }
    }

  
}
