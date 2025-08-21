pipeline {
    agent any // Exécute cette pipeline sur n'importe quel agent disponible
    stages {
        // Étape pour le "Build"
        stage('Build') {
            steps {
                echo 'Début du processus de build...'
            }
        }

        // Étape pour le "Test"
        stage('Test') {
            steps {
                // Le bloc 'script' permet d'utiliser du code plus complexe
                script {
                    if (fileExists('index.html')) {
                        echo 'Vérification réussie : le fichier index.html existe.'
                    } else {
                        // Fait échouer la pipeline si le fichier n'est pas trouvé
                        error 'Test échoué : le fichier index.html est manquant !'
                    }
                }
            }
        }
    }
}
