<script lang="ts">
	import Experience from "../Experience.svelte";
	import Education from "../Education.svelte";

	let experiences = [
		{
			jobTitle: 'Fullstack Developer',
			company: 'Storebrand',
			startDate: 'October 2021',
			endDate: 'Present',
			description: 'React, Java 11, PostgreSQL, Couchbase',
		},
		{
			jobTitle: 'Fullstack Developer',
			company: 'Apcoa Parking Norway',
			startDate: 'February 2021',
			endDate: 'October 2021',
			description: 'Node, Angular, Ionic, PostgreSQL',
		},
		{
			jobTitle: 'Fullstack Developer',
			company: 'SuperEgo AS',
			startDate: 'October 2020',
			endDate: 'February 2021',
			description: 'React, Android, PHP.',
		},
	];

	let educations = [
		{
			degree: 'Ms Industrial Economics',
			university: 'NTNU',
			startDate: 'Aug 2016',
			endDate: 'Jun 2020',
			description: 'Integrated 5-year engineering program.'
		},
		{
			degree: 'Bachelor in mathematics',
			university: 'NTNU',
			startDate: 'Aug 2013',
			endDate: 'Jun 2016',
			description: ''
		},
	];
</script>

<svelte:head>
	<title>Resume</title>
	<meta name="description" content="Resume" />
</svelte:head>

<div class="text-column">
	<h1>Resume</h1>

	<p>
		I am 4x Certified in Azure and Google Cloud Platform. 482.5 student credits from NTNU, Trondheim. I was also a finalist in the National Math Competition for High school students in 2013. I generally enjoy thinking about complex problems.
	</p>

	<h2>Work Experience</h2>
	{#each experiences as experience (experience.company)}
		<Experience {...experience} />
	{/each}

	<h2>Education</h2>
	{#each educations as education (education.degree)}
		<Education {...education} />
	{/each}

	<h2>Certifications and Courses</h2>
	<ul>
		<li>AZ-204: Developing Solutions for Microsoft Azure</li>
		<li>AZ-104: Microsoft Azure Administrator </li>
		<li>AZ-900: Microsoft Azure Fundamentals </li>
		<li>Google Cloud: Associate Cloud Engineer </li>
		<li>Total Typescript by Matt Pocock</li>
		<li>Epic React by Kent C. Dodds</li>
		<li>NSM grunnprinsipper for IKT-sikkerhet</li>
	</ul>

</div>
