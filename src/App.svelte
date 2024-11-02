<script>
	import FeedbackList from "./components/FeedbackList.svelte";

	let feedback = [
		{
			id: 1,
			rating: 10,
			text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quae.'
		},
		{
			id: 2,
			rating: 9,
			text: 'Laboris quis incididunt enim cupidatat exercitation culpa magna aliquip cillum deserunt.'
		},
		{
			id: 3,
			rating: 7,
			text: 'Ut quis exercitation consectetur consequat. Exercitation esse aute duis sit ex ipsum fugiat est.'
		},
	];

	const deleteFeedback = (e) => {
		const itemId = e.detail;
		feedback = feedback.filter((item) => item.id !== itemId);	}
</script>

<main class="container">
	<FeedbackList {feedback} on:delete-feedback={deleteFeedback}/>
</main>

