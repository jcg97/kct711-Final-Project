node {
  stage ('Build') {
    withMaven {
      sh "mvn -B -DskipTests clean package"
    } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe reports and FindBugs reports
  }
}