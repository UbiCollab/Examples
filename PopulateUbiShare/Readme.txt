This project has been built with maven. 
For using maven just run "mvn clean install" to build the APK
and "mvn android:deploy  android:run" to deply the app and run it on your device or emulator.

However, before building you must mavenize the ubicollab sdk jar. 
The jar can be built from https://github.com/UbiCollab/UbiCollabSDK 
And it also can be found on the currUbiclobVersion folder within this project.
But you have to maveninze it so it matches the following import:

		    <groupId>no.sintef.ubicollab</groupId>
		    <artifactId>sdk</artifactId>
		    <version>/version> (Ive used the same as github)

Mavenizing the jar is not so difficult, you mainly have to run the following command:
mvn install:install-file -Dfile=<path-to-file> -DgroupId=<group-id> \
    -DartifactId=<artifact-id> -Dversion=<version> -Dpackaging=<packaging>

If you do not use maven, you have to configure the project and add the jars yourself.