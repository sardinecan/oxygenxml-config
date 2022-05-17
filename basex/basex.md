# BaseX config cheatsheet

## Enable cross-origin/cross-domain

To enable (cross-origin or cross-domain)[https://developer.mozilla.org/fr/docs/Web/HTTP/CORS] just add the following code at the end of the file `basex/webapp/WEB-INF/web.xml`.

```xml
<!-- allow cross-origin -->
<filter>
  <filter-name>cross-origin</filter-name>
  <filter-class>org.eclipse.jetty.servlets.CrossOriginFilter</filter-class>
</filter>
<filter-mapping>
  <filter-name>cross-origin</filter-name>
  <url-pattern>/*</url-pattern>
</filter-mapping>
```

## Increase session timeout 

If you are storing users in sessions, you can increase the session
timeout by adding the following entry in the `basex/webapp/WEB-INF/web.xml` file:
```xml
<!-- Increase timeout to 8 hours -->
<session-config>
  <session-timeout>480</session-timeout>
</session-config>
```