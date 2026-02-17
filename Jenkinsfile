pipeline {
    agent any 

    stages  {
        stage('Build')  {
            steps {
                echo "Execute build commands or scripts"
                sh 'chmod u+x hello.sh'
                sh './hello.sh'
            }
        }

        stage('Test')   {
            steps{
                echo "Execute test commands or scripts"
                sh 'chmod u+x test.sh'
                sh './test.sh'
            }
        }
    }

    post {
        success {
            echo "Deployment was successful"
        }
        failure {
            echo "Deployment was failure"
        }
    }
}