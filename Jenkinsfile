

pipeline {
agent any
stages {
stage('Clone repository') {
steps {
checkout([$class: 'GitSCM',
branches: [[name: '*/main']],
userRemoteConfigs: [[url: 'https://github.com/Jatinsharma159/Jenkins.git']]])
}
}
stage('Build') {
steps {
build 'PES2UG21CS193-1'
sh 'g++ Pipe.cpp -o output'
}
}
stage('Test') {
steps {
sh './output'
}
}
stage('Deploy') {
steps {
echo 'deploy"
}
}
}
post{
failure{
error 'Pipeline failed'
}
}
}
