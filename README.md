#liferay-scala-portlet

Derived from Miguel Pastor setup:
http://www.liferay.com/web/miguel.pastor/blog/-/blogs/13173412

This is not the full Liferay plugins SDK, only the necessary parts to develop Scala portlets.
There are additions to the plugins build-common.xml file, the portlets build.xml file and some
additional properties to be added to the build.properties.  The Liferay plugins SDK can be downloaded
from http://www.liferay.com/downloads.

**Note:** This is for the Liferay 6.0 development branch.

## Instructions

1. Drop these 3 files in the `$PLUGINS_SDK` directory:

```
$PLUGINS_SDK/build-common.xml
$PLUGINS_SDK/portlets/build.xml
$PLUGINS_SDK/build.properties
```

2. Add portlet_scala_tmpl to the `$PLUGINS_SDK/tools` directory

```
$PLUGINS_SDK/tools/portlet_scala_tmpl/build.xml
$PLUGINS_SDK/tools/portlet_scala_tmpl/docroot/css/main.css
$PLUGINS_SDK/tools/portlet_scala_tmpl/docroot/js/main.js
$PLUGINS_SDK/tools/portlet_scala_tmpl/docroot/jsp/view.jsp
$PLUGINS_SDK/tools/portlet_scala_tmpl/docroot/WEB-INF/lib/
$PLUGINS_SDK/tools/portlet_scala_tmpl/docroot/WEB-INF/liferay-display.xml
$PLUGINS_SDK/tools/portlet_scala_tmpl/docroot/WEB-INF/liferay-plugin-package.properties
$PLUGINS_SDK/tools/portlet_scala_tmpl/docroot/WEB-INF/liferay-portlet.xml
$PLUGINS_SDK/tools/portlet_scala_tmpl/docroot/WEB-INF/portlet.xml
$PLUGINS_SDK/tools/portlet_scala_tmpl/docroot/WEB-INF/src/ScalaPortlet.scala
$PLUGINS_SDK/tools/portlet_scala_tmpl/docroot/WEB-INF/web.xml
```

3. Run the following command line to create a new Scala portlet:

```
$PLUGINS_SDK/portlets/create.sh <portlet-name> "<Title>" scala
```

## Updating Scala Libraries

To udpate the version of the Scala libraries, run the following command:

```
$PLUGINS_SDK/portlets/<portlet-name>-portlet/ant update-scala-libraries
```