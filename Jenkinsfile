pipline{
    agent{
        'jenkins-slave'
    }
    stages{
        stage('Build'){
            echo "********************Building Eureka Application********************"
            sh "mvn clean package"
        }
    }
}