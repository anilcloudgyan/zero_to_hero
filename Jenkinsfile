@Library('my-shared-library') _
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
        stage("Unit Test MVN"){
            steps{
                script{
                    //sh 'mvn test' 
                    mvnTest()
                }
            }
        }
        stage("Integartion "){
            steps{
                script{
                    sh 'mvn verify -DskipUnittests   '
                }
            }
        }
    }
}
