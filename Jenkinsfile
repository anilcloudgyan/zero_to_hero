/* groovylint-disable-next-line CompileStatic */
pipeline {
    agent any
    {
        stages {
            stage('Git CheckOut'){
                steps{
                    script{
                        git branch: 'main', credentialsId: 'sonar-api', url: 'https://github.com/anilcloudgyan/mrdevops_java_app.git'
                    }
                }
            }
        }
    }
}
