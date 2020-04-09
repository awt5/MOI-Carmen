pipeline {
    agent any
    stages {
        stage('Build'){
            steps{
                sh 'echo "Start Building app"'
            }
        }
        stage('Unit Test'){
            steps{
                sh 'echo "Running Tests"'
		        sh 'java -version'
            }
        }
        stage('Deploy'){
            parallel {
                stage('DeployToDevEnv'){
                    steps {
                        sh 'echo "Deploying to Dev enviroment"'
                    }
                }
                stage('DeployToQaEnv'){
                    steps {
                        sh 'echo "Deploying to QA environment"'
                    }
                }
            }

        }
    }
}
