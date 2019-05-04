
node {
  stage('checkout sources') {
        // You should change this to be the appropriate thing
        git url: 'https://github.com/sstarkey7/special-topics-labs-ci.git'
  }

  stage('Build') {
    // you should build this repo with a maven build step here
    withMaven (maven: 'maven3') {
              sh "mvn package"
            }

  }

  junit 'target/surefire-reports/*.xml'

}
