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
                sh 'docker run -d -p 5000:5000 --name $JOB_NAME dockerapp'
            }
        }
    }
}
