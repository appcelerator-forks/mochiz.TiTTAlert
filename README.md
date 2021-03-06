TiTTAlert module
===========================================
Titanium Mobile iOS Module project for [TTAlertView](https://github.com/twotoasters/TTAlertView)

![screenshot 2012-12-24 at 12 46 45](https://f.cloud.github.com/assets/217503/29435/a47801e8-4d7c-11e2-8115-6a05a3eecb0c.png)

INSTALL MODULE
--------------------
1. Run `build.py` which creates your distribution
2. cd to `/Library/Application Support/Titanium`
3. copy this zip file into the folder of your Titanium SDK

REGISTER MODULE
---------------------
Register your module with your application by editing `tiapp.xml` and adding your module.
Example:

```
<modules>
	<module platform="iphone" version="0.1">com.qnyp.tittalert</module>
</modules>
```

USING MODULE IN CODE
-------------------------
For example

```
var tittalert = require('com.qnyp.tittalert');
var ttalert = tittalert.createView({
    'title': 'single button alert',
    'message': 'Message',
    'cancelButtonTitle': 'キャンセル'
});
ttalert.show();
```

USAGE
-------------------------

single button alert
```
tittalert.createView({
    'title': 'single button alert',
    'message': 'message here',
    'cancelButtonTitle': 'cancel'
});
```

two button alert
```
tittalert.createView({
    'title': 'two button alert',
    'message': 'message here',
    'cancelButtonTitle': 'cancel'
    'otherButtonTitles': ['OK']
});
```

three button alert
```
tittalert.createView({
    'title': 'three button alert',
    'message': 'message here',
    'cancelButtonTitle': 'cancel'
    'otherButtonTitles': ['ONE', 'TWO']
});
```

click event
```
ttalert = tittalert.createView({
    'title': 'two button alert',
    'message': 'message here',
    'cancelButtonTitle': 'cancel'
    'otherButtonTitle': 'OK'
});
ttalert.addEventListener('click', function(e){
    if(e.cancel) {
        // canceled
    }
    if(e.index == 1) {
        // ok
    }
});
```

IMAGES
-------------------------
You can change backgroundImage.
Images are in `assets` directory.


ABOUT EXAMPLE APP
-------------------------
Example app is in `example` directory.

LICENSE
-------------------------
MIT License
