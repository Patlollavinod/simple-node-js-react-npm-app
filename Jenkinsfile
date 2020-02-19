pipeline {
         agent any
         //tools {nodejs "nodejs"}
         //f15275d15d373a3944edc01ebe4760951321d917

    stages {
        stage("Code Checkout") {
            steps {
                git branch: 'master',
                //The repository containing the sonar-project.properties
                url: 'https://github.com/edsherwin/simple-node-js-react-npm-app.git'
                  }
              }
         stage('Code Quality') {
                   steps {
                       script {
                         //
                         sh "pwd"
                         //This will call the sonar-scanner installed in the Jenkins, then it will used the sonar-project.properties configuration on the directory(workspace)
                         sh "/opt/sonar-scanner/bin/sonar-scanner -Dproject.settings=sonar-project.properties"
                                       }
                               }
                           }
            }
}
