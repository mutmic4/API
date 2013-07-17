<a href="/1.3/README.md">Back to the Table of Contents</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="API_APPENDICES.md">Back to Appendix List</a>
<h2>APPENDIX A</h2>
<div class="text-2"><a id="appendix-b"></a><strong>KEY TERM DEFINITIONS</strong></div>
<b>BRANDNAME –</b> The company, brand, or individual that will appear as the sender’s name for campaign.
<br/><b>CAMPAIGNID -</b> ID of the campaign to subscribe the user to (integer)
<br/><b>CAMPAIGNREF –</b> Depending on your API settings you may be required to subscribe a user first before sending them messages. If you are required to subscribe a user first then a valid Campaign Reference is required. This would be the campaign ID to which the user is subscribed.
<br/><b>CTA – </b> mobile owner will be prompted for subscribing/unsubscribing confirmation via SMS. They will be sent a SMS Opt-in request (yes/no)
<br/><b>DURATION –</b> Duration of the slide displayed in seconds (integer)
<br/><b>DATABASEID –</b> The identification code for Barcode Database(integer)
<br/><b>ENDDATE -</b> The format should be YYYY-MM-DD hh:mm:ss
<br/><b>EMAIL –</b> valid email address
<br/><b>EMAILID –</b> The identification code for email template
<br/><b>FROM –</b> A valid shortcode or longcode for the sender address (string). When sending to a list of many numbers (SendSavedContent) if the FROM value cannot be used for a certain country the system will re-write the sender address to use a valid shortcode for those numbers.
<br/><b>HISTORYID –</b> This is permanent refference number used to indentify the SMS/MMS messae sending in our History. HISTORYID is used API reports.
<br/><b>MAILINGADDRESS -</b> This is the physical address that will appear in your email footers. You are required to provide your physical address in accordance with the CAN-SPAM act of 2003. Please make sure to include your company name and country in the address.
<br/><b>MMSID -</b> The identification code of saved MMS
<br/><b>NOTIFY –</b> mobile owner will be notified via SMS about being subscribed/unsubscribed. They will be sent confirmation SMS (yes/no)
<br/><b>ORIGIN –</b> This identifies the Postback. It can be SMS_MT, MMS_MT or SUB.
<br/><b>PASSWORD -</b> Valid account password (32 hexadecimal hashed password)
<br/><b>SCHEDULEDID –</b> This is refference ID for sending campaign. It is common for every number belonging to that campaign. When campaign sending is processed system will generate postback notifications linking SCHEDULEDID with TRACKINGID and HISTORYID.
<br/><b>SEQUENCE -</b> encloses all MMS slide presentation data, encloses one or multiple SLIDEs (up to a max of 8)
<br/><b>SLIDE -</b> Represents a single slide within the MMS sequence could include IMAGE/URL/TEXT/PIC etc. (special rules for slides within save MMS special consideration section)
<br/><b>SPID –</b> The carrier ID (integer – appendix D)
<br/><b>STARTDATE –</b> The format should be YYYY-MM-DD hh:mm:ss
<br/><b>TRACKINGID –</b> On success API returns with the tracking ID to identify messages seding, on failures no tracking ID is returned. It is the internal reference number for SMS/MMS sending, it is temporary ID and where possible HISTORYID should be used. Once the message sending is processed you shall receive the postback containing both TRACKINGID and HISTORYID.
<br/><b>TRANSACTIONID –</b> The identification that will be encoded into delivered barcode(string)
<br/><b>TEXT –</b> SMS message limited to 160 characters (string)
<br/><b>TO –</b> the message recipients phone number in international format.
<br/><b>USER -</b> Valid account username
<br/><b>PASSTEMPLATEID -</b> Valid Pass Template ID (Integer)
<br/><b>PASSDATAID -</b> Valid Pass Data Row ID (Integer)
<br/><b>PASSDATA -</b> All the data that goes on the pass (Array)
<br/><b>BARCODEVALUE -</b> Barcode value or Id that will be encoded into the barcode on the pass
<br/><b>BARCODETEXT -</b> Barcode text that will be shown below the barcode image on the pass
