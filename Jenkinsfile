pipeline {
     agent any
	 stages {
	     stage('Lint HTML') {
		    steps {
			  sh 'tidy -q -e *.html'
			  }
			  }
	 stages {
	     stage('Upload to AWS') {
		    steps {
		       sh 'echo "Hello World1"'
                 sh '''
                     echo "Multiline shell steps works too"
                     ls -lah
                 '''
                  withAWS(region:'us-west-2',credentials:'aws-static') {
                  sh 'echo "Uploading content with AWS creds"'
                      s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'hammadhammad')
				}
			}
		}
	}
}	
}


