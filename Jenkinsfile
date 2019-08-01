pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			steps {
				sh 'tidy -q -e *.html'
				withAWS(region:'us-east-2', credentials:'aws-static') {
				    s3Upload(file:'index.html', bucket:'uda-jenkins-pipeline', path:'index.html')
				}
			}
		}
	}
}