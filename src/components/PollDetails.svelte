<script>
  export let poll;
</script>

<div class="poll">
  <h3>{poll.question}</h3>
  <div class="answer">
    <div class="percent percent-a"></div>
    <span>{poll.answerA} ({poll.votesA})</span>
  </div>
</div>

<style>
</style>