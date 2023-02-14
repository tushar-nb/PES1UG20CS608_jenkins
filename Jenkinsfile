pipeline {
  agent any
  stages {
    stage('Build'){
      steps{
        
        sh 'cd main && g++ -o a pipeline.cpp'
        build 'PES1UG20CS608-1'
        echo 'Build stage successful'
      }
    }
    stage('Test'){
      steps{
        sh 'cd main'
//         echo "$PWD"
        echo .* *
        sh './a.exe'
        echo 'test stage successful'
//         post{
//           always{
//             junit 'target/surefire-reports/*.xml'
//           }
//         }
     }
    }
    stage('Deploy'){
      steps{
        sh 'scp myprogram user@server:/path/to/deploy'
        echo 'Deployment successful'
      }
    }
  }
  post{
    failure{
      echo 'pipeline failed'
    }
  }
}
