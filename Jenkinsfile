pipeline { 
 agent any 
 environment { 
 // Set JAVA_HOME to the path of your Java 17 installation 
 JAVA_HOME = 'C:/Program Files/Java/jdk-21' 
 // Add Java bin directory to PATH 
 PATH = "${JAVA_HOME}\\bin;${env.PATH}" 
 } 
 tools { 
 maven 'maven' 
 } 
 stages { 
 stage('GetCode') { 
 steps { 
 git branch: 'main', url: 'https://github.com/kingtheraja/kingthearaja.git' 
 } 
 } 

 } 
}
