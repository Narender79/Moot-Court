pipeline {
    agent any
    environment {
        GITHUB_TOKEN = credentials('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') // your Jenkins credential ID
    }
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/Narender79/Moot-Court.git', credentialsId: 'github-token'
            }
        }
        stage('Build') {
            steps {
                echo 'Building project...'
                // your build commands here
            }
        }
        stage('Archive') {
            steps {
                archiveArtifacts '**/target/*.jar' // or the right path for your project
            }
        }
    }
}
