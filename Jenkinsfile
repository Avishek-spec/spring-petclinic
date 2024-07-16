#!groovy
pipeline {
    agent any

    stages {
        stage('MavenPackage') {
            steps {
                   
                sh './mvnw package'

            }
        }

        stage('DockerBuild') {
            steps {
                     
                    sh 'docker build -t avisheksarkar2024/springpetclinic:latest .'
                   }
           }

        stage('Imagepush') {
            steps {
                     
                    sh 'docker push avisheksarkar2024/springpetclinic:latest '
                   }
           }

      }
   
   }
