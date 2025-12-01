pipeline{
  agent any
    stages {
      stage ('Build') {
        agent { label 'node-1' }
        steps {
          echo "this is build stage"
        }
      }
    
  stage ('Deploy') {
    agent { label 'node-2' }
    steps {
      echo "this is deploy stage"
    }
  }
      stage ('test') {
        agent any
        steps {
          echo "this is test stage"
        }
      }
      
    }  
}
