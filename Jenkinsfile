pipeline {
         agent any
         tools {nodejs "nodejs"}

    stages {
        stage("Code Checkout") {
            steps {
                git branch: 'master',
                credentialsId: 'jenkins',
                url: 'https://github.com/edsherwin/simple-node-js-react-npm-app.git'
                  }
              }
         stage('Code Quality') {
                   steps {
                       script {
                          def scannerHome = tool 'sonar-scanner';
                          withSonarQubeEnv("sonarqube") {
                          sh "${tool("sonar-scanner")}/bin/sonar-scanner"
                                       }
                               }
                           }
                        }

        //  stage("Install Dependencies") {
        //                           steps {
        //                                 sh "npm install"

        //                                }
        //                         }
             }
     }