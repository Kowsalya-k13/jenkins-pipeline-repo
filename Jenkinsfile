@Library('test-shared-library') _

pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                gitCheckout('https://github.com/your-org/your-repo.git', 'main')
            }
        }
        stage('Build') {
            steps {
                buildApp('mvn clean package')
            }
        }
        stage('Deploy') {
            steps {
                deployApp('./scripts/deploy.sh')
            }
        }
    }
}
