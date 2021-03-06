<a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="API_METHODS.md">Back to API Methods</a>
<h2>sendSavedEmail</h2>
<p><strong>Synopsis:</strong><br />
This API function sends stored email template using an <i>emailid</i> from a specified account to one <i>email</i> address. 
If 'Enforce Campaign Check' is turned ON this function will require the ID of email campaign that email address is subscribed to passed inside campaignref node.
<p><strong>Request:</strong></p>
<pre>&lt;REQUEST&gt;
  &lt;ACTION&gt;sendSavedEmail&lt;/ACTION&gt;
	&lt;API_KEY&gt;API KEY&lt;/API_KEY&gt;
	&lt;EMAILID&gt;EMAILID&lt;/EMAILID&gt;
	&lt;EMAIL&gt;EMAIL&lt;/EMAIL&gt;
	&lt;CAMPAIGNREF&gt;CAMPAIGN ID&lt;/CAMPAIGNREF&gt;
	&lt;DATA&gt;
		&lt;FIRST_NAME&gt;First Name&lt;/FIRST_NAME&gt;
		&lt;LAST_NAME&gt;Last Name&lt;/LAST_NAME&gt;
		&lt;GENDER&gt;Gender&lt;/GENDER&gt;
		...
	&lt;/DATA&gt;	
&lt;/REQUEST&gt;</pre>
<div><strong>Request Parameters:</strong></div>
<pre><strong>Mandatory:</strong> Action, API_KEY, EMAILID, Email
<strong>Optional:</strong> N/A</pre>
<strong>Response Parameters:</strong>
EMAILID, Status, Email, TrackingID, Errorcode, Errorinfo<br>
<strong>Related Errorcodes: </strong><br />
E401, E402, E403, E713, E915  
<div><strong>Request Examples</strong></div>
XML:
<pre>&lt;REQUEST&gt;
	&lt;ACTION&gt;sendSavedEmail&lt;/ACTION&gt;
	&lt;API_KEY&gt;qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ&lt;/API_KEY&gt;
	&lt;EMAIL&gt;john@email.com&lt;/EMAIL&gt;
	&lt;EMAILID&gt;1234&lt;/EMAILID&gt;
	&lt;CAMPAIGNREF&gt;5678&lt;/CAMPAIGNREF&gt;
	&lt;DATA&gt;
		&lt;FIRST_NAME&gt;John&lt;/FIRST_NAME&gt;
		&lt;LAST_NAME&gt;Smith&lt;/LAST_NAME&gt;
		&lt;AGE&gt;29&lt;/AGE&gt;
		&lt;PET&gt;Dog&lt;/PET&gt;
	&lt;/DATA&gt;	
&lt;/REQUEST&gt;</pre>
GET:
<pre>https://secure.skycore.com/API/wxml/1.3/index.php?action=sendsavedemail&api_key=qTFkykO9JTfahCOqJ0V2Wf5Cg1t8iWlZ
&email=john@email.com&emailid=1234&campaignref=5678&data_first_name=John&data_last_name=Smith&data_age=29
&data_pet=Dog</pre>
<div><strong>Response Example: Success</strong></div>
<pre>&lt;RESPONSE&gt;
    &lt;STATUS&gt;Success&lt;/STATUS&gt;
    &lt;EMAILID&gt;1234&lt;/EMAILID&gt;
    &lt;TRACKINGID&gt;EMAIL_12346&lt;/TRACKINGID&gt;
    &lt;EMAIL&gt;john@email.com&lt;/EMAIL&gt;
    &lt;CAMPAIGNREF&gt;5678&lt;/CAMPAIGNREF&gt;
&lt;/RESPONSE&gt;</pre>
<div><strong>Response Example: Failure</strong></div>
<pre>&lt;RESPONSE&gt;
	 &lt;STATUS&gt;Failure&lt;/STATUS&gt;
	 &lt;ERRORCODE&gt;E713&lt;/ERRORCODE&gt;
         &lt;EMAIL&gt;john@email.com&lt;/EMAIL&gt;
         &lt;EMAILID&gt;1234&lt;/EMAILID&gt;
         &lt;CAMPAIGNREF&gt;5678&lt;/CAMPAIGNREF&gt;
	 &lt;ERRORINFO&gt;There is billing problem on your account&lt;/ERRORINFO&gt;
&lt;/RESPONSE&gt;</pre>
