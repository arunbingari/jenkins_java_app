pipeline {
    agent any
    parameters {
        choice(name: 'APP_VERSION', choices:['1.1.0','1.1.1','1.1.3'], description: 'Version of the application')
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Test the application')
    }
        stages {
        stage('build') {
            steps {
                script {
                    echo "Building the 2nd time application..."
                }
            }
        }
        stage('test') {
            steps {
                when {
                     params.executeTests 
                }
                script {
                    echo "Testing the application 2nd time ..."

                }
            }
        }
        stage('deploy') {
            steps {
                script {
                    echo "Deploying the application..."
                    echo "Deploying the veriosn ${params.APP_VERSION}"
                }
            }
        }
    }
}