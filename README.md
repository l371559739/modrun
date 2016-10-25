# ModRun
ModRun is a Java classloader which can load and run classes directly from 
Maven repositories and resolve dependencies at runtime. 

ModRun is short for Module Runner. In Maven context a "module" is the same as an artifact in
a specific version.


When running an application with ModRun you just point to the Maven repository containing the
artifact you want to run, then tell ModRun what artifact id, version and main class to run.

ModRun will resolve dependencies at runtime - loading other modules (artifacts) in the correct
versions directly from the Maven repository.

ModRun can even load multiple versions of the same artifact into the same JVM. If an application
depends on module A and module B, and A and B both depend on module C - but in different versions,
ModRun can load one version of C for module A, and another version of C for module B.

ModRun is still in early development, but the early proof-of-concept is working.

