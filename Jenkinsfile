pipeline {
    agent any 

    stages  {
        stage('Checkout')   {
            steps {
                echo "Checkout the source code from the git repository"
                git clone 'https://github.com/atharva0300/calculator'
            }
        }

        stage('Build')  {
            steps {
                echo "Execute build commands or scripts"
                chmod u+x hello.sh
                ./hello.sh
            }
        }

        stage('Test')   {
            steps{
                echo "Execute test commands or scripts"
                chmod u+x test.sh
                ./test.sh
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