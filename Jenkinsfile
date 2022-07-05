pipeline {
  agent any
 
  stages {
    stage ('push_to_test') {
      steps {
        build job: 'push_to_test'
        result 
      }
    }
    stage ('test'){
      steps {
      if (bool == 'success')
      build job: 'push_to_prod'
      
      }
    }
}
  }
