pipeline{

    agent {
        node {
            label 'workstation'
        }
    }

    options {
     ansicolor('xterm')
    }

    environment {
     SAMPLE_URL = "example.com"
    }

    stages {

        stage('One') {
                steps{
                    sh 'echo Hello World'
                    sh 'echo Hello Universe'
                    sh 'echo ${SAMPLE_URL}'
                }
        }
    }
    post {
        always {
            sh 'echo Post Cleanup steps'
        }
    }
}