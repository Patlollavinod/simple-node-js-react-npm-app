pipeline {
         agent any
         //tools {nodejs "nodejs"}
         //f15275d15d373a3944edc01ebe4760951321d917

    stages {
        stage("Code Checkout") {
            steps {
                git branch: 'master',
                //credentialsId: 'jenkins',
                url: 'https://github.com/edsherwin/simple-node-js-react-npm-app.git'
                  }
              }
         stage('Code Quality') {
                   steps {
                       script {
                         //
                         sh "pwd"
                         sh "/opt/sonar-scanner/bin/sonar-scanner -Dproject.settings=sonar-project.properties"
                                       }
                               }
                           }
                        }
             }
     }
