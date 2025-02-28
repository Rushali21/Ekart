pipeline{
    agent {
        node {
            label 'slave1'
        }
    }
    stages  {
        stage ('maven version') {
            steps {
                sh 'mvn -v'
            }
        }
    }
    stage ('git clone repo')
    {
        steps {
            git branch: 'main', url: 'https://github.com/Rushali21/Ekart.git'
        }
    }
    stage ('maven build')
    {
        steps {
            sh 'mvn clean package'
        }
    }


}
