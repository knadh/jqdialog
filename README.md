# jQdialog
jqDialog is a small (3.6 KB minified) dialog plugin that provides smooth, persistent, non-intrusive alternatives for alert(), confirm() and prompt(). There is also a notify() dialog that pops up and goes away in X seconds.

Kailash Nadh, September 2011

Documentation: http://kailashnadh.name/code/jqdialog

License:	GNU Public License, http://www.fsf.org/copyleft/gpl.html

## Example
<pre>
// notify dialog
$.jqDialog.notify("This dialog will disappear in 3 seconds", 3);

// alert dialog
$.jqDialog.alert("This is a non intrusive alert", function() {	// callback function for 'OK' button
	alert("This intrusive alert says you clicked OK");
});

// prompt
$.jqDialog.prompt("Please enter your name",	// message
	'Sam',	// default value in the input
	function(data) { alert("Your name is " + data); },		// callback function for 'OK' button
	function() { alert("This intrusive alert says you clicked Cancel"); }		// callback function for 'Cancel' button
);

// confirm dialog
$.jqDialog.confirm("Are you sure want to click either of these buttons?",
	function() { alert("This intrusive alert says you clicked YES"); },		// callback function for 'YES' button
	function() { alert("This intrusive alert says you clicked NO"); }		// callback function for 'NO' button
);

// custom content
$.jqDialog.content('No dialog controls, just custom content&lt;br /&gt;&lt;input type="text" name="test" /&gt;');
</pre>