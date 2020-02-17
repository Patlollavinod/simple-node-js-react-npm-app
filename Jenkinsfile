node {
  stage('SCM') {
    git 'https://github.com/edsherwin/simple-node-js-react-npm-app.git'
    sh sonar-scanner
  }
//   stage('SonarQube analysis') {
//     def scannerHome = tool 'SonarScanner 4.0';
//     withSonarQubeEnv('SonarQube') { // If you have configured more than one global server connection, you can specify its name
//       sh "${scannerHome}/bin/sonar-scanner"
//     }
//   }
}