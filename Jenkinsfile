pipeline{
 agent any
stages{
stage('Build'){
steps{
sh 'javac -d . src/*.java'
sh 'echo Main-Class: Rectangulator > MANIFEST.MF'
sh 'jar -cvmf MANIFEST.MF rectangle.jar *.class'
}
}
stage('Run'){
steps{
sh 'java -jar rectangle.jar 4 5'
}
}
 stage('Test'){
  steps{
   
  }
}
post{
success{
archiveArtifacts artifacts: 'rectangle.jar', fingerprint:true
}
}

}
