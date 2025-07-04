@Library('test-shared-library') _

pipeline {
    agent any

    stages {
        // stage('Checkout') {
        //     steps {
        //         gitCheckout('', 'main')
        //     }
        // }
        stage('Build') {
            steps {
                buildApp('mvn clean package')
            }
        }
        // stage('Deploy') {
        //     steps {
        //         deployApp('./scripts/deploy.sh')
        //     }
        // }
    }
}
