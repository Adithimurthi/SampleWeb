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
		export AWS_ACCESS_KEY_ID=AKIAJRWZWY3CPV3F3JPQ
		export AWS_SECRET_ACCESS_KEY=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
		aws s3 sync . s3://121284source --exclude '.git'
		'''
            }
        }
    }
}
