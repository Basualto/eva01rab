pipeline {
    agent any
    
    tools {
        git 'Git'
    }
    
    stages {
        stage('Checkout') {
            steps {
                script {
                    try {
                        // Limpia el workspace
                        deleteDir()
                        
                        // Intenta clonar el repositorio
                        checkout([
                            $class: 'GitSCM',
                            branches: [[name: '*/main']],
                            extensions: [],
                            userRemoteConfigs: [[
                                url: 'https://github.com/Basualto/eva01rab.git'
                                // No es necesario credentialsId si el repositorio es público
                            ]]
                        ])
                    } catch (Exception e) {
                        // Manejo de errores
                        echo "Error al clonar el repositorio: ${e.message}"
                        currentBuild.result = 'FAILURE'
                        throw e
                    }
                }
            }
        }
    }
}
