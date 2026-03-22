pipeline {
  agent any
  stages {
    stage('check out / git') {
      steps {
        git(url: 'https://github.com/saumya-dutta/maven-samples', branch: 'master')
      }
    }

    stage('run') {
      steps {
        sh '''export JAVA_HOME=$(/usr/libexec/java_home -v 1.8)
export PATH=$JAVA_HOME/bin:$PATH

java -version
mvn verify'''
      }
    }

  }
}