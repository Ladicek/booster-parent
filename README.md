# Parent pom.xml for booster projects

Contains the necessary dependencies and the required versions for the booster projects.


## Extending the parent

You may want to override:

* project name -  `OpenShift.io Boosters`
* project description - `Strap in; we're going to production. Now.`
* project url - `https://github.com/openshiftio`
* SCM metadata (mandatory for release)

```xml
<scm>
  <url>https://github.com/openshiftio</url>
  <connection>https://github.com/openshiftio/booster-parent.git</connection>
  <developerConnection>scm:git:git:@github.com:openshiftio/booster-parent.git</developerConnection>
  <tag>HEAD</tag>
</scm>
```

* developers section
  
## Release process
  
1. `mvn release:prepare`
2. `git checkout $TAG`
3. `mvn clean deploy -Prelease`