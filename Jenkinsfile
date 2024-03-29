pipeline {
  agent any
  tools { 
      maven 'DHT_MVN' 
      jdk 'DHT_SENSE' 
  }

  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/crustyapples/maven-samples', branch: 'master')
      }
    }

    stage('run') {
      steps {
        sh 'mvn test'
        sh 'mvn verify'
        sh 'mvn clean'
      }
    }

  }
  tools {
    maven 'DHT_MVN'
    jdk 'DHT_SENSE'
  }
}
