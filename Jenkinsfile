pipeline {
    agent none
    stages{
        stage('Docker Push') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'dockerhub', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
                    sh "docker login -u $USERNAME -p $PASSWORD"
                    sh "docker push myimage:$BUILD_NUMBER"
                }
            }
        }
    }
}
