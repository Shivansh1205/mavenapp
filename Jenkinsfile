pipeline{
agent any
tools{
maven 'Maven'
configured inJenkins
}
stages{
stage('Checkout'){
steps{
git branch:'main',url'https://github.com/Shivansh1205/mavenapp'
}
}
stage('Build'){
steps{
sh'mvn clean package'
}
}
stage('Test'){
steps{
sh 'mvn test'
}
}
stage('Run Application'){
steps{
sh 'java -jar target/mavenapp=1.0-SNAPSHOT.jar'
}
}
}
post{
success{
echo 'build'
}
failure{
echo 'fail'
}
}
}
