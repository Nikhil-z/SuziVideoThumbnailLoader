Use SuziLoader<br/>
This loader will load the thumbnails for the videos which is locally stored on your filesystem.

    String path = Environment.getExternalStorageDirectory().getAbsolutePath() + "/video.mp4";
	ImageView mThumbnail = (ImageView) findViewById(R.id.thumbnail);

	SuziLoader loader = new SuziLoader(); //Create it for once
	loader.with(MainActivity.this) //Context
		.load(path) //Video path
		.into(mThumbnail) // imageview to load the thumbnail
		.type("mini") // mini or micro
		.show(); // to show the thumbnail

To get this dependency use the following steps

Step 1. Add the JitPack repository to your build file<br/>
Add it in your root build.gradle at the end of repositories:

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}

Step 2. Add the dependency

	dependencies {
		compile 'com.github.sushinpv:SuziVideoThumbnailLoader:0.1.0'
	}
	

ADD READ EXTERNAL STORAGE Permission in manifest

    <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE"/>
