pipeline {
    agent any
    

    stages {
        stage ("git required for doing testing in loans ") {
            steps {
                git 'https://github.com/k123-v/Apr-Project.git'
            }
        }
        
        stage("Connect to mvn and doing testing in loans branch") {
            steps {
                sh 'echo "welcome to testing in loans branch"'                  
            }
        }

    }

}