Android Runtime Permission Library
==================================
Easily handle runtime permissions in android.

 * Short code.
 * Can check multiple permissions at once.
 * Handle "don't ask again" condition.
 * Open source.
 * Light weight.
 * Fully customizable.

Dependency:
-----------

**Gradle (Jcenter)**
```
compile 'com.nabinbhandari.android:permissions:2.0'
```
    
    
**Maven**
```
<dependency>
  <groupId>com.nabinbhandari.android</groupId>
  <artifactId>permissions</artifactId>
  <version>2.0</version>
  <type>pom</type>
</dependency>
```    

Usage:
------

```java
Permissions.runPermissionCheck(this, rationale, new PermissionHandler() {
    @Override
    public void onGranted() {
        //do the task.
    }
}, Manifest.permission.CALL_PHONE, Manifest.permission.READ_CONTACTS); //as many as you need.
```

```java
@Override
public void onRequestPermissionsResult(int requestCode, @NonNull String[] permissions,
                                       @NonNull int[] grantResults) {
    Permissions.onRequestPermissionsResult(this, permissions, grantResults);
}
```

 * You can also override other methods like onDenied, onSetNotToAskAgain, etc if you want to change the default behaviour.
 * Dialog messages and texts can be modified by changing the values of public variables in the 'Permissions' class.
 

## LICENSE

    Copyright 2017 Nabin Bhandari

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
