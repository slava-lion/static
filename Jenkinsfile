pipeline {
	agent any 
	stages {
		stage('Upload to AWS') {
            steps {
                withAWS(region:'us-west-2', credentials:'43920f14-1a06-496f-9cbc-b46b6ce31e2f') {
                sh 'echo "Uploading content with AWS creds"'
                	s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkinsproject3udacity')
                }
            }
        }
	}
}