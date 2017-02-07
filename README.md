https://issues.apache.org/jira/browse/FELIX-5527

```
[INFO] Scanning for projects...
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Build Order:
[INFO]
[INFO] maven-bundle-plugin-bug-20170207
[INFO] mod-a
[INFO] mod-b
[INFO]
[INFO] ------------------------------------------------------------------------
[INFO] Building maven-bundle-plugin-bug-20170207 1.0.0
[INFO] ------------------------------------------------------------------------
[INFO]
[INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ maven-bundle-plugin-bug-20170207 ---
[INFO]
[INFO] ------------------------------------------------------------------------
[INFO] Building mod-a 1.0.0
[INFO] ------------------------------------------------------------------------
[INFO]
[INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ mod-a ---
[INFO] Deleting /home/someone/git/com.github/io7m/maven-bundle-plugin-bug-20170207/mod-a/target
[INFO]
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ mod-a ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] Copying 1 resource
[INFO]
[INFO] --- maven-compiler-plugin:3.5.1:compile (default-compile) @ mod-a ---
[INFO] Changes detected - recompiling the module!
[INFO] Compiling 1 source file to /home/someone/git/com.github/io7m/maven-bundle-plugin-bug-20170207/mod-a/target/classes
[INFO]
[INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ mod-a ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] skip non existing resourceDirectory /home/someone/git/com.github/io7m/maven-bundle-plugin-bug-20170207/mod-a/src/test/resources
[INFO]
[INFO] --- maven-compiler-plugin:3.5.1:testCompile (default-testCompile) @ mod-a ---
[INFO] No sources to compile
[INFO]
[INFO] --- maven-surefire-plugin:2.12.4:test (default-test) @ mod-a ---
[INFO] No tests to run.
[INFO]
[INFO] --- maven-jar-plugin:2.4:jar (default-jar) @ mod-a ---
[INFO] Building jar: /home/someone/git/com.github/io7m/maven-bundle-plugin-bug-20170207/mod-a/target/mod-a-1.0.0.jar
[INFO]
[INFO] ------------------------------------------------------------------------
[INFO] Building mod-b 1.0.0
[INFO] ------------------------------------------------------------------------
[INFO]
[INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ mod-b ---
[INFO] Deleting /home/someone/git/com.github/io7m/maven-bundle-plugin-bug-20170207/mod-b/target
[INFO]
[INFO] --- maven-resources-plugin:3.0.0:resources (default-resources) @ mod-b ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] skip non existing resourceDirectory /home/someone/git/com.github/io7m/maven-bundle-plugin-bug-20170207/mod-b/src/main/resources
[INFO]
[INFO] --- maven-compiler-plugin:3.5.1:compile (default-compile) @ mod-b ---
[INFO] Changes detected - recompiling the module!
[INFO] Compiling 1 source file to /home/someone/git/com.github/io7m/maven-bundle-plugin-bug-20170207/mod-b/target/classes
[INFO]
[INFO] --- maven-resources-plugin:3.0.0:testResources (default-testResources) @ mod-b ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] skip non existing resourceDirectory /home/someone/git/com.github/io7m/maven-bundle-plugin-bug-20170207/mod-b/src/test/resources
[INFO]
[INFO] --- maven-compiler-plugin:3.5.1:testCompile (default-testCompile) @ mod-b ---
[INFO] No sources to compile
[INFO]
[INFO] --- maven-surefire-plugin:2.19.1:test (default-test) @ mod-b ---
[INFO] No tests to run.
[INFO]
[INFO] --- maven-bundle-plugin:3.2.0:bundle (default-bundle) @ mod-b ---
[ERROR] Bundle com.io7m.bugs:mod-b:bundle:1.0.0 : Classes found in the wrong directory: {META-INF/versions/9/com/io7m/bugs/Hello.class=com.io7m.bugs.Hello}
[ERROR] Error(s) found in bundle configuration
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Summary:
[INFO]
[INFO] maven-bundle-plugin-bug-20170207 ................... SUCCESS [  0.177 s]
[INFO] mod-a .............................................. SUCCESS [  2.835 s]
[INFO] mod-b .............................................. FAILURE [  1.653 s]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 7.065 s
[INFO] Finished at: 2017-02-07T16:29:38+00:00
[INFO] Final Memory: 19M/151M
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.apache.felix:maven-bundle-plugin:3.2.0:bundle (default-bundle) on project mod-b: Error(s) found in bundle configuration -> [Help 1]
[ERROR]
[ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR]
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoExecutionException
[ERROR]
[ERROR] After correcting the problems, you can resume the build with the command
[ERROR]   mvn <goals> -rf :mod-b
```

