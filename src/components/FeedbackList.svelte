<script>
    //import {onMount, onDestroy} from 'svelte'
    import {fade, scale} from 'svelte/transition';
    import FeedbackItem from "./FeedbackItem.svelte";
    import {FeedbackStore} from '../stores'
    

    //replacing da
    /*
    let feedback = []
    const unsubscribe = FeedbackStore.subscribe( (data) => feedback = data)

     onMount(() => {
        console.log('mounted')
    })

    //unsubscribe in the undestroy
    onDestroy( () => {
        unsubscribe()
    }) */

    //console.log(feedback)
</script>
<!--since we do not have an equal to on the delete-feedback prop, it is just forwarded up to the app where feedbacklist is embedded-->
<!-- {#each feedback as fb (fb.id)} if we use feedback then we have to manually unsubscribe-->
{#each $FeedbackStore as fb (fb.id)}
    
    <div in:scale out:fade="{{duration: 500}}">
        <!--since we do not have an = on the delete-feedback prop, it is just forwarded up to the app where feedbacklist is embedded-->
    <!-- we are not able to use transitions on custom components so we put it on div eg we could say transition:fade-->
        <!--<FeedbackItem item={fb} on:delete-feedback/>-->
        <FeedbackItem item={fb} />
    </div>
    
{/each}