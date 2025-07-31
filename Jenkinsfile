pipeline{
    agent{
        label 'jenkins-slave'
    }
    stages{
        
        stage('Build'){
            steps{
            echo "********************Building Eureka Application********************"
            sh "mvn clean package"
        }
        }
    }
}