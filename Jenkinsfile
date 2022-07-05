pipeline {
  agent {test-jnlp}
 
  tools {
  maven 'Maven3'
  }
  stages {
    stage ('push_to_test') {
      steps {
        build job: 'push_to_test'
      }
    }
    stage ('Build') {
      steps {
      sh 'mvn clean install -f MyWebApp/pom.xml'
      }
    }
    }
}
