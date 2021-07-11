pipeline {
    agent any
    

    stages {
        stage ("git required for doing testing in master") {
            steps {
                git 'https://github.com/k123-v/Apr-Project.git'
            }
        }
        
        stage("Connect to mvn and doing testing in master branch") {
            steps {
                sh 'echo "welcome to testing in master branch"'                  
            }
        }

    }

}
