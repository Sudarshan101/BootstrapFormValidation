#website Link 

https://www.codesolution.co.in/

<h1>Bootstrap Form validation</h1>
		<p>we have to add css and js of bootstrap in our project. you can <a href="https://getbootstrap.com/docs/3.3/" target="_blank">download</a> css and js of bootstrap from the here: <a href="https://getbootstrap.com/docs/3.3/" target="_blank">https://getbootstrap.com/docs/3.3/</a>. And for the validation we have to add validation JS below of the bootstrap JS. Click on the below link for validation JS <a href="https://getbootstrap.com/docs/3.3/" target="_blank">download</a></p>
		<h2>Required field validation</h2>
		<p>for the required any field add "required" attribute in the field</p>
		<h3>html Code</h3>
<pre>
	&#60;form data-toggle="validator" role="form">
	  &#60;div class="form-group">
		&#60;label class="control-label" for="name">Name</label>
		&#60;input type="text" class="form-control" id="name" placeholder="Enter your name" required />
		&#60;div class="help-block with-errors">&#60;/div>
	  &#60;/div>
	  &#60;button type="submit" class="btn btn-default">Submit</button>
	&#60;/form></code>
</pre>
	<p style="display:inline-block;vertical-align:middle;">For the bootstrap validation we have to add &nbsp;<pre style="display:inline-block;vertical-align:middle;">data-toggle="validator"</pre>&nbsp; and &nbsp; <pre style="display:inline-block;vertical-align:middle;">role="form"</pre> &nbsp; in the form tag. and use "form-group" class parent for field. And "form-control" class in the field. And if you want to change effect on label tag then you have to add "control-label" class in the label tag. and for the error message <pre style="display:inline-block;vertical-align:middle;">&#60;div class="help-block with-errors">&#60;/div></pre> this div end of the field, inside the parent div. You can also set information in this div if you want</p>
	<br /><br />
		<h1>formate validation </h1>
		<p>for the set formate in any field we have to add "pattern" attribute in the field according to our requirement.</p>
		<h3>html Code</h3>
<pre>
	&#60;form data-toggle="validator" role="form">
	  &#60;div class="form-group">
		&#60;label class="control-label" for="name">Name</label>
		&#60;input type="text" pattern="^[_A-z0-9]{1,}$" class="form-control" id="name" placeholder="Enter your name" required />
		&#60;div class="help-block with-errors">&#60;/div>
	  &#60;/div>
	  &#60;button type="submit" class="btn btn-default">Submit</button>
	&#60;/form></code>
</pre>
	<p style="display:inline-block;vertical-align:middle;">For the formate validation we have to add &nbsp;<pre style="display:inline-block;vertical-align:middle;">pattern="^[_A-z0-9]{1,}$"</pre>&nbsp;. If you want to set limit then you have to add minlimit or maxlimit attributes <pre style="display:inline-block;vertical-align:middle;">minlength="6"</pre> &nbsp; and &nbsp; <pre style="display:inline-block;vertical-align:middle;">maxlength="15"</pre> in the field.</p>
		<br /><br />
		<h3>Some Other patterns </h3>
			<p><b>For the Number formate</b> <pre style="display:inline-block;vertical-align:middle;">pattern="[0-9]+$"</pre></p>
			<p><b>For the email formate</b> <pre style="display:inline-block;vertical-align:middle;">pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,3}$"</pre></p>
			<p><b>For the date formate</b> <pre style="display:inline-block;vertical-align:middle;">pattern="(?:(?:0[1-9]|1[0-9]|2[0-9])-(?:0[1-9]|1[0-2])|(?:(?:30)-(?!02)(?:0[1-9]|1[0-2]))|(?:31-(?:0[13578]|1[02])))-(?:19|20)[0-9]{2}"</pre></p>
			<p><b>For the Name with only one space</b> <pre style="display:inline-block;vertical-align:middle;">pattern="([a-zA-Z]+ )+[a-zA-Z]+$|^[a-zA-Z]+$"</pre></p>
			<p><b>For the Name with only one space</b> <pre style="display:inline-block;vertical-align:middle;">pattern="([a-zA-Z]){5}([0-9]){4}([a-zA-Z]){1}"</pre></p>
			<h1>Match field validation </h1>
		<p>for the Match filed we have to add <pre style="display:inline-block;vertical-align:middle;">data-match="#MATCH_FIELD_ID"</pre> attribute in the field according to our requirement. And if you want to set error for match error you have to ad one more attribute in the field <pre style="display:inline-block;vertical-align:middle;">data-match-error="Your message for matching error"</pre></p>
		<h3>html Code</h3>
<pre>
	&#60;form data-toggle="validator" role="form">
	  &#60;div class="form-group">
		&#60;label class="control-label" for="Password">Password&#60;/label>
		&#60;input type="password" data-minlength="6" class="form-control" id="Password" placeholder="Enter your name" required />
		&#60;div class="help-block with-errors">Minimum of 6 characters&#60;/div>
	  &#60;/div>
	   &#60;div class="form-group">
	   &#60;label class="control-label" for="ConfirmPassword">Confirm Password&#60;/label>
        &#60;input type="password" class="form-control" id="ConfirmPassword" data-match="#Password" data-match-error="Whoops, Password not match" placeholder="Confirm Password" required />
        &#60;div class="help-block with-errors">&#60;/div>
      &#60;/div>
	  &#60;button type="submit" class="btn btn-default">Submit&#60;/button>
	&#60;/form>
</pre>
