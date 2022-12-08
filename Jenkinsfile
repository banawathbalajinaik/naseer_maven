pipeline {
    agent any
    stages {
        stage ('git'){
           steps{
               sh '''
               rm -rf *
               git clone https://github.com/banawathbalajinaik/naseer_maven.git
               '''
           } 
        }
        stage ('maven'){
           steps{
               sh '''
               cd naseer_maven
               mvn clean
               '''
           } 
        }
        stage ('maven_test'){
           steps{
               sh '''
               cd naseer_maven
               mvn test
               '''
           } 
        }
        stage ('maven_compile'){
           steps{
               sh '''
               cd naseer_maven
               mvn compile
               '''
           } 
        }
        stage ('maven_install'){
           steps{
               sh '''
               cd naseer_maven
               mvn install
               '''
           } 
        }
    }
}
