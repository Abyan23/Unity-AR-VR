Teknologi yang dipakai untuk pengembangan
AR.JS untuk AR
Unity untuk VR

Dikarenakan permintaan HTTPS untuk kamera, dan keterbatasan unity WebGL tidak dapat mengakses kamera browser secara native, jadi untuk AR jadi saya menggunakan AR.JS untuk fokus ke AR saja

Kamera dijalankan otomatis mengggunakan getUserMedia() dari browser
Untuk marker yang digunakan berada didalam file StreamingAssets/Marker.jpg

Memanggil Webview pada Flutter

WebViewController()
  ..setJavaScriptMode(JavaScriptMode.unrestricted)
  ..setMediaPlaybackRequiresUserGesture(false)
  ..loadRequest(Uri.parse('https://abyan23.github.io/Unity-AR-VR/'));

  Di AndroidManifest.xml tambahkan:
  <uses-permission android:name="android.permission.CAMERA"/>

Jika ingin clone, load seluruh folder WebBuild ke assets Flutter. index.html akan otomatis memanggil file-file yang dibutuhkan di dalam folder Build
  ..setJavaScriptMode(JavaScriptMode.unrestricted)
  ..setMediaPlaybackRequiresUserGesture(false)
  ..loadFlutterAsset('WebBuild/index.html');

  
