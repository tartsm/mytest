
stage('all steps once') {
    node ('master') {
	     ws('/ds1/jenkins/workspace/myWorkflowTest') {
		     checkout scm
	    	     build('multi_branch_roadlog_dsl')
	    //build job: 'mytest_2_roadlog_dsl_clean_install', parameters: [string(name: 'MESSAGE', value: 'jeeee')]
	     }
    }
}
