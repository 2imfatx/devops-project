pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Build') {
      environment {
        CXX = 'g++' // or any other C++ compiler you have installed
      }

      steps {
        sh "${CXX} -o my_app hello.cpp" // replace main.cpp with the name of your C++ source file
      }
    }

    stage('Test') {
      steps {
        sh './my_app' // replace my_app with the name of your compiled executable
      }
    }
  }
}
