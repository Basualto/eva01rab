pipeline {
    agent any
    stages {
        stage('Clonar Repositorio') {
            steps {
                git branch: 'main', url: 'https://github.com/KeldarWolf/ProyectoRetailOff.git'
                echo 'El repositorio se ha descargado exitosamente'
            }
        }
        stage('Verificar Dependencias') {
            steps {
                echo '--Revisando las dependencias requeridas para el proyecto...'
                // Aquí puedes incluir comandos específicos de tu proyecto, como validar archivos o dependencias
            }
        }
        stage('Compilar Proyecto') {
            steps {
                echo '--Iniciando el proceso de compilación...'
                // Comando para compilar, por ejemplo:
                // sh './gradlew build' o 'mvn clean install'
            }
        }
        stage('Ejecutar Pruebas') {
            steps {
                echo '--Corriendo las pruebas definidas en el proyecto...'
                // Comando para ejecutar pruebas, por ejemplo:
                // sh './gradlew test'
            }
        }
        stage('Desplegar Proyecto') {
            steps {
                echo '--Realizando el despliegue de la aplicación...'
                // Aquí puedes incluir comandos para desplegar, como copiar archivos a un servidor
            }
        }
    }
}
