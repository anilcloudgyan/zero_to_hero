@Library('my_jenkins_shared_lib') _
pipeline {
    agent any
    stages {
        stage('Git CheckOut'){
            steps{
            //git branch: 'main', credentialsId: 'sonar-api', url: 'https://github.com/anilcloudgyan/mrdevops_java_app.git'
            gitCheckout(
                branch: "main",
                url:"https://github.com/anilcloudgyan/mrdevops_java_app.git"
            )
            }
        }
    }
}
