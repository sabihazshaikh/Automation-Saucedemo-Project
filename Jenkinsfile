pipeline{
    agent any
    stages{
        stage('Checkout'){
            steps{ git 'https://github.com/laxmiambekar1096/Automation_Projects.git'}
        }
        stage('Build'){
            steps { bat 'mvn clean install' }
        }
        stage('Test'){
            steps{ bat 'mvn test' }
        }
    }
    post{
        always { junit 'target/surefire-reports/*.xml'
    }
}
}
