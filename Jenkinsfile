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
  stages {
    stage('Test') {
      steps {
        helloWorld("issam","monday")
        sh '''
          git --version
          curl --version
        '''
      }
    }
  }
}
