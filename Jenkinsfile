
stage('all steps once') {
    node ('master') {
	     ws('/ds1/jenkins/workspace/myWorkflowTest') {
		     checkout scm
	    	     //build('multi_branch_roadlog_dsl')
	    	build job: 'multi_branch_roadlog_dsl_clean', parameters: [string(name: 'myparam', value: 'jeeee')]
	     }
    }
}
