pipeline {
  agent any
 
  stages {
    stage ('push_to_test') {
      steps {
        build job: 'push_to_test'
      }
    }
    stage {'test'){
      steps {
      if (push_to_test == 'success')
      build job: 'push_to_prod'
      
      }
    }
}
  }
