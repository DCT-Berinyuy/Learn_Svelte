<!--	JavaScript	-->
<script>
	const formValues = {
		name: "",
		profileSummary: "",
		country: '',
		jobLocation: []
	}
</script>

<!--	HTML	-->
<main>
	<div>
		<pre>
			{JSON.stringify(formValues, null, 2)}
		</pre>
	</div>
	<form action="">
		<div>
			<label for="name">Name</label>
			<input type="text" id="name" bind:value={formValues.name}/>
		</div>

		<div>
			<label for="profile">Profile</label>
			<textarea name="" id="profile" bind:value={formValues.profileSummary}/>
		</div>

		<div>
			<label for="country">Country</label>
			<select name="" id="country" bind:value={formValues.country}>
				<option value="">Select a country</option>
				<option value="cameroon">Cameroon</option>
				<option value="rwanda">Rwanda</option>
				<option value="nigeria">Nigeria</option>
			</select>
		</div>

		<div>
			<label for="job-location">Job Location</label>
			<select name="" id="job-location" bind:value={formValues.jobLocation} multiple>
				<option value="">Select a country</option>
				<option value="cameroon">Cameroon</option>
				<option value="rwanda">Rwanda</option>
				<option value="nigeria">Nigeria</option>
				<option value="gana">Gana</option>
			</select>
		</div>
	</form>
</main>

<!--	CSS		-->
<style>
	input + label {
		display: inline-flex;
	}
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}
	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>