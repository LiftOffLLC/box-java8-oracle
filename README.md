Wercker Oracle Java 8 box
=========================

Wercker box with Oracle Java 8, maven3, git, ruby and heroku toolbelt installed

Basic working example 
---------------------

To build simple Java 8 application You just have to create ```wercker.yml``` file with following content and place in the root of your Java project.

```yml
box: LiftOffLLC/java8-oracle@1.0
build:
  steps:
    - script:
        name: Show base information
          code: |
            echo $JAVA_HOME
            java -version
            javac -version
      - script:
          name: Maven package
          code: mvn package
```


