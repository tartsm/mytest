
stage('checkout') {
    node ('master') {
	     ws('/ds1/jenkins/workspace/myWorkflowTest') {
		     checkout scm
	    	     //build('multi_branch_roadlog_dsl')
	     }
    }
}
stage('build') {
    node ('master') {
		env.WORKSPACE = '/ds1/jenkins/workspace/myWorkflowTest'
	    	build job: 'multi_branch_roadlog_dsl_clean', parameters: [string(name: 'WORKSPACE ', value: '/ds1/jenkins/workspace/myWorkflowTest')]
	     
    }
}
