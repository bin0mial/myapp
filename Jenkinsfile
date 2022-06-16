pipeline {
    agent {label "linux"}
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
                sh ```
                    cat README.md
                ```
            }
        }
    }
}
