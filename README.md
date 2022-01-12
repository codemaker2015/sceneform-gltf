Sceneform SDK for Android
=========================

Sceneform is a 3D framework with a physically based renderer that's optimized
for mobile devices and that makes it easy for you to build augmented reality
apps without requiring OpenGL.


## Demo

<img src="demo/demo.gif" width="240" height="520" />

## Choosing the right Sceneform SDK version for your project

As of ARCore release 1.16.0, Google open-sourced the implementation of Sceneform
allowing you to extend Sceneform's features and capabilities. As part of the
1.16.0 release, support for `SFA` and `SFB` assets was removed in favor of
adding `glTF` support

You can continue to use Sceneform 1.15.0 (or earlier). There is no requirement
that you migrate to Sceneform 1.16.0.

Do not use Sceneform 1.17.0 as that release will not work correctly. (Sceneform
1.17.1 can be used, but is otherwise identical to Sceneform 1.15.0.)


<table>
  <tr>
    <th>Sceneform SDK</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Sceneform SDK<br>versions <b>1.0.0 - 1.15.0</b></td>
    <td>
      <ul>
        <li>Closed source</li>
        <li>Included in your project as an external Gradle dependency</li>
        <li>
          <code>FBX</code> and <code>OBJ</code> files can be converted to
          Sceneform's <code>SFA</code> and <code>SFB</code> Sceneform
          formats
        </li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>Sceneform SDK<br>version <b>1.16.0</b></td>
    <td>
      <ul>
        <li>Open source</li>
        <li>Built alongside an application as a Gradle module</li>
        <li>
          Supports <a href="https://www.khronos.org/gltf/">glTF</a> instead of
          <code>SFA</code> and <code>SFB</code> Sceneform formats
        </li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>Sceneform SDK<br>version <b>1.17.0</b></td>
    <td>Do not use</td>
  </tr>
  <tr>
    <td>Sceneform SDK<br>version <b>1.17.1</b></td>
    <td>Identical to version 1.15.0</td>
  </tr>
</table>


## Getting started with Sceneform 1.16.0

Use the following steps to include and build the Sceneform 1.16.0 SDK with your
app:

1. Download `sceneform-android-sdk-1.16.0.zip` from the Sceneform SDK
   [releases](https://github.com/google-ar/sceneform-android-sdk/releases/tag/v1.16.0)
   page.
2. Extract the `sceneformsrc` and `sceneformux` directories into your project's
   top-level directory. The resulting directory structure should be similar to
   the following:
```
project
+-- app
|   +-- build.gradle
|   +-- ...
+-- sceneformsrc
+-- sceneformux
+-- build.gradle
+-- settings.gradle
+-- ...
```

3. Modify your project's `settings.gradle` to include the Sceneform projects:
```
include ':app'

// Add these lines:
include ':sceneform'
project(':sceneform').projectDir=new File('sceneformsrc/sceneform')

include ':sceneformux'
project(':sceneformux').projectDir=new File('sceneformux/ux')
```

4. Finally, add a reference to the Sceneform SDK to your app's `build.gradle`:
```
dependencies {
    api project(":sceneformux")
}
```

To get started with the Sceneform SDK, check out the
[Sceneform sample](https://github.com/google-ar/sceneform-android-sdk/tree/master/samples/gltf/app).


## Archived Sceneform 1.15.0 content

Documentation for the Sceneform SDK for Android 1.15.0 is available from
https://developers.google.com/sceneform.

* [Getting started](https://developers.google.com/sceneform/develop/getting-started)
* [API reference](https://developers.google.com/sceneform/reference)
* [Samples](https://github.com/google-ar/sceneform-android-sdk/tree/v1.15.0/samples)


## Release notes

The SDK release notes are available on the
[releases](https://github.com/google-ar/sceneform-android-sdk/releases) page.
