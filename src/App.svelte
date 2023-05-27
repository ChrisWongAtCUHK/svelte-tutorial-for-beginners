<script>
  import Header from './components/Header.svelte';
  import Footer from './components/Footer.svelte';
  import PollList from './components/PollList.svelte';
  import CreatePollForm from './components/CreatePollForm.svelte';
  import Tabs from './shared/Tabs.svelte';

  let items = ['Current Polls', 'Add New Poll'];
  let activeItem = items[0];

  const tabChange = (e) => {
    activeItem = e.detail;
  };

  let polls = [{
    id: 1,
    question: 'Python or JavaScript?',
    answerA: 'Python',
    answerB: 'JavasSript',
    votesA: 9,
    votesB: 15
  }];

  const addPoll = (e) => {
    const poll = e.detail;
    polls = [poll, ...polls];
    console.log(polls);
    activeItem = items[0];
  };

  const handleVote = (e) => {
    const {option, id} = e.detail;
    
    let copiedPolls = [...polls];
    let upvotedPoll = copiedPolls.find(poll => poll.id == id);

    upvotedPoll[option]++
    polls = copiedPolls;
  };
</script>

<Header/>
<main>
  <Tabs {items} {activeItem} on:tabChange={tabChange}/>
  {#if activeItem === items[0]}
    <PollList {polls} on:vote={handleVote}/>
  {:else if activeItem === items[1]}
    <CreatePollForm on:add={addPoll}/>
  {/if}
</main>
<Footer/>

<style>
  main {
    max-width: 960px;
    margin: 40px auto;
  }
</style>
