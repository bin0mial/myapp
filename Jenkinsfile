pipeline {
    agent {label "server1"}
    stages {
        stage('Hello') {
            steps {
                echo "Hello world!"
            }
        }
        stage('cat README.md') {
            when {
                branch "fix-*"
            }
            steps {
                sh '''
                    cat README.md
                '''
            }
        }
        stage('install dependencies') {
            steps {
                sh 'npm i'
            }
        }
        stage('start server') {
            steps {
                sh 'sudo systemctl restart myapp'
            }
        }
    }
}
