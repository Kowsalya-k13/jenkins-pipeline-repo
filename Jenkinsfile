@Library('test-shared-library') _

pipeline {
    agent any

    stages {
        stage('First Stage') {
            steps {
                gitCheckout('', 'main')
            }
        }
        stage('Second Stage') {
            steps {
                buildApp('mvn clean package')
            }
        }
        stage('Third Stage') {
            steps {
                deployApp('./scripts/deploy.sh')
            }
        }
    }
}
