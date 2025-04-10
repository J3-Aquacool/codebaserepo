pipeline {
    agent any
    tools {
        maven "MAVEN"
            }
    stages {
        stage('Initialize'){
            steps{
              echo "PATH = ${env.M2_HOME}\\bin;${env.PATH}"
              echo "M2_HOME = ${env.M2_HOME ?: '/opt/maven'}"
            }
        }
        stage('Build') {
            steps {
                dir("D:\\demo2023-eclipse1\\eclipse-workspace\\DemoCICDMavenProject") {
                bat 'mvn -B -DskipTests clean compile package exec:java'
                }
            }
         
        }
      stage('Test') {
            steps {
                 dir("D:\\demo2023-eclipse1\\eclipse-workspace\\DemoCICDMavenProject")
                {
                bat 'mvn test'
                }
                }
         }
    
    }
    }
