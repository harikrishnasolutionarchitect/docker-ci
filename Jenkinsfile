pipeline {
  agent any
  stages {
    
    
   
    stage('ce-terraform-repo') {
      steps {
        git url:'https://github.com/harikrishnasolutionarchitect/docker-ci.git', branch:'main'
      }
    }
    
    
    stage('tfsec') {
  agent {
   docker {
     image 'tfsec/tfsec-ci:v0.57.1'
     reuseNode true
   }
  }
  steps {
   sh '''
     tfsec . --no-color
    '''

}
}


    
    
    
    
    
    
  }
}


