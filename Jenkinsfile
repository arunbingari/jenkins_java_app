pipeline {
    agent any
    parameters {
        choice(name: 'APP_VERSION', choices:['1.1.0','1.1.1','1.1.3'], description: 'Version of the application')
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Test the application')
    }
        stages {
        stage('build') {
            steps {
               
                    echo "Building ..."
                
            }
        }
        stage('test') {
           
                when {
                    expression { 
                        params.executeTests 
                    }
                }
                steps {
                    echo "Testing ..."

                }
            
        }
        stage('deploy') {
            steps {
                
                    echo "Deploying ..."
                    echo "Deploying the veriosn ${params.APP_VERSION}"
                }
            }
        }
    }