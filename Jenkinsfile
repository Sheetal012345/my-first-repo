pipeline{
  agent any
  stages
    stage('Checkout'){
      steps{
        git 'https://github.com/Sheetal012345/my-first-repo'
      }
      
    }
  stage('Publish'){
    steps{
      publishHTML{[
        allowmissing:true,
          alwaysLinktoLastBuild:false,
          keepAll:false,
          reportDir:'.',
          reportFiles:'Hello.html',
        reportName:'myhtmlfile',
        ]
      }
    }
  }
}
