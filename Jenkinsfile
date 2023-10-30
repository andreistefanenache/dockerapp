pipeline {
    agent any
    stages{
/*        stage('Build') {
            steps {
                sh 'docker build -t dockerapp .'
            }
        } */
        stage('Deploy') {
            steps {
		sh 'docker compose up -d'
            }
        }
    }
}
