pipeline {
    agent any
    stages{
        stage('Build') {
            steps {
                sh 'docker build -t dockerapp .'
            }
        }
        stage('Deploy') {
            steps {
		sh 'docker stop $(docker ps -q)'
		sh 'docker rm $(docker ps -a -q)'
                sh 'docker run -d -p 5000:5000 dockerapp'
            }
        }
    }
}
