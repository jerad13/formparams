FormParams
==========

jQuery plugin to GET or SET form fields to/from JS object.

### Basic usage
	<form id="testForm">
		<input name="name" placeholder="name" value="tom"/>
		<input name="surname" placeholder="surname" value="B"/>
		<input type="checkbox" name="optin" />Opt-In<br>
		<input type="radio" name="gender" value="m" />M <input type="radio" name="gender" value="f" />F<br>
		<input name="address[line1]" placeholder="address line 1" value=""/>
		<input name="address[line2]" placeholder="address line 2" value=""/>
		<input name="address[line3]" placeholder="address line 3" value=""/>
	</form>


    $(function(){
		// GET form fields to object
        var formObj = $('#testForm').formParams();
		
		// GET form fields to object and convert types ('123' to 123, 'true' to true)
        var formObj = $('#testForm').formParams(true);

		
		
		// SET form fields from object
		// (form fields that do not have the corresponding value in the object are left unchanged):
		$('#testForm').formParams(formObj);

		// SET form fields from object 
		// and clear form fields that don't have the corresponding value in the object
		$('#testForm').formParams(formObj, true);
	});
	

Demo page available soon (download and open index.html)
