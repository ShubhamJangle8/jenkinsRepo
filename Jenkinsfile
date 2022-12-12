pipeline{
    tools{
        maven 'mymaven'
    }
    
    agent any
    
    stages{
        stage('Clone repo')
        {
            steps{
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
            }
        }
        stage('Compile the code using maven')
        {
            steps{
                sh 'mvn compile'
            }
        }
        stage('Code review')
        {
            steps{
                sh 'mvn pmd:pmd'
            }
        }
         stage('Unit Testing')
        {
            steps{
                sh 'mvn test'
            }
        }
         stage('package')
        {
            steps{
                sh 'mvn package'
            }
        }
    }
}
