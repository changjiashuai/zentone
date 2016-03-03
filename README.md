
![logo](https://github.com/nisrulz/zentone/raw/master/app/src/main/res/mipmap-xhdpi/ic_launcher.png)

#ZenTone

Generating pure tone of an specific frequency was never that easy.
ZenTone does all the heavy lifting for you.

Checkout the app using the same in [Playstore](https://play.google.com/store/apps/details?id=in.excogitation.library_zentone)

#Integration
- Zentone is available in the MavenCentral, so getting it as simple as adding it as a dependency
```gradle
compile 'com.github.nisrulz:zentone:1.0.3'
```

#Usage
+ To play a tone of certain frequency and duration
```java
ZenTone.getInstance().generate(freq, duration, volume, new ToneStoppedListener() {
      @Override
      public void onToneStopped() {
          // Do something when the tone has stopped playing
      }
  });
```
*where*

|argument|type|value in
|---|---|---|
|freq|`int`|Hz
|duration|`int`|seconds
|volume|`float`|ranging from `0.0f` to `1.0f`


+ To stop the tone
```java
ZenTone.getInstance().stop();
```

License
=======

    Copyright 2016 Nishant Srivastava

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.