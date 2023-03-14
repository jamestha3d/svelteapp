<script>
	import FeedbackList from './components/FeedbackList.svelte';
	import FeedbackStats from './components/FeedbackStats.svelte';
	import FeedbackForm from './components/FeedbackForm.svelte';
	

	/* we do not need this anymore as we are using the store
	let feedback = [ insert your objects here] */
	



	/* const addFeedback = (e) => {
		//console.log('got here')
		const newFeedback = e.detail
		feedback = [newFeedback, ...feedback]
	} */

	/* const deleteFeedback = (e) => {
		const itemId = e.detail
		feedback = feedback.filter((item)=> item.id != itemId)
	} */
	
</script>

<main class="container">
	<!--<FeedbackForm on:add-feedback={addFeedback} />-->
	<FeedbackForm />
	<!--<FeedbackStats {count} {average} />-->
	<FeedbackStats />
	<!-- <FeedbackList on:delete-feedback={deleteFeedback}/> -->
	<FeedbackList />
	
</main>

