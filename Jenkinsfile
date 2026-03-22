pipeline {
  agent any

  tools {
    jdk 'JDK_HOME'
    maven 'MVN'
  }

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Build') {
      steps {
        sh '''
          java -version
          mvn -version
          mvn verify
        '''
      }
    }
  }
}
