AS3 Parse Class
=====================

This is a static ActionScript 3.0 Class for interacting with the Parse REST API.

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
/**
 * Parse.Post(className:String, parameters:Object, success:Function, error:Function);
 */
Parse.Post('Scores', {gamerId: 'camdagr8', score: 1337},	function (resp) {		trace(JSON.stringify(resp));	},	function (err) {		trace(err); 	});

/**
 * Parse.Get(className, parameters:Object, where:Object, success:Function, error:Function);
 */
Parse.Get('Scores', {count: 1}, {gamerId: 'camdagr8'},	function (resp) {		trace(JSON.stringify(resp));	},	function (err) {		trace(err);	}
);```