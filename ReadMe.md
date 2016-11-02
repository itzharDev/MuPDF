# MuPDF

Compiled NDK project. ready to use as module in your android project

right now for `armeabi` `armeabi-v7a` `mips`

MIN API - **14**

**last compiled** - 11/2/2016

### Tech

to compile MuPDF project yourself, follow this:

* [MuPDF] - MuPDF project

### Usage
`settings.gradle:`
```gradle
include ':mupdf'
project(':mupdf').projectDir = new File('../path/to/MuPDF')
```

`build.gradle:`

```gradle
dependencies {
    compile project(':mupdf')
}
```
`AndroidManifest.xml:`

**add this to your `application` tag:**

```java
tools:replace="android:icon,android:label"
```

`Java:`
```java
Uri contentUri = FileProvider.getUriForFile(context, context.getApplicationContext().getPackageName() + ".provider", filePath);
Intent intent = new Intent(context, MuPDFActivity.class);
intent.setAction(Intent.ACTION_VIEW);
intent.setData(contentUri);
startActivity(intent);
```



LIBRARY LICENSE

MuPDF is Copyright 2006-2014 Artifex Software, Inc.

This program is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU Affero General Public License along with this program. If not, see http://www.gnu.org/licenses/.



[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [MuPDF]: <http://www.mupdf.com/docs/how-to-build-mupdf-for-android>

