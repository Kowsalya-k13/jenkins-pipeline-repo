@Library('test-shared-library') _

pipeline {
    agent any

    stages {
        stage('First Stage') {
            steps {
                gitCheckout('https://github.com/BBrucelee2002/argocd-testing.git', 'main')
            }
        }
        stage('Second Stage') {
            steps {
                buildApp()
            }
        }
        stage('Third Stage') {
            steps {
                deployApp()
            }
        }
    }
}
