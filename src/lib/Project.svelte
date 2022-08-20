<script>
	export let project;
	let one = project.split('/')[0];
	let two = project.split('/')[1];
	let CardApp = `https://project-card-app.herokuapp.com/project_card/${one}/${two}?theme=light`;
	let Github = `https://github.com/${one}/${two}`;
</script>

<a href={Github}>
	<img src={CardApp} alt={project} />
</a>

