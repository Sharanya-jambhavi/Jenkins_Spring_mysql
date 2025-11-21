pipeline{
    agent any

    tools{
        maven 'maven'
    }
    stages{
        stage('Checkout'){
            steps{
                sh 'mvn clean package -DskipTests'
            }
        }
            
        stage('Build'){
            steps{
                sh 'mvn clean package'
            }
        }
    }
    post{
        always{
            echo 'This will always run'
        }
        success{
            echo 'This will run only if successful'
        }
        failure{
            echo 'This will run only if failed'
    }
}
