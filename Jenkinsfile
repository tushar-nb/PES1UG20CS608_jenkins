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
        sh 'cd main && ./a'
        echo 'test stage successful'
     }
    }
//     stage('Deploy'){
//       steps{
//         sh 'scp myprogram user@server:/path/to/deploy'
//         echo 'Deployment successful'
//       }
//     }
//   }
  post{
    always{
      echo 'pipeline is success'
    }
    failure{
      echo 'pipeline failed'
    }
    
  }
}
