pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git branch: 'main', credentialsId: 'pipelineJobGit', url: 'https://github.com/prithvigowda99/pipelinejob.git'
        echo "this is build stage"
      }
    }
    stage('Deploy') {
      steps {
        git branch: 'main', credentialsId: 'pipelineJobGit', url: 'https://github.com/prithvigowda99/jenkins.git'
        echo "this is deploy stage"
      }
    }
    stage('Test') {
      steps {
        sh '''
          pwd
          ls -lrt
        '''
        echo "this is test stage"
      }
    }
    stage('Parallel Execution') {
      steps {                    // ✅ REQUIRED: steps wrapper
        parallel {
          stage('Chrome') {
            steps {              // ✅ REQUIRED: each parallel stage needs steps
              echo "executing in chrome browser"
            }
          }
          stage('Firefox') {
            steps {              // ✅ REQUIRED: each parallel stage needs steps
              echo "executing in firefox browser"
            }
          }
        }
      }
    }
  }
}
