node {
  stage ('Build') {
    git url: 'https://github.com/cyrille-leclerc/multi-module-maven-project'
    withMaven {
      sh "mvn -B -DskipTests clean package"
    } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe reports and FindBugs reports
  }
}