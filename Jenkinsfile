@Library('my-shared-library') _
pipeline {
    agent any
    parameters {
     choice choices: ['create', 'delete'], description: 'choose create or delete', name: 'action'          
    }
    stages {
        stage('Git CheckOut'){
            when { expression {  params.action == 'create' } }
            steps{
            //git branch: 'main', credentialsId: 'sonar-api', url: 'https://github.com/anilcloudgyan/mrdevops_java_app.git'
            gitCheckout(
                branch: "main",
                url:"https://github.com/anilcloudgyan/mrdevops_java_app.git"
            )
            }
        }
        stage("Unit Test maven"){
            when { expression {  params.action == 'create' } }
            steps{
                script{
                    //sh 'mvn test' 
                    mvnTest()
                }
            }
        }
        stage("Integartion Test maven"){
            when { expression {  params.action == 'create' } }
            steps{
                script{
                    //sh 'mvn verify -DskipUnittests'
                    mvnIntergrationTest()
                }
            }
        }
    }
}
