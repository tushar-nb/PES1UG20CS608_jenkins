pipeline {
  agent any
  stages {
    stage('Build'){
      steps{
        sh 'g++ -o a pipeline.cpp'
        echo 'Build stage successful'
      }
    }
    stage('Test'){
      steps{
        sh './a'
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
