pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                git credentialsId: 'github_key', url: 'https://github.com/sunnybhambhani/cicd-pipeline-train-schedule-pipelines.git'
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}
