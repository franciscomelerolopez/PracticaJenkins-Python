pipeline {
    agent any

    stages {
        stage('Construir') {
            steps {
                echo "          -------------CONSTRUYENDO MI SOFTWARE/CODE"
                echo "          Creando entorno virtual"
                sh 'virtualenv entorno_virtual'
                echo "          Activando el entorno_virtual"
                sh '. entorno_virtual/bin/activate'
                //sh 'pip3 --version'
                //echo "          Instalando los requerimientos concretos de este proyecto"
                //sh 'pip3 install -r requirements.txt'
                echo "          Instalando aplicación para testear"
                sh 'pip3 install pytest'
                echo "           Instalado aplicación/libreria necesaria para este proyecto concreto"
                sh 'pip3 install flask'
                echo "           Terminando de instalar requerimientos"
            }
        }
        stage('Test') {
            steps {
                echo "Ejecutando y probando"
                sh 'python ./src/main.py'
                //cd src && pytest && cd ..
                //echo "            Puedes probarla durante 20 segundos esta aplicación en modo local"   
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }   
}
