stage('first step on first node') {
// Mark the code checkout 'stage'....
    node ('master') {
        ws('/ds1/jenkins/workspace/myWorkflowTestGit') {
            // Checkout code from repository
            checkout scm
            // Run the maven build
            withMaven(jdk: 'jdk1.8.0_45', maven: 'Maven 3') {
                sh "mvn clean install"
            }
        }
    }
}
