pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
		sh '''
		export AWS_DEFAULT_REGION=us-east-1 &&
		export AWS_ACCESS_KEY_ID=AKIA5QFEMYR4NKA6U5XT &&
		export AWS_SECRET_ACCESS_KEY=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 
		aws s3 sync . s3://121284source --exclude './.git/'
		'''
            }
        }
    }
}
