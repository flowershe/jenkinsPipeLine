pipeline {
  agent {
    docker {
      image 'maven:3.3.9-jdk-8'
      args '-v /Users/floreshe/.m2:/root/.m2'
    }
    
  }
  stages {
    stage('Initialize') {
      steps {
        sh 'echo PATH = ${PATH} echo M2_HOME = ${M2_HOME} maven clean'
      }
    }
    stage('Build') {
      steps {
        sh 'mvn clean install -DskipTests'
      }
    }
  }
}