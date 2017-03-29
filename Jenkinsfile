pipeline{
stages{
stage('Build'){
steps{
sh 'javac -d . src/*.java'
sh 'echo Main-Class: Rectangulator > MAINFEST.MF'
sh 'jar -cvmf MANIFEST.MF rectangle.jar *.class'
}
}
stage('Run'){
steps{
sh 'java -jar rectangle.jar 4 5'
}
}
}
}
