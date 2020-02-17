node {
  stage('Checkout') {
    git 'https://github.com/edsherwin/simple-node-js-react-npm-app.git'
  }
  stage('build & SonarQube Scan') {
    //withSonarQubeEnv('sonarqube') {
      //sh 'mvn clean package sonar:sonar'
      sonar-scanner --version
    } // SonarQube taskId is automatically attached to the pipeline context
  }
}
 
// No need to occupy a node
// stage("Quality Gate") {
//   timeout(time: 1, unit: 'HOURS') { // Just in case something goes wrong, pipeline will be killed after a timeout
//     def qg = waitForQualityGate() // Reuse taskId previously collected by withSonarQubeEnv
//     if (qg.status != 'OK') {
//       error "Pipeline aborted due to quality gate failure: ${qg.status}"
//     }
//   }
// }