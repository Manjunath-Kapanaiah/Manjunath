pipeline {
    agent any
    tools {
        // 'mymaven' must be configured in Jenkins Global Tool Configuration
        maven 'mymaven' 
    }
    stages {
        stage('Clone code') {
            steps {
                // The 'git' step is a built-in cross-platform step
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
            }
        }
        stage('Maven Compile') {
            steps {
                // CHANGED: Use 'bat' for Windows Command Prompt
                bat 'mvn compile'
            }
        }
        stage('Maven Test') {
            steps {
                // CHANGED: Use 'bat' for Windows Command Prompt
                bat 'mvn test'
            }
        }
        stage('Maven Install (Package & Install)') {
            steps {
                // CHANGED: Use 'bat' for Windows Command Prompt
                bat 'mvn install'
            }
        }
    }
}
