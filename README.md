AS3 Parse Class
=====================

This is a static ActionScript 3.0 Class for interacting with the Parse REST API and works with AIR 3.0


Dependencies
=====================
This class requires the top level JSON Class http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/3/JSON.html 


Language Version
=====================
ActionScript 3.0


Runtime Version 
=====================
Flash Player 11, AIR 3.0


Usage
=====================

Import com.illumifi.Parse to your project. 
```actionscript
Parse.Get('Scores', {objectId: 'OEyhrxNx9z'},	function (resp) {		trace(JSON.stringify(resp));	},	function (e) {		trace(JSON.stringify(e));	}
);```