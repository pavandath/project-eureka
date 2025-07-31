pipeline{
    agent{
        label 'jenkins-slave'
    }
    stages{
        steps{
        stage('Build'){
            echo "********************Building Eureka Application********************"
            sh "mvn clean package"
        }
        }
    }
}