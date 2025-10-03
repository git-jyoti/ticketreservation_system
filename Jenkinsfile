pipeline {
   agent any
  stages {
    stage('Cloning Git') {
      steps {
        git branch: 'main', url: 'https://github.com/Hemantakumarpati/ticket-reservation-system.git'
      }
    }
   stage('Compile Package and Create war file') {
      steps {
        sh "mvn package"
      }
    }
  }
}

    
    
  
