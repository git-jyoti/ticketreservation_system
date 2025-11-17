pipeline {
   agent any
    tools {
    maven 'maven'  // Matches the name in Global Tool Configuration
  }
environment { 
   NAME = "ticketreservation_system"
   VERSION = "${env.BUILD_ID}-${env.GIT_COMMIT}"
   IMAGE = "${NAME}:${VERSION}"
   IMAGE_REPO="jyotipmohapatra"
   IMAGE_URL='hub.docker.com'
   
}
  stages {
    stage('Cloning Git') {
      steps {
      git branch: 'main', url: 'https://github.com/git-jyoti/ticketreservation_system.git'
      }
    }
    stage('Compile Package and Create war file') {
      steps { 
        sh "mvn package"
      }
    }
  }
}
    
    
  
