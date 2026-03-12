pipeline{
  agent any
  stages{
    stage('Checkout'){
      steps{
        git 'https://github.com/Sheetal012345/my-first-repo.git'
      }
      
    }
  stage('Publish'){
    steps{
      publishHTML([
        allowMissing:true,
          alwaysLinkToLastBuild:false,
          keepAll:false,
          reportDir:'.',
          reportFiles:'Hello.html',
        reportName:'myhtmlfile',
        ]
      )
    }
  }
}}
