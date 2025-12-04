pipeline{
  agent any
    stages {
      stage ('Build') {
        
        steps {
          git branch: 'main', credentialsId: 'pipelineJobGit', url: 'https://github.com/prithvigowda99/pipelinejob.git'
          echo "this is build stage"
        }
      }
    
  stage ('Deploy') {
    
    steps {
      echo "this is deploy stage"
    }
  }
      stage ('test') {
      
        steps {
          echo "this is test stage"
        }
      }
      
    }  
}
