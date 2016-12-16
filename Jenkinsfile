jobDsl scriptText: '''job(\'mytest_2_roadlog_dsl_clean_install\') {
	
	customWorkspace(\'/ds1/jenkins/workspace/myWorkflowTestGit\')
	
	jdk(\'jdk1.8.0_45_x86_linux\')
	
	steps{
		    maven {
				mavenInstallation(\'Maven 3\')
				goals(\'clean install\')
				mavenOpts(\'-Xrs -Xmx1024M -Xss20M -XX:MaxPermSize=1024M -XX:ReservedCodeCacheSize=64M -XX:+UseGCOverheadLimit\')
				rootPOM(\'pom.xml\')
			}

	}//steps

}//mytest_2_roadlog_dsl_clean_install'''


stage('first step on first node') {
// Mark the code checkout 'stage'....
    node ('master') {
        ws('/ds1/jenkins/workspace/myWorkflowTestGit') {
            // Checkout code from repository
            checkout scm
            // Run the maven build
            mytest_2_roadlog_dsl_clean_install()
            }
        }
    }
}
