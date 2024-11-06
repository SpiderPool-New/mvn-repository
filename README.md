# mvn-repository
Myself maven repository

## Usage

`pom.xml`:
```xml
<repositories>
     <repository>
        <id>spiderpool-mvn-repository</id>
        <name>spiderpool-mvn-repository</name>
        <url>https://raw.githubusercontent.com/SpiderPool-New/mvn-repository/master/repository</url>
    </repository>
</repositories>
```
或
```xml
<repositories>
    <repository>
        <id>spiderpool-mvn-repository</id>
        <name>spiderpool-mvn-repository</name>
        <url>https://raw.github.com/SpiderPool-New/mvn-repository/master/repository</url>
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
