# mvn-repository
Myself maven repository

## Usage
### add user and password
change `~/.m2/settings.xml`

```xml
<settings>
  <servers>
    <server>
      <id>github-spiderpool-mvn-repository</id>
      <username>YOUR-USERNAME</username>
      <password>YOUR-PASSWORD</password>
    </server>
  </servers>
</settings>
```

### change pom.xml
`pom.xml`:
```xml
<repositories>
     <repository>
        <id>github-spiderpool-mvn-repository</id>
        <name>github-spiderpool-mvn-repository</name>
        <url>https://raw.githubusercontent.com/SpiderPool-New/mvn-repository/main/repository</url>
        <snapshots>
            <enabled>true</enabled>
            <updatePolicy>always</updatePolicy>
        </snapshots>
    </repository>
</repositories>
```
或
```xml
<repositories>
    <repository>
        <id>github-spiderpool-mvn-repository</id>
        <name>github-spiderpool-mvn-repository</name>
        <url>https://raw.github.com/SpiderPool-New/mvn-repository/main/repository</url>
        <snapshots>
            <enabled>true</enabled>
            <updatePolicy>always</updatePolicy>
        </snapshots>
    </repository>
</repositories>
```
## Install jar to  repository
for example:
```shell
mvn install:install-file -Dfile=./demo-xxx-1.x.x.jar -DgroupId=com.xxx.yyy -DartifactId=demo-xxx -Dversion=1.xxx.xxx -Dpackaging=jar -DgeneratePom=true -DcreateChecksum=true
```
or
```shell
mvn install:install-file -Dfile=./demo-xxx-1.x.x.jar -DgroupId=com.xxx.yyy -DartifactId=demo-xxx -Dversion=1.xxx.xxx -Dpackaging=jar -DgeneratePom=true -DcreateChecksum=true -DlocalRepositoryPath=./github/SpiderPool-New/mvn-repository/repository -DcreateChecksum=true
```
        
## Update the mvn-repository
```shell
git push to the Github
```

## Docs
https://anjia0532.github.io/2018/10/11/git-maven-howto/
