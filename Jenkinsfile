pipeline {
  agent any

        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/ellsalif/api_auto.git'
            }
        }
    stage('Testing') {
      steps {
        bat 'Tests/api.robot'
      }
    }
    stage('Reporting') {
      steps {
        archiveArtifacts 'log.html, output.xml, report.html'
      }
    }

  }

