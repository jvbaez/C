<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<HTML xmlns="http://www.w3.org/1999/xhtml"
      xmlns:og="http://ogp.me/ns#"
      xmlns:fb="http://www.facebook.com/2008/fbml"> 
<HEAD>
	<title>Untitled QnA</title>
	<meta http-equiv="Content-type" content="text/html;charset=UTF-8"/> 
	<meta name="viewport" content="width=device-width; initial-scale=1.0; maximum-scale=1.0; user-scalable=0;" />
	<meta name="apple-mobile-web-app-capable" content="no" />
	<meta name="apple-mobile-web-app-status-bar-style" content="black" /> 
	<meta property="og:type" content="website"/>
	<meta property="og:image" content=""/>
	<meta http-equiv="X-UA-Compatible" content="IE=edge" />
	<link rel="apple-touch-icon" href="http://www.qnamarkup.org/images/QnA_300.png"/> 
	<link rel="stylesheet" href="//code.jquery.com/ui/1.11.1/themes/smoothness/jquery-ui.css">
  	<script src="//code.jquery.com/jquery-1.10.2.js"></script>
  	<script src="//code.jquery.com/ui/1.11.1/jquery-ui.js"></script>
</HEAD>
<BODY BGCOLOR="#ffffff" BACKGROUND="" MARGINWIDTH="0" MARGINHEIGHT="0" onLoad="startAT('1');"><style>	
	body {
		font-family: 'Palatino Linotype', 'Book Antiqua', Palatino, serif;
	}

	#rawmarkup{
		display:none;
	}
	
	#QandA img{
		width:100%;
	}

	div.main{
		min-width:300px;
		max-width:650px;
		margin: 0 auto;
	padding:0 5px 0 5px;
		}
	div.frame{
		float:left;
		width:100%;
		margin:5px 0 5px 0;
	}
	div.full{
		float:left;
		width:100%;
	}
	.button{
		padding:8px;
		margin:8px 0 0px 0;
		width:100%;
	}
	div.question_text{
		float:left;
		font-family: Verdana, Geneva, sans-serif;
		font-size: 14px;
		line-height: 20px;
		color:#ffffff;
		min-width:30px;
		background:#be54eb;
		border-radius: 15px;
		padding:10px 15px 14px 15px;
		margin-right:45px;
	}

	div.question_text a:link, div.question_text a:hover, div.question_text a:active, div.question_text a:visited{ color:#e3fbfc; } 

	div.question_arrow{
		float:left; 
		width: 0; 
		height: 0; 
		border-left: 5px solid transparent; 
		border-right: 10px solid transparent; 
		border-top: 15px solid #be54eb;
		margin:0 20px;
	}
	div.ans_text{
		float:right;
		font-family: Verdana, Geneva, sans-serif;
		font-size: 14px;
		line-height: 20px;
		color:#0a0a0a;
		min-width:30px;
		background:#d9235f;
		border-radius: 15px;
		padding:10px 15px 14px 15px;
		margin-left:45px;
	}
	div.ans_arrow{
		float:right; 
		width: 0; 
		height: 0; 
		border-left: 10px solid transparent; 
		border-right: 5px solid transparent; 
		border-top: 15px solid #d9235f;
		margin:0 20px;
	}
	div.choices{
		float:left;
		width:100%;
		margin:15px 0 0 0;
	}
	div.credits{
		float:left;
		dispaly:none;
		width:100%;
		background:#eee;
		margin:0px 0 15px 0;
	}
	div.credit_text{
		font-family: Verdana, Geneva, sans-serif;
		font-size: 14px;
		line-height: 20px;
		padding:4px 15px 10px 15px;
	}
	li.error{
		list-style-type: none;
		background:#ffdddd;
		margin: 10px 0 0 0;
		padding: 5px;
	}

	.qpad {
		float:left;
		padding:0 15px;
	}

	a.qabutton {
		float:left;
		font-family: Verdana, Geneva, sans-serif;
		font-size: 14px;
		line-height: 20px;
		width:100%;
		background: #eee;
		border-radius: 8px;
		padding:10px 0px 12px 0;
		margin: 0 0 8px 0;
		border: solid 1px #888;
		text-align:left;
		color: #000000;
		text-decoration: none;
	}

	a.qabutton:hover, a.qabutton:active {
		float:left;
		font-family: Verdana, Geneva, sans-serif;
		font-size: 14px;
		line-height: 20px;
		width:100%;
		background: #ddd;
		border-radius: 8px;
		padding:10px 0px 12px 0;
		margin: 0 0 8px 0;
		border: solid 1px #888;
		text-align:left;
		color: #000000;
		text-decoration: underline;
	}
	

	div.xdiv {
		float:left;
		width:100%;
		margin: 0 0 8px 0;
		background: #eee;
		border: solid 1px #888;
		border-radius: 8px;
	}	

	input.xinput {
		-webkit-box-sizing: border-box; /* Safari/Chrome, other WebKit */
		-moz-box-sizing: border-box;    /* Firefox, other Gecko */ 
		box-sizing: border-box;         /* Opera/IE 8+ */
		float:left;
		width:100%;
		font-family: Verdana, Geneva, sans-serif;
		font-size: 14px;
		line-height: 20px;
		background: #fff;
		border-top-left-radius: 8px;
		border-top-right-radius: 8px;
		padding:10px 10px 12px 10px;
		border: solid 0px #888;
		border-bottom: solid 1px #888;
		text-align:left;
		color: #000000;
		text-decoration: none;
	}
	
	a.xbutton {
		float:left;
		width:100%;
		text-align:left;
		font-family: Verdana, Geneva, sans-serif;
		font-size: 14px;
		line-height: 20px;
		background: #eee;
		border-radius: 8px;
		padding:10px 0px 12px 0px;
		color: #000000;
		text-decoration: none;
	}
	
	a.xbutton:hover, a.xbutton:active {
		border-top-left-radius: 0px;
		border-top-right-radius: 0px;
		background: #ddd;
	}
</style>
<FORM name="FORM" id="FORM"><div id="conversation" style="margin:15px auto 0 auto;padding:0 15px;max-width:500px"><div id='QandA' class='QandA'><div style='padding:15px;background:#ddffdd;text-align:center;'>Loading QnA...</div></div><div id='Choices' class='choices'></div><div id='rawmarkup' style='display:none;'>Q(1): Are you interested in filing for Bankruptcy? 
A:Yes
	Q(1.1): Are you filing an individual or business?
	A: I am filing as an individual.
		Q(1.1.1): Have you received a bankruptcy discharge in the last 8 years?
		A: Yes
			Q(1.1.1.1):Have you received a discharge on a Chapter 7 case within eight years from the date that the first case was filed?
			A: You cannot receive a second discharge in any Chapter 7 chase that is filed within eight years from the date that the first case was filed. 
		A: No
			Q(1.1.1.2): Have you had a bankruptcy filing dismissed within the previous 180 days?
			A: Yes
				Q(1.1.1.2.1): Please select the reason for the dismissal.
				A:I violated a court order.	
					Q(1.1.1.2.1.1): You are ineligible to file Chapter 7 bankruptcy.	
				A:The court ruled that my filing was fraudulent or constituted an abuse of the bankruptcy system.
					Q(1.1.1.2.1.2): You are ineligible to file Chapter 7 bankruptcy.
				A:I requested a dismissal after a creditor asked for relief.
					Q(1.1.1.2.1.3): You are ineligible to file Chapter 7 bankruptcy. 
				A:I meet the criteria of more than one of the above mentioned.
					Q(1.1.1.2.1.4):You are ineligible to file Chapter 7 bankruptcy. 
			A: No 
				Q(1.1.1.2.2): Is your current monthly income less than or equal to the median income for a family your size in your state? 
				A: Yes
					Q(1.1.1.2.2.1): You may file for Chapter 7 bankruptcy. 
				A: No
					Q(1.1.1.2.2.2): Do you believe that you are eligible under the Chapter 7 Bankruptcy Means Test?
					A: Yes. 
						Q(1.1.1.2.2.2.1): To confirm that you qualify under the means test please head over to &lt;a href="http://www.uscourts.gov/forms/means-test-forms/chapter-7-means-test-calculation"&gt;http://www.uscourts.gov/forms/means-test-forms/chapter-7-means-test-calculation&lt;/a&gt;.
					A: No.
						Q(1.1.1.2.2.2.2):GOTO:1.1.1.2.1.4
						A: If you do not pass the means test or believe you are not eligible, you may able to file under Chapter 13 bankruptcy.LINK FOR

					A: What is the means test?
						Q(1.1.1.2.2.2.3): The bankruptcy "means test" determines whether your income is low enough for you to file Chapter 7 bankruptcy. It's a formula designed to keep filers with higher incomes from filing for Chapter 7 bankruptcy. High income filers who fail the means test may use Chapter 13 bankruptcy to repay a portion of their debts, but may not use Chapter 7 bankruptcy to wipe out their debts altogether. GOTO:1.1.1.2.2.2
				A: I am unsure what this mean.
					Q(1.1.1.2.2.3): Your "current monthly income" is your average income over the last six months before you file. If your income is less than or equal to the median, the law presumes that you are eligible for Chapter 7 bankruptcy. GOTO:1.1.1.2.2  
												
	A: I am filing as a business.
		Q(1.1.2): This service is designed for individuals looking to file for bankruptcy. If you would like more information about filing for bankruptcy as a business, sole proprietorship, or corporation. For more information please visit &lt;a hreft="http://www.uscourts.gov/services-forms/bankruptcy"&gt;http://www.uscourts.gov/services-forms/bankruptcy&lt;/a&gt;.
	
A: No
	Q(1.2): Thank you. Have a nice day. 
		




</div><div id="ondeck" name="ondeck"><div id="doc" name="doc" style="display:none;"></div><div id='Q-1' name='Q-1' style='display:none;'> Are you interested in filing for Bankruptcy? 
</div><div id='Q-1.1' name='Q-1.1' style='display:none;'> Are you filing an individual or business?
</div><div id='Q-1.1.1' name='Q-1.1.1' style='display:none;'> Have you received a bankruptcy discharge in the last 8 years?
</div><div id='Q-1.1.1.1' name='Q-1.1.1.1' style='display:none;'>Have you received a discharge on a Chapter 7 case within eight years from the date that the first case was filed?
</div><div id='Q-1.1.1.2' name='Q-1.1.1.2' style='display:none;'> Have you had a bankruptcy filing dismissed within the previous 180 days?
</div><div id='Q-1.1.1.2.1' name='Q-1.1.1.2.1' style='display:none;'> Please select the reason for the dismissal.
</div><div id='Q-1.1.1.2.1.1' name='Q-1.1.1.2.1.1' style='display:none;'> You are ineligible to file Chapter 7 bankruptcy.	
</div><div id='Q-1.1.1.2.1.2' name='Q-1.1.1.2.1.2' style='display:none;'> You are ineligible to file Chapter 7 bankruptcy.
</div><div id='Q-1.1.1.2.1.3' name='Q-1.1.1.2.1.3' style='display:none;'> You are ineligible to file Chapter 7 bankruptcy. 
</div><div id='Q-1.1.1.2.1.4' name='Q-1.1.1.2.1.4' style='display:none;'>You are ineligible to file Chapter 7 bankruptcy. 
</div><div id='Q-1.1.1.2.2' name='Q-1.1.1.2.2' style='display:none;'> Is your current monthly income less than or equal to the median income for a family your size in your state? 
</div><div id='Q-1.1.1.2.2.1' name='Q-1.1.1.2.2.1' style='display:none;'> You may file for Chapter 7 bankruptcy. 
</div><div id='Q-1.1.1.2.2.2' name='Q-1.1.1.2.2.2' style='display:none;'> Do you believe that you are eligible under the Chapter 7 Bankruptcy Means Test?
</div><div id='Q-1.1.1.2.2.2.1' name='Q-1.1.1.2.2.2.1' style='display:none;'> To confirm that you qualify under the means test please head over to <a href="http://www.uscourts.gov/forms/means-test-forms/chapter-7-means-test-calculation">http://www.uscourts.gov/forms/means-test-forms/chapter-7-means-test-calculation</a>.
</div><div id='Q-1.1.1.2.2.2.2' name='Q-1.1.1.2.2.2.2' style='display:none;'>GOTO:1.1.1.2.1.4
</div><div id='Q-1.1.1.2.2.2.3' name='Q-1.1.1.2.2.2.3' style='display:none;'> The bankruptcy "means test" determines whether your income is low enough for you to file Chapter 7 bankruptcy. It's a formula designed to keep filers with higher incomes from filing for Chapter 7 bankruptcy. High income filers who fail the means test may use Chapter 13 bankruptcy to repay a portion of their debts, but may not use Chapter 7 bankruptcy to wipe out their debts altogether. GOTO:1.1.1.2.2.2
</div><div id='Q-1.1.1.2.2.3' name='Q-1.1.1.2.2.3' style='display:none;'> Your "current monthly income" is your average income over the last six months before you file. If your income is less than or equal to the median, the law presumes that you are eligible for Chapter 7 bankruptcy. GOTO:1.1.1.2.2  
												
</div><div id='Q-1.1.2' name='Q-1.1.2' style='display:none;'> This service is designed for individuals looking to file for bankruptcy. If you would like more information about filing for bankruptcy as a business, sole proprietorship, or corporation. For more information please visit <a hreft="http://www.uscourts.gov/services-forms/bankruptcy">http://www.uscourts.gov/services-forms/bankruptcy</a>.
	
</div><div id='Q-1.2' name='Q-1.2' style='display:none;'> Thank you. Have a nice day. 
		




</div><div id='A-1.1' name='A-1.1' style='display:none;'>Yes
</div><div id='A-href-1.1' name='A-href-1.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1' name='A-target-1.1' style='display:none;'></div><div id='X-1.1' name='X-1.1' style='display:none;'></div><div id='A-1.1.1' name='A-1.1.1' style='display:none;'> I am filing as an individual.
</div><div id='A-href-1.1.1' name='A-href-1.1.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1' name='A-target-1.1.1' style='display:none;'></div><div id='X-1.1.1' name='X-1.1.1' style='display:none;'></div><div id='A-1.1.1.1' name='A-1.1.1.1' style='display:none;'> Yes
</div><div id='A-href-1.1.1.1' name='A-href-1.1.1.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.1' name='A-target-1.1.1.1' style='display:none;'></div><div id='X-1.1.1.1' name='X-1.1.1.1' style='display:none;'></div><div id='A-1.1.1.1.1' name='A-1.1.1.1.1' style='display:none;'> You cannot receive a second discharge in any Chapter 7 chase that is filed within eight years from the date that the first case was filed. 
</div><div id='A-href-1.1.1.1.1' name='A-href-1.1.1.1.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.1.1' name='A-target-1.1.1.1.1' style='display:none;'></div><div id='X-1.1.1.1.1' name='X-1.1.1.1.1' style='display:none;'></div><div id='A-1.1.1.2' name='A-1.1.1.2' style='display:none;'> No
</div><div id='A-href-1.1.1.2' name='A-href-1.1.1.2' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2' name='A-target-1.1.1.2' style='display:none;'></div><div id='X-1.1.1.2' name='X-1.1.1.2' style='display:none;'></div><div id='A-1.1.1.2.1' name='A-1.1.1.2.1' style='display:none;'> Yes
</div><div id='A-href-1.1.1.2.1' name='A-href-1.1.1.2.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.1' name='A-target-1.1.1.2.1' style='display:none;'></div><div id='X-1.1.1.2.1' name='X-1.1.1.2.1' style='display:none;'></div><div id='A-1.1.1.2.1.1' name='A-1.1.1.2.1.1' style='display:none;'>I violated a court order.	
</div><div id='A-href-1.1.1.2.1.1' name='A-href-1.1.1.2.1.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.1.1' name='A-target-1.1.1.2.1.1' style='display:none;'></div><div id='X-1.1.1.2.1.1' name='X-1.1.1.2.1.1' style='display:none;'></div><div id='A-1.1.1.2.1.2' name='A-1.1.1.2.1.2' style='display:none;'>The court ruled that my filing was fraudulent or constituted an abuse of the bankruptcy system.
</div><div id='A-href-1.1.1.2.1.2' name='A-href-1.1.1.2.1.2' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.1.2' name='A-target-1.1.1.2.1.2' style='display:none;'></div><div id='X-1.1.1.2.1.2' name='X-1.1.1.2.1.2' style='display:none;'></div><div id='A-1.1.1.2.1.3' name='A-1.1.1.2.1.3' style='display:none;'>I requested a dismissal after a creditor asked for relief.
</div><div id='A-href-1.1.1.2.1.3' name='A-href-1.1.1.2.1.3' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.1.3' name='A-target-1.1.1.2.1.3' style='display:none;'></div><div id='X-1.1.1.2.1.3' name='X-1.1.1.2.1.3' style='display:none;'></div><div id='A-1.1.1.2.1.4' name='A-1.1.1.2.1.4' style='display:none;'>I meet the criteria of more than one of the above mentioned.
</div><div id='A-href-1.1.1.2.1.4' name='A-href-1.1.1.2.1.4' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.1.4' name='A-target-1.1.1.2.1.4' style='display:none;'></div><div id='X-1.1.1.2.1.4' name='X-1.1.1.2.1.4' style='display:none;'></div><div id='A-1.1.1.2.2' name='A-1.1.1.2.2' style='display:none;'> No 
</div><div id='A-href-1.1.1.2.2' name='A-href-1.1.1.2.2' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.2' name='A-target-1.1.1.2.2' style='display:none;'></div><div id='X-1.1.1.2.2' name='X-1.1.1.2.2' style='display:none;'></div><div id='A-1.1.1.2.2.1' name='A-1.1.1.2.2.1' style='display:none;'> Yes
</div><div id='A-href-1.1.1.2.2.1' name='A-href-1.1.1.2.2.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.2.1' name='A-target-1.1.1.2.2.1' style='display:none;'></div><div id='X-1.1.1.2.2.1' name='X-1.1.1.2.2.1' style='display:none;'></div><div id='A-1.1.1.2.2.2' name='A-1.1.1.2.2.2' style='display:none;'> No
</div><div id='A-href-1.1.1.2.2.2' name='A-href-1.1.1.2.2.2' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.2.2' name='A-target-1.1.1.2.2.2' style='display:none;'></div><div id='X-1.1.1.2.2.2' name='X-1.1.1.2.2.2' style='display:none;'></div><div id='A-1.1.1.2.2.2.1' name='A-1.1.1.2.2.2.1' style='display:none;'> Yes. 
</div><div id='A-href-1.1.1.2.2.2.1' name='A-href-1.1.1.2.2.2.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.2.2.1' name='A-target-1.1.1.2.2.2.1' style='display:none;'></div><div id='X-1.1.1.2.2.2.1' name='X-1.1.1.2.2.2.1' style='display:none;'></div><div id='A-1.1.1.2.2.2.2' name='A-1.1.1.2.2.2.2' style='display:none;'> No.
</div><div id='A-href-1.1.1.2.2.2.2' name='A-href-1.1.1.2.2.2.2' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.2.2.2' name='A-target-1.1.1.2.2.2.2' style='display:none;'></div><div id='X-1.1.1.2.2.2.2' name='X-1.1.1.2.2.2.2' style='display:none;'></div><div id='A-1.1.1.2.2.2.2.1' name='A-1.1.1.2.2.2.2.1' style='display:none;'> If you do not pass the means test or believe you are not eligible, you may able to file under Chapter 13 bankruptcy.LINK FOR

</div><div id='A-href-1.1.1.2.2.2.2.1' name='A-href-1.1.1.2.2.2.2.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.2.2.2.1' name='A-target-1.1.1.2.2.2.2.1' style='display:none;'></div><div id='X-1.1.1.2.2.2.2.1' name='X-1.1.1.2.2.2.2.1' style='display:none;'></div><div id='A-1.1.1.2.2.2.3' name='A-1.1.1.2.2.2.3' style='display:none;'> What is the means test?
</div><div id='A-href-1.1.1.2.2.2.3' name='A-href-1.1.1.2.2.2.3' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.2.2.3' name='A-target-1.1.1.2.2.2.3' style='display:none;'></div><div id='X-1.1.1.2.2.2.3' name='X-1.1.1.2.2.2.3' style='display:none;'></div><div id='A-1.1.1.2.2.3' name='A-1.1.1.2.2.3' style='display:none;'> I am unsure what this mean.
</div><div id='A-href-1.1.1.2.2.3' name='A-href-1.1.1.2.2.3' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.2.3' name='A-target-1.1.1.2.2.3' style='display:none;'></div><div id='X-1.1.1.2.2.3' name='X-1.1.1.2.2.3' style='display:none;'></div><div id='A-1.1.2' name='A-1.1.2' style='display:none;'> I am filing as a business.
</div><div id='A-href-1.1.2' name='A-href-1.1.2' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.2' name='A-target-1.1.2' style='display:none;'></div><div id='X-1.1.2' name='X-1.1.2' style='display:none;'></div><div id='A-1.2' name='A-1.2' style='display:none;'> No
</div><div id='A-href-1.2' name='A-href-1.2' style='display:none;'>javascript:void('');</div><div id='A-target-1.2' name='A-target-1.2' style='display:none;'></div><div id='X-1.2' name='X-1.2' style='display:none;'></div></div><textarea id="original" name="original" style="display:none;" disabled="disabled"><div id="doc" name="doc" style="display:none;"></div><div id='Q-1' name='Q-1' style='display:none;'> Are you interested in filing for Bankruptcy? 
</div><div id='Q-1.1' name='Q-1.1' style='display:none;'> Are you filing an individual or business?
</div><div id='Q-1.1.1' name='Q-1.1.1' style='display:none;'> Have you received a bankruptcy discharge in the last 8 years?
</div><div id='Q-1.1.1.1' name='Q-1.1.1.1' style='display:none;'>Have you received a discharge on a Chapter 7 case within eight years from the date that the first case was filed?
</div><div id='Q-1.1.1.2' name='Q-1.1.1.2' style='display:none;'> Have you had a bankruptcy filing dismissed within the previous 180 days?
</div><div id='Q-1.1.1.2.1' name='Q-1.1.1.2.1' style='display:none;'> Please select the reason for the dismissal.
</div><div id='Q-1.1.1.2.1.1' name='Q-1.1.1.2.1.1' style='display:none;'> You are ineligible to file Chapter 7 bankruptcy.	
</div><div id='Q-1.1.1.2.1.2' name='Q-1.1.1.2.1.2' style='display:none;'> You are ineligible to file Chapter 7 bankruptcy.
</div><div id='Q-1.1.1.2.1.3' name='Q-1.1.1.2.1.3' style='display:none;'> You are ineligible to file Chapter 7 bankruptcy. 
</div><div id='Q-1.1.1.2.1.4' name='Q-1.1.1.2.1.4' style='display:none;'>You are ineligible to file Chapter 7 bankruptcy. 
</div><div id='Q-1.1.1.2.2' name='Q-1.1.1.2.2' style='display:none;'> Is your current monthly income less than or equal to the median income for a family your size in your state? 
</div><div id='Q-1.1.1.2.2.1' name='Q-1.1.1.2.2.1' style='display:none;'> You may file for Chapter 7 bankruptcy. 
</div><div id='Q-1.1.1.2.2.2' name='Q-1.1.1.2.2.2' style='display:none;'> Do you believe that you are eligible under the Chapter 7 Bankruptcy Means Test?
</div><div id='Q-1.1.1.2.2.2.1' name='Q-1.1.1.2.2.2.1' style='display:none;'> To confirm that you qualify under the means test please head over to <a href="http://www.uscourts.gov/forms/means-test-forms/chapter-7-means-test-calculation">http://www.uscourts.gov/forms/means-test-forms/chapter-7-means-test-calculation</a>.
</div><div id='Q-1.1.1.2.2.2.2' name='Q-1.1.1.2.2.2.2' style='display:none;'>GOTO:1.1.1.2.1.4
</div><div id='Q-1.1.1.2.2.2.3' name='Q-1.1.1.2.2.2.3' style='display:none;'> The bankruptcy "means test" determines whether your income is low enough for you to file Chapter 7 bankruptcy. It's a formula designed to keep filers with higher incomes from filing for Chapter 7 bankruptcy. High income filers who fail the means test may use Chapter 13 bankruptcy to repay a portion of their debts, but may not use Chapter 7 bankruptcy to wipe out their debts altogether. GOTO:1.1.1.2.2.2
</div><div id='Q-1.1.1.2.2.3' name='Q-1.1.1.2.2.3' style='display:none;'> Your "current monthly income" is your average income over the last six months before you file. If your income is less than or equal to the median, the law presumes that you are eligible for Chapter 7 bankruptcy. GOTO:1.1.1.2.2  
												
</div><div id='Q-1.1.2' name='Q-1.1.2' style='display:none;'> This service is designed for individuals looking to file for bankruptcy. If you would like more information about filing for bankruptcy as a business, sole proprietorship, or corporation. For more information please visit <a hreft="http://www.uscourts.gov/services-forms/bankruptcy">http://www.uscourts.gov/services-forms/bankruptcy</a>.
	
</div><div id='Q-1.2' name='Q-1.2' style='display:none;'> Thank you. Have a nice day. 
		




</div><div id='A-1.1' name='A-1.1' style='display:none;'>Yes
</div><div id='A-href-1.1' name='A-href-1.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1' name='A-target-1.1' style='display:none;'></div><div id='X-1.1' name='X-1.1' style='display:none;'></div><div id='A-1.1.1' name='A-1.1.1' style='display:none;'> I am filing as an individual.
</div><div id='A-href-1.1.1' name='A-href-1.1.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1' name='A-target-1.1.1' style='display:none;'></div><div id='X-1.1.1' name='X-1.1.1' style='display:none;'></div><div id='A-1.1.1.1' name='A-1.1.1.1' style='display:none;'> Yes
</div><div id='A-href-1.1.1.1' name='A-href-1.1.1.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.1' name='A-target-1.1.1.1' style='display:none;'></div><div id='X-1.1.1.1' name='X-1.1.1.1' style='display:none;'></div><div id='A-1.1.1.1.1' name='A-1.1.1.1.1' style='display:none;'> You cannot receive a second discharge in any Chapter 7 chase that is filed within eight years from the date that the first case was filed. 
</div><div id='A-href-1.1.1.1.1' name='A-href-1.1.1.1.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.1.1' name='A-target-1.1.1.1.1' style='display:none;'></div><div id='X-1.1.1.1.1' name='X-1.1.1.1.1' style='display:none;'></div><div id='A-1.1.1.2' name='A-1.1.1.2' style='display:none;'> No
</div><div id='A-href-1.1.1.2' name='A-href-1.1.1.2' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2' name='A-target-1.1.1.2' style='display:none;'></div><div id='X-1.1.1.2' name='X-1.1.1.2' style='display:none;'></div><div id='A-1.1.1.2.1' name='A-1.1.1.2.1' style='display:none;'> Yes
</div><div id='A-href-1.1.1.2.1' name='A-href-1.1.1.2.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.1' name='A-target-1.1.1.2.1' style='display:none;'></div><div id='X-1.1.1.2.1' name='X-1.1.1.2.1' style='display:none;'></div><div id='A-1.1.1.2.1.1' name='A-1.1.1.2.1.1' style='display:none;'>I violated a court order.	
</div><div id='A-href-1.1.1.2.1.1' name='A-href-1.1.1.2.1.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.1.1' name='A-target-1.1.1.2.1.1' style='display:none;'></div><div id='X-1.1.1.2.1.1' name='X-1.1.1.2.1.1' style='display:none;'></div><div id='A-1.1.1.2.1.2' name='A-1.1.1.2.1.2' style='display:none;'>The court ruled that my filing was fraudulent or constituted an abuse of the bankruptcy system.
</div><div id='A-href-1.1.1.2.1.2' name='A-href-1.1.1.2.1.2' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.1.2' name='A-target-1.1.1.2.1.2' style='display:none;'></div><div id='X-1.1.1.2.1.2' name='X-1.1.1.2.1.2' style='display:none;'></div><div id='A-1.1.1.2.1.3' name='A-1.1.1.2.1.3' style='display:none;'>I requested a dismissal after a creditor asked for relief.
</div><div id='A-href-1.1.1.2.1.3' name='A-href-1.1.1.2.1.3' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.1.3' name='A-target-1.1.1.2.1.3' style='display:none;'></div><div id='X-1.1.1.2.1.3' name='X-1.1.1.2.1.3' style='display:none;'></div><div id='A-1.1.1.2.1.4' name='A-1.1.1.2.1.4' style='display:none;'>I meet the criteria of more than one of the above mentioned.
</div><div id='A-href-1.1.1.2.1.4' name='A-href-1.1.1.2.1.4' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.1.4' name='A-target-1.1.1.2.1.4' style='display:none;'></div><div id='X-1.1.1.2.1.4' name='X-1.1.1.2.1.4' style='display:none;'></div><div id='A-1.1.1.2.2' name='A-1.1.1.2.2' style='display:none;'> No 
</div><div id='A-href-1.1.1.2.2' name='A-href-1.1.1.2.2' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.2' name='A-target-1.1.1.2.2' style='display:none;'></div><div id='X-1.1.1.2.2' name='X-1.1.1.2.2' style='display:none;'></div><div id='A-1.1.1.2.2.1' name='A-1.1.1.2.2.1' style='display:none;'> Yes
</div><div id='A-href-1.1.1.2.2.1' name='A-href-1.1.1.2.2.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.2.1' name='A-target-1.1.1.2.2.1' style='display:none;'></div><div id='X-1.1.1.2.2.1' name='X-1.1.1.2.2.1' style='display:none;'></div><div id='A-1.1.1.2.2.2' name='A-1.1.1.2.2.2' style='display:none;'> No
</div><div id='A-href-1.1.1.2.2.2' name='A-href-1.1.1.2.2.2' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.2.2' name='A-target-1.1.1.2.2.2' style='display:none;'></div><div id='X-1.1.1.2.2.2' name='X-1.1.1.2.2.2' style='display:none;'></div><div id='A-1.1.1.2.2.2.1' name='A-1.1.1.2.2.2.1' style='display:none;'> Yes. 
</div><div id='A-href-1.1.1.2.2.2.1' name='A-href-1.1.1.2.2.2.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.2.2.1' name='A-target-1.1.1.2.2.2.1' style='display:none;'></div><div id='X-1.1.1.2.2.2.1' name='X-1.1.1.2.2.2.1' style='display:none;'></div><div id='A-1.1.1.2.2.2.2' name='A-1.1.1.2.2.2.2' style='display:none;'> No.
</div><div id='A-href-1.1.1.2.2.2.2' name='A-href-1.1.1.2.2.2.2' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.2.2.2' name='A-target-1.1.1.2.2.2.2' style='display:none;'></div><div id='X-1.1.1.2.2.2.2' name='X-1.1.1.2.2.2.2' style='display:none;'></div><div id='A-1.1.1.2.2.2.2.1' name='A-1.1.1.2.2.2.2.1' style='display:none;'> If you do not pass the means test or believe you are not eligible, you may able to file under Chapter 13 bankruptcy.LINK FOR

</div><div id='A-href-1.1.1.2.2.2.2.1' name='A-href-1.1.1.2.2.2.2.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.2.2.2.1' name='A-target-1.1.1.2.2.2.2.1' style='display:none;'></div><div id='X-1.1.1.2.2.2.2.1' name='X-1.1.1.2.2.2.2.1' style='display:none;'></div><div id='A-1.1.1.2.2.2.3' name='A-1.1.1.2.2.2.3' style='display:none;'> What is the means test?
</div><div id='A-href-1.1.1.2.2.2.3' name='A-href-1.1.1.2.2.2.3' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.2.2.3' name='A-target-1.1.1.2.2.2.3' style='display:none;'></div><div id='X-1.1.1.2.2.2.3' name='X-1.1.1.2.2.2.3' style='display:none;'></div><div id='A-1.1.1.2.2.3' name='A-1.1.1.2.2.3' style='display:none;'> I am unsure what this mean.
</div><div id='A-href-1.1.1.2.2.3' name='A-href-1.1.1.2.2.3' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.1.2.2.3' name='A-target-1.1.1.2.2.3' style='display:none;'></div><div id='X-1.1.1.2.2.3' name='X-1.1.1.2.2.3' style='display:none;'></div><div id='A-1.1.2' name='A-1.1.2' style='display:none;'> I am filing as a business.
</div><div id='A-href-1.1.2' name='A-href-1.1.2' style='display:none;'>javascript:void('');</div><div id='A-target-1.1.2' name='A-target-1.1.2' style='display:none;'></div><div id='X-1.1.2' name='X-1.1.2' style='display:none;'></div><div id='A-1.2' name='A-1.2' style='display:none;'> No
</div><div id='A-href-1.2' name='A-href-1.2' style='display:none;'>javascript:void('');</div><div id='A-target-1.2' name='A-target-1.2' style='display:none;'></div><div id='X-1.2' name='X-1.2' style='display:none;'></div></textarea><textarea id="transcript" name="transcript" style="display:none;" disabled="disabled"></textarea><div style="float:left;width:100%;margin:15px 0 0px 0;border-top: solid 1px #ddd;"><div id=credits class=credits style="display:none;"><div class=credit_text></div></div><p align=center> <a href="http://www.qnamarkup.org/" target=_top>code your own</a></p></div></FORM></div></div>
<script type="text/javascript">
	var QNum = 0;
	var Qhtml = "";
	var Dhtml = "";
	var label = "";
	var GOTOfired = 0;

	$("#conversation input").on("keypress", 'form', function (e) {
    	var code = e.keyCode || e.which;
    	if (code == 13) {
        	e.preventDefault();
        	return false;
    	}
	});

	function answerQ(lb,restart) {
		label = lb;
		Dhtml = 'D-'+label;
		Qhtml = 'Q-'+label;
		var Ahtml = 'A-'+label;
		var Jhtml = 'J-'+QNum;
		var Xhtml = 'X-'+label;
		var Xihtml = 'Xi-'+label;
		
		var input_error = 0;
		if (restart == undefined) {
			var regexp = new RegExp("\<variable\>");
			if (document.getElementById(Ahtml).innerHTML.match(regexp)) {
				document.getElementById(Xihtml).value = document.getElementById(Xihtml).value.replace(/(^\s*|\s*$)/,"");
				if (document.getElementById(Xihtml).value == "") {
					input_error = "Your answer appears to be empty.";
				} else {
					document.getElementById(Xihtml).value = document.getElementById(Xihtml).value.replace(/</g,"&lt;");
					document.getElementById(Xihtml).value = document.getElementById(Xihtml).value.replace(/>/g,"&gt;");
				}
			} 
		}
			
		if (input_error != 0) {
			alert(input_error);
			document.getElementById(Xihtml).focus();			
		} else {
			if (restart == undefined) {
				document.getElementById('QandA').innerHTML += "<div class='frame'><div class='full'><div class='ans_text'>"+document.getElementById(Ahtml).innerHTML+"</div></div><div class='ans_arrow'></div></div></div></div>";
				// insert answer from button
				if(document.getElementById(Ahtml).innerHTML != "") { document.getElementById('transcript').value += "USER: "+document.getElementById(Ahtml).innerHTML; }
				if (document.getElementById('QandA').innerHTML.match(regexp)) {
				 	var duplicatevars = new RegExp("id=\""+document.getElementById(Xhtml).innerHTML+"(.)*"+document.getElementById(Xhtml).innerHTML+"\"","g");
					document.getElementById('QandA').innerHTML = document.getElementById('QandA').innerHTML.replace(duplicatevars, "");
					document.getElementById('QandA').innerHTML = document.getElementById('QandA').innerHTML.replace(/\<variable\>(\<\/variable\>)?/, "<input type=hidden id=\""+document.getElementById(Xhtml).innerHTML+"\" name=\""+document.getElementById(Xhtml).innerHTML+"\" value=\""+document.getElementById(Xihtml).value+"\"/>"+document.getElementById(Xihtml).value);
					document.getElementById('transcript').value = document.getElementById('transcript').value.replace(/\<variable\>(\<\/variable\>)?/, document.getElementById(Xihtml).value+"\n");
					var thisvariable = new RegExp("<(X|x)>"+document.getElementById(Xhtml).innerHTML+"<\/(X|x)>","g");
					document.getElementById('ondeck').innerHTML = document.getElementById('ondeck').innerHTML.replace(thisvariable, document.getElementById(document.getElementById(Xhtml).innerHTML).value);
					document.getElementById('doc').innerHTML = document.getElementById('doc').innerHTML.replace(thisvariable, document.getElementById(document.getElementById(Xhtml).innerHTML).innerHTML);
					console.log("thisvariable: "+thisvariable);
					console.log("Variable name: "+document.getElementById(Xhtml).innerHTML);
					console.log("Variable value: "+document.getElementById(document.getElementById(Xhtml).innerHTML).value);
				}
				document.getElementById('Choices').innerHTML = '';
				setTimeout(function() {renderQnA(Qhtml,Jhtml,Dhtml,restart)}, 300);
			} else {
				document.getElementById('Choices').innerHTML = '';
				renderQnA(Qhtml,Jhtml,Dhtml,restart);			
			}

		}
		
	}


	function renderQnA(Qht,Jht,Dht,restar) {
		Dhtml = Dht;
					
		var GOTOfired = 0;
		swapGOTO(Qht,Jht);

		if (GOTOfired == 0) {
			document.getElementById('QandA').innerHTML += "<div id="+Jht+" style=\"float:left;width:100%;height:1px;\">&nbsp;</div>";
		}
		document.getElementById('QandA').innerHTML += "<div class='frame'><div class='full'><div class='question_text'>"+ document.getElementById(Qhtml).innerHTML+"</div></div><div class='question_arrow'></div></div>";		

		document.getElementById('QandA').innerHTML = document.getElementById('QandA').innerHTML.replace(/(\<br\>){2}/gi,"</div></div><div class='question_arrow'></div></div></div></div><div class='frame'><div class='full'><div class='question_text'>");
		document.getElementById('QandA').innerHTML = document.getElementById('QandA').innerHTML.replace(/(\<br\> \<br\>)/gi,"<br><br>");

		// add question 
		document.getElementById('transcript').value += "BOT: "+ document.getElementById(Qhtml).innerHTML;
		document.getElementById('transcript').value = document.getElementById('transcript').value.replace(/(\<br\>){2}/gi,"\nBOT: ");
				
		if (document.getElementById(Dhtml)) {
			document.getElementById('doc').innerHTML += document.getElementById(Dhtml).innerHTML;
		}
						
		tmp = getElementsByIdRegExp("div", "A-"+label+"(\\.{1}\\d){1}$");
		a_href = getElementsByIdRegExp("div", "A-href-"+label+"(\\.{1}\\d){1}$");
		a_target = getElementsByIdRegExp("div", "A-target-"+label+"(\\.{1}\\d){1}$");
		tmp_x = getElementsByIdRegExp("div", "X-"+label+"(\\.{1}\\d){1}$");
		var Xishere = 0;
		for ( var i = 0; i < tmp.length; i++ ) {
			var nextlabel = tmp[i].id.substr(2);
			var Xihtml = 'Xi-'+nextlabel;
			var regexp = "\<variable\>";
			var regexp_js = "^javascript:";
			if (tmp[i].innerHTML.match(regexp)) {
				document.getElementById('Choices').innerHTML += "<div class=\"xdiv\"><input type=\"text\" id=\""+Xihtml+"\" name=\""+Xihtml+"\" class=\"xinput\" onkeypress=\"{if (event.keyCode==13)answerQ('"+nextlabel+"')}\"/><a href=\"javascript:void('');\" class=\"xbutton\" onClick=\"answerQ('"+nextlabel+"');\"><span class=\"qpad\">Save above text as answer.</span></a></div>";
				Xishere = Xihtml;
			} else if (a_href[i].innerHTML.match(regexp_js) && a_href[i].innerHTML != "javascript:void('');") {
				tmp[i].innerHTML = tmp[i].innerHTML.replace(/(\<br\>){2}/gi,"<br> <br>");
				var script_call = a_href[i].innerHTML.replace(/^javascript:/gi,"");
				document.getElementById('Choices').innerHTML += "<a href=\"javascript:void('');\" class=\"qabutton\" onClick=\"answerQ('"+nextlabel+"');"+script_call+"\" "+a_target[i].innerHTML+"><span class=\"qpad\">"+tmp[i].innerHTML+"</span></a>";							
			} else {
				tmp[i].innerHTML = tmp[i].innerHTML.replace(/(\<br\>){2}/gi,"<br> <br>");
				document.getElementById('Choices').innerHTML += "<a href=\""+a_href[i].innerHTML+"\" class=\"qabutton\" onClick=\"answerQ('"+nextlabel+"');\" "+a_target[i].innerHTML+"><span class=\"qpad\">"+tmp[i].innerHTML+"</span></a>";				
			}
		}			

		if (restar == undefined) {
			document.getElementById('Choices').innerHTML += "<a href=\"javascript:void('');\" class=\"qabutton\" onClick=\"startAT('1');\"><span class=\"qpad\">Start over.</span></a>";
		}
				
		if (QNum != 0) { 
			scroll2Q(Jht);           	
		} else if (restar != undefined) {
			window.scrollTo(0,0);
		}
		if (Xishere != 0 && window.self == window.top) {
			console.log("Set focus for: "+Xishere);
			document.getElementById(Xishere).focus();
		}
		console.log("Q#: "+QNum);
		QNum++;
			
	}

	
	function swapGOTO(QH,JH) {
		var regex = new RegExp("GOTO:(\d*)(\.\d+)*");
		if (regex.test(document.getElementById(QH).innerHTML)) {
			var Qtext = document.getElementById(QH).innerHTML.match(/(GOTO:(\d*)(.\s*\d+)*)/);
			document.getElementById('QandA').innerHTML += "<div id="+JH+" style=\"float:left;width:100%;height:1px;\">&nbsp;</div>";
			// Add question
			// note I added () around the < to avoid a < followed by a ? which causes problems in php
			var Qtexttrans = document.getElementById(QH).innerHTML.replace(/(<)?GOTO:(\d*)(.\s*\d+)*>?/,"");
			Qtexttrans = Qtexttrans.replace(/\s*$/,"");
			if (Qtexttrans != "") {
				document.getElementById('transcript').value += "BOT: "+Qtexttrans+"\n";
			}
			if (document.getElementById(QH).innerHTML.match(/^GOTO:(\d*)(.\s*\d+)*/)) {
				document.getElementById('QandA').innerHTML += document.getElementById(QH).innerHTML.replace(/(<)?GOTO:(\d*)(.\s*\d+)*>?/,"<"+Qtext+">");
			} else {
				document.getElementById('QandA').innerHTML += "<div class='frame'><div class='full'><div class='question_text'>"+ document.getElementById(QH).innerHTML.replace(/(<)?GOTO:(\d*)(.\s*\d+)*>?/,"<"+Qtext+">")+"</div></div><div class='question_arrow'></div></div>";						
			}
			// replace GOTO with text
			label = Qtext[0].replace("GOTO:","");
			Qhtml = 'Q-'+label;
			if (document.getElementById(Dhtml)) {
				document.getElementById('doc').innerHTML += document.getElementById(Dhtml).innerHTML;
			}
			Dhtml = 'D-'+label;
			GOTOfired = 1;
			swapGOTO(Qhtml,JH);
		}
	}

	
	function scroll2Q(id) {
		var top = document.getElementById(id).offsetTop; //Getting Y of target element
		console.log("Jump to Y for ("+id+"): "+top);
		//adapted from https://github.com/Yappli/smooth-scroll
		var speed = 800;
		var moving_frequency = 5; // Affects performance !
		var hop_count = speed/moving_frequency
        var getScrollTopDocumentAtBegin = document.documentElement.scrollTop + document.body.scrollTop;
        var gap = (top - getScrollTopDocumentAtBegin) / hop_count;
		for(var i = 1; i <= hop_count; i++)
        {
        	(function()
           	{
           		var hop_top_position = gap*i;
           	    setTimeout(function(){  window.scrollTo(0, hop_top_position + getScrollTopDocumentAtBegin); }, moving_frequency*i);
           	 })();
        }
	}

	function getElementsByIdIs(selectorTag, name) {
		var items = [];
		var myPosts = document.getElementsByTagName(selectorTag);
			//omitting undefined null check for brevity
			if (myPosts[0].id == name) {
				items.push(myPosts[0]);
			}
		
		return items;
	}

	function getElementsByIdRegExp(selectorTag, expression) {
		// note you need to escape \ in the expression with \, i.e., \\ = \
		var regex = new RegExp(expression);
		var items = [];
		var myPosts = document.getElementsByTagName(selectorTag);
		for (var i = 0; i < myPosts.length; i++) {
			if (regex.test(myPosts[i].id)) {
				items.push(myPosts[i]);
			}
		}
		
		return items;
	}	

	// startAT QnA
	function startAT(id) {
		document.getElementById('ondeck').innerHTML = document.getElementById('original').value;
		document.getElementById('QandA').innerHTML = "";
		document.getElementById('transcript').value = "";
		QNum = 0;
		answerQ(id,'1');
	}
		
	//show funtion
	function show(id) { 
   		if (document.getElementById) { // DOM3 = IE5, NS6
        	document.getElementById(id).style.display = 'block';
    	} else { 
        	if (document.layers) {  
            	document.id.display = 'block';
        	} else {
                document.all.id.style.display = 'block';
        	}
    	}
	}

	//hide funtion
	function hide(id) { 
    	if (document.getElementById) { // DOM3 = IE5, NS6
        	document.getElementById(id).style.display = 'none';         
    	} else { 
        	if (document.layers) {  
                document.id.display = 'none';
        	} else {
                document.all.id.style.display = 'none';
        	}
    	}
	}

	//show OR hide funtion depends on if element is shown or hidden
	function shoh(id) { 
    	if (document.getElementById) { // DOM3 = IE5, NS6
        	if (document.getElementById(id).style.display == "none"){
            	document.getElementById(id).style.display = 'block';
        	} else {
            	document.getElementById(id).style.display = 'none';         
        	}   
    	} else { 
        	if (document.layers) {  
            	if (document.id.display == "none"){
                	document.id.display = 'block';
            	} else {
                	document.id.display = 'none';
            	}
        	} else {
            	if (document.all.id.style.visibility == "none"){
                	document.all.id.style.display = 'block';
            	} else {
                	document.all.id.style.display = 'none';
            	}
        	}
    	}
	}

	function transcript(output) {
		if (output == 1) {
			return document.getElementById('transcript').value;
		} else {
			var output = document.getElementById('transcript').value.replace(/<[^>]*>/g,"");
			return output;
		}
	}		
	
	function doc() {
		return document.getElementById('doc').innerHTML;
	}	

	function mail2(to,subject,body) {
		to = encodeURIComponent(to);
		subject = encodeURIComponent(subject);
		body = encodeURIComponent(body);
		window.location.href = "mailto:"+to+"?subject="+subject+"&body="+body;
	}
	
	function submit2(action,method,docAs,instructions,transcriptAs) {
		document.FORM.action = action;
		document.FORM.method = method; 
		if (docAs) {
			var doctext = document.createElement("textarea");
			doctext.style.display ='none';
			doctext.name= docAs;
			doctext.value= document.getElementById('doc').innerHTML;
			document.getElementById('FORM').appendChild(doctext);
			if (instructions) {
				var instructtext = document.createElement("textarea");
				instructtext.type='hidden';
				instructtext.style.display ='none';
				instructtext.name= 'i';
				instructtext.value= instructions;
				document.getElementById('FORM').appendChild(instructtext);	
			}
		}
		if (transcriptAs) {
			var ttext = document.createElement("textarea");
			ttext.type='hidden';
			ttext.style.display ='none';
			ttext.name= transcriptAs;
			ttext.value= document.getElementById('transcript').value;
			document.getElementById('FORM').appendChild(ttext);
		}
		document.getElementById('ondeck').innerHTML = "";
		document.FORM.submit();
	}

	// h/t http://runnable.com/U5HC9xtufQpsu5aj/use-javascript-to-save-textarea-as-a-txt-file
	function save2(filename,content)
	{

	// I'm using file system support as a proxy for support for this feature. 
	// Check based on one found at: http://blog.teamtreehouse.com/building-an-html5-text-editor-with-the-filesystem-apis
	// Handle vendor prefixes.
	window.requestFileSystem = window.requestFileSystem || 
							   window.webkitRequestFileSystem;
	// Check for support.
	if (window.requestFileSystem) {
	// content = ID of textarea to save
	// name = name to save file as, including file extension     
	// grab the content of the form field and place it into a variable
	//    var textToWrite = document.getElementById(content).value;
	//  create a new Blob (html5 magic) that conatins the data from your form feild
		var textFileAsBlob = new Blob([content], {type:'text/plain'});
		
	// Specify the name of the file to be saved
		var fileNamecontentAs = filename;
		
	// Optionally allow the user to choose a file name by providing 
	// an imput field in the HTML and using the collected data here
	// var fileNamecontentAs = txtFileName.text;

	// create a link for our script to 'click'
		var downloadLink = document.createElement("a");
	//  supply the name of the file (from the var above).
	// you could create the name here but using a var
	// allows more flexability later.
		downloadLink.download = fileNamecontentAs;
	// provide text for the link. This will be hidden so you
	// can actually use anything you want.
		downloadLink.innerHTML = "My Hidden Link";
		
	// allow our code to work in webkit & Gecko based browsers
	// without the need for a if / else block.
		window.URL = window.URL || window.webkitURL;
			  
	// Create the link Object.
		downloadLink.href = window.URL.createObjectURL(textFileAsBlob);
	// when link is clicked call a function to remove it from
	// the DOM in case user wants to save a second file.
		downloadLink.onclick = destroyClickedElement;
	// make sure the link is hidden.
		downloadLink.style.display = "none";
	// add the link to the DOM
		document.body.appendChild(downloadLink);
		
	// click the new link
		downloadLink.click();
	} else {
		alert('This feature is not supported by your browser.');
	}
		
	}

	function destroyClickedElement(event)
	{
	// remove the link from the DOM
		document.body.removeChild(event.target);
	}

	// EOF

</script></BODY>
</HTML>
