pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			steps {
				withAWS(region:'us-east-2', credentials:'AKIAX6QGKHSVK36OX5FQ') {
				    s3Upload(file:'index.html', bucket:'uda-jenkins-pipeline', path:'./')
				}
			}
		}
	}
}