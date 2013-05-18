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

Using this class is fairly straight forward but I've included a few usage examples to help you on your way. Crack open the source and look at each static method to get a better understanding of the parameters required for usage. 

```actionscript
/**
 * Parse.Post(className:String, parameters:Object, success:Function, error:Function);
 */
Parse.Post('Scores', {gamerId: 'camdagr8', score: 1337},	function (resp) {		trace(JSON.stringify(resp));	},	function (err) {		trace(err); 	});

/**
 * Parse.Get(className:String, parameters:Object, where:Object, success:Function, error:Function);
 */
Parse.Get('Scores', {count: 1}, {gamerId: 'camdagr8'},	function (resp) {		trace(JSON.stringify(resp));	},	function (err) {		trace(err);	}
);

/**
 * Parse.User.Get(objectId:String, success:Function, error:Function);
 */
Parse.User.Get('cAKgPVSYpD',	function (resp) {		trace(JSON.stringify(resp));	},	function (err) {		trace(err);	});

/**
 * Parse.SignIn(userName:String, password:String, success:Function, error:Function);
 */
Parse.SignIn('camdagr8', 'Pwnzj004LYF',
	function (resp) {
		trace(JSON.stringify(resp));
	},
	function (err) {
		trace(err);
	}
);```