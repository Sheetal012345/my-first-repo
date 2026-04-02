pipeline{
  agent any
  stages{
    stage('Checkout'){
      steps{
        git url:'https://github.com/Sheetal012345/my-first-repo.git',branch :'master'
      }
      
    }
  stage('Build Image'){

    steps {
      bat 'docker build -t mywebsite .'
    }
  } 
  stage ('Stop old container'){
    steps{
      bat 'docker stop mycont || exit 0'
      bat 'docker rm mycont || exit 0'
    }
  }
  stage ('Run Image - Containerize'){
    steps{
      bat 'docker run -d -p 7000:80 --name mycont mywebsite'
    }
  }
  
}}
