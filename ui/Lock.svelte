<form>
	<fieldset>
		<p>Contract</p>
		<input type="text" id="lcont" name="fname">
		<p>Amount</p>
		<input type="text" id="lamt" name="fname">
		<p>Lock date</p>
		<input type="date" id="ldate" name="trip-start"
			value="2018-07-22"
			min="2018-01-01" max="2018-12-31">
		<input  type="submit" id="lock" value="Lock">
	</fieldset>
	<fieldset>
		<p>Contract</p>
		<input type="text" id="wcont" name="fname">
		<p>Amount</p>
		<input type="text" id="wamt" name="fname"><br><br>
		<input type="submit" id="withdrw" value="Withdraw">
	</fieldset>
</form>

<style>
	form{
	display: inline-block;
	background-color: #15baff;
	width: 65%;
	outline: 1px solid black;
	padding: 2% 0;
	margin: 5% 0 5% 15%;	
}
	p{
		color: 	#800080;
}
	input[type=text] {
		width: 70%;
		border: none;
		background-color: #15baff;
		border-bottom: 2px solid black;
		outline: none;
}
	input[type=submit] {
		width: 30%;
		padding: 5px;
		color: white;
		background-color: #BA55D3;
		float: right;
}
	fieldset{
		border: 3px solid black;
		width: 90%;
		height: 60%;
		margin: 0 auto;
		margin-bottom: 1%;
}
</style>
