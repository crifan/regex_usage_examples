# 把xml中非法的大于号和小于号替换掉

用正则批量替换：

```bash
Callback<([\w\.]+)>
Callback&lt;$1&gt;
```

从：

```xml
  <item name="android.accounts.AccountManager android.accounts.AccountManagerFuture&lt;android.os.Bundle&gt; removeAccount(android.accounts.Account, android.app.Activity, android.accounts.AccountManagerCallback<android.os.Bundle>, android.os.Handler)">
...
  <item name="android.accounts.AccountManager android.accounts.AccountManagerFuture&lt;android.os.Bundle&gt; updateCredentials(android.accounts.Account, java.lang.String, android.os.Bundle, android.app.Activity, android.accounts.AccountManagerCallback<android.os.Bundle>, android.os.Handler)”>
...
```

替换成：

```xml
  <item name="android.accounts.AccountManager android.accounts.AccountManagerFuture&lt;android.os.Bundle&gt; removeAccount(android.accounts.Account, android.app.Activity, android.accounts.AccountManagerCallback&lt;android.os.Bundle&gt;, android.os.Handler)”>
...
  <item name="android.accounts.AccountManager android.accounts.AccountManagerFuture&lt;android.os.Bundle&gt; updateCredentials(android.accounts.Account, java.lang.String, android.os.Bundle, android.app.Activity, android.accounts.AccountManagerCallback&lt;android.os.Bundle&gt;, android.os.Handler)">
```

以及更加复杂一点的：

`Android/sdk/platform-tools/api/android/hardware/camera2/annotations.xml`

```xml
  <item name="android.hardware.camera2.CameraDevice android.hardware.camera2.CaptureRequest.Builder createCaptureRequest(int, java.util.Set<java.lang.String>) 0">
    <annotation name="androidx.annotation.IntDef">
      <val name="value" val="{android.hardware.camera2.CameraDevice.TEMPLATE_PREVIEW, android.hardware.camera2.CameraDevice.TEMPLATE_STILL_CAPTURE, android.hardware.camera2.CameraDevice.TEMPLATE_RECORD, android.hardware.camera2.CameraDevice.TEMPLATE_VIDEO_SNAPSHOT, android.hardware.camera2.CameraDevice.TEMPLATE_ZERO_SHUTTER_LAG, android.hardware.camera2.CameraDevice.TEMPLATE_MANUAL}" />
    </annotation>
  </item>
```

要把其中的：

```xml
java.util.Set<java.lang.String>
```

替换成：

```xml
java.util.Set&lt;java.lang.String&gt;
```

且，又不想

* 很傻的把前缀写成固定的：`java.util.Set`
  * 这样前缀换了，就不支持了
    * 虽然此处只有这一个例子，但是还是应该写的更加通用
* 以及后续打算放到全局去替换的
  * 所以要写成通用的

参考自己教程

[环视断言 · 应用广泛的超强搜索：正则表达式](https://book.crifan.com/books/super_search_regex/website/regex_syntax/look_around/)

```bash
(?=xxx): (positive) look ahead (assertion)=正向肯定断言
(?!xxx): negative look ahead (assertion)=正向否定断言
(?<=xxx): (positive) look behind (assertion)=反向肯定断言
(?<!xxx): negative look behind (assertion)=反向否定断言
```

然后去写成：

```bash
(?<!\s)<([\.\w]+)>
&lt;$1&gt;
```

即可：只识别中间内容，不会误判

可以把：

```xml
  <item name="android.hardware.camera2.CameraDevice android.hardware.camera2.CaptureRequest.Builder createCaptureRequest(int, java.util.Set<java.lang.String>) 0">
```

替换成：

```xml
  <item name="android.hardware.camera2.CameraDevice android.hardware.camera2.CaptureRequest.Builder createCaptureRequest(int, java.util.Set&lt;java.lang.String&gt;) 0">
```
