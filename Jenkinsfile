pipeline {
  agent {
    node{
     label 'docker-agent-alpine'
    }
  }
  trigger {
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
