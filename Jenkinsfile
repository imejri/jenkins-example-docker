library identifier: 'github-api-global-lib@main',
    // 'mylibraryname' is just an identifier, it can be anything you like
    // 'master' refers to a valid git ref (branch)
    retriever: modernSCM([
      $class: 'GitSCMSource',
      //credentialsId: 'your-credentials-id', // remove this if it's public!
      remote: 'https://github.com/imejri/github-api-global-lib.git'
])

pipeline {
  agent { label "centos" }
  options {
      durabilityHint('PERFORMANCE_OPTIMIZED')
      }
    
  //  environment {
        //BUILD_FOLDER = '/infra/build/'
   // }
  stages {
    stage('Test') {
      steps {
        helloWorldSimple('issam','lundi')
        sh '''
          git --version
          curl --version
        '''
      }
    }
  }
}
