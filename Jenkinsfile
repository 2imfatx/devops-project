pipeline {
  agent {
    node{
     label 'docker-agent-alpine'
    }
  }
  triggers {
    pollSCM '* * * * *'
  }
  stages{
    stage('Build'){
      steps{
       echo 'Building..' 
      }
    }
  }

  
}
