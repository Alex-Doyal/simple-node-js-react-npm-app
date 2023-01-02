pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''pipeline {
    agent {
        docker {
            image \'node:lts-bullseye-slim\' 
            args \'-p 3000:3000\' 
        }
    }
    stages {
        stage(\'Build\') { 
            steps {
                sh \'npm install\' 
            }
        }
    }
}
'''
        }
      }

    }
  }