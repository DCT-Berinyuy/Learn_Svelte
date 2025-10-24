<!--	JavaScript	-->
<script>
	const formValues = {
		name: "",
		profileSummary: "",
		country: '',
		jobLocation: [],
		remoteWork: false,
		skillSet: [],
		yearsOfExperience: '',
	}

	function submitForm() {
		console.log(formValues)
	}
</script>

<!--	HTML	-->
<main>
	<div>
		<pre>
			{JSON.stringify(formValues, null, 2)}
		</pre>
	</div>
	<form on:submit|preventDefault={submitForm}><!--We specify a modifier using a pipe character-->
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

		<div>
			<input type="checkbox" name="" id="remoteWork" bind:checked={formValues.remoteWork} />
			<label for="remoteWork">Open for remote work?</label>
		</div>

		<div>
			<label for="">Skill set</label>
			<input 
			type="checkbox" 
			id="html" 
			value="html" 
			bind:group={formValues.skillSet} 
			/>
			<label for="html">HTML</label>
			<input 
			type="checkbox" 
			id="css" 
			value="css" 
			bind:group={formValues.skillSet} 
			/>
			<label for="css">CSS</label>
			<input 
			type="checkbox" 
			id="javascript" 
			value="javascript" 
			bind:group={formValues.skillSet} 
			/>
			<label for="javascript">JavaScript</label>
		</div>

		<div>
			<label for="">Years of Experience</label>
			<input 
			type="radio" 
			id="0-2" 
			value="0-2" 
			bind:group={formValues.yearsOfExperience} 
			/>
			<label for="0-2">0-2</label>
			<input 
			type="radio" 
			id="3-5" 
			value="3-5" 
			bind:group={formValues.yearsOfExperience} 
			/>
			<label for="3-5">3-5</label>
			<input 
			type="radio" 
			id="6-10" 
			value="6-10" 
			bind:group={formValues.yearsOfExperience} 
			/>
			<label for="6-10">6-10</label>
		</div>

		<div>
			<button>Submit</button>
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