pipeline {
  agent any
 
  stages {
    
    stage ('push_to_test') {
      steps {
        build job: 'push_to_test'
        result = check
      }
    }
    stage ('test'){
      steps {
      if (check == 'success')
      build job: 'push_to_prod'
      
      }
    }
}
  }
