pipeline {
agent any

stages{
stage('Build'){
steps{
     sh "composer install"
}
}
stage("Test"){
steps {
sh 'vendor/bin/phpunit tests'
}
}
stage('Deploy'){

steps{

    sh 'docker-compose up -d'
}
}
}
}
