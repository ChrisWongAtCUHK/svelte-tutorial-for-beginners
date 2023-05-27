<script>
  import { createEventDispatcher } from 'svelte';
  import PollDetails from './PollDetails.svelte';
  export let polls = [];

  const dispatch = createEventDispatcher();

  const handleVote = (e) => {
    const {option, id} = e.detail;
    
    dispatch('vote', {option, id});
  };
</script>

<div class="poll-list">
  {#each polls as poll(poll.id)}
    <PollDetails {poll} on:vote={handleVote}/>
  {/each}
</div>

<style>
  .poll-list {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 20px;
  }
</style>