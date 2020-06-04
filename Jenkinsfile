pipeline {
     agent any
	 stages {
	     stage('Upload to AWS') {
		     steps {
			     sh 'echo "Hello World"'
				 sh '''
				     echo "multiline shell steps work too"
					 ls -lah
			     '''
             }
		 }
    }		 
}
