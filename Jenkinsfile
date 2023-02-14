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
//         sh 'cd main'
// //         echo "$PWD"
//         echo 'before printing directory list .'
//         echo .* *
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
