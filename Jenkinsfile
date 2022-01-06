pipeline {
  agent { dockerfile true }
  options {
      durabilityHint('PERFORMANCE_OPTIMIZED')
      }
  stages {
    stage('Test') {
      steps {
        sh '''
          git --version
          curl --version
        '''
      }
    }
  }
}
