This directory contains these projects:

(1) CleanDatastore

A utility used when unit testing to wipe a Google AppEngine datastore. 
No usage documentation.

(2) GaeHttpClient

Apache HttpClient is not supported on Google AppEngine. 
This code is a more generic implementation of the 
functionality first described in the blog posts:

http://peterkenji.blogspot.com/2009/08/using-apache-httpclient-4-with-google.html
and
http://esxx.blogspot.com/2009/06/using-apaches-httpclient-on-google-app.html

It works specifically with httpClient 4.2.2 libraries and 
supports variable deadlines (timeouts), redirects, certificate
validation, and expect-continue semantics (provided Google's 
UrlFetchService supports those semantics).

(3) TomcatUtils

A wrapper to the Javax ImageIO library for resizing the images 
on Aggregate to provide thumbnail images on Tomcat deployments.
On Google AppEngine, this functionality is provided through a 
different set of APIs.

NOTE: The Javax ImageIO library is not redistributable. Included in 
the /lib directory of this project is a subset of the library that
is redistributable.

(4) OpenID4Java

This is a copy of the openid4java sources 
( http://code.google.com/p/openid4java/ )
Updated to:
* use current jars
* not have untyped-collection errors
* add piping for passing in an HttpClientFactory 
 (so that the code in GAEHttpClient can be used 
  on AppEngine).
* use common-logging vs. slf4j

This is NOT an eclipse project

(5) spring-security-patch

This is a delta off of springframework security 
( http://static.springsource.org/spring-security/site/ )
Updated to:
* use the jar produced by (4) OpenID4Java
* use 3.1.3.RELEASE springframework https://github.com/SpringSource/spring-security.git
* use current jars

This is NOT an eclipse project

(6) UsableServerDiagnosticApp

This is the GWT sample app with an additional Server Information page.
If a user has trouble running ODK Aggregate on a hosting service, 
use this application to verify that the service properly handles 
GWT applications and is Tomcat 6.

(7) gwt-google-maps-v3

The gwt-google-maps-v3-snapshot.jar is built from code formerly at:
  http://code.google.com/p/gwt-google-maps-v3/
Unfortunately, that has since been removed, and, even then, the 
uploaded jars on that site do not include both the source and the
compiled classes, so they failed during GWT compiles.

To build, do the following:
(1) compile the project -- should compile with 11 warnings
(7) Export... / Java / JAR File
(8) Choose: Export generated class files and resources
(9) Choose: Export Java source files and resources
(10) Enter JAR file (gwt-google-maps-v3-snapshot.jar) and choose to compress contents.
(11) Finish
(12) You'll get a warning that it exported with warnings (the original 11).
