<script>
  import Header from './components/Header.svelte';
  import Footer from './components/Footer.svelte';
  import Tabs from './shared/Tabs.svelte';

  let items = ['Current Polls', 'Add New Poll'];
  let activeItem = items[0];

  const tabChange = (e) => {
    activeItem = e.detail;
  };
</script>

<Header/>
<main>
  <Tabs {items} {activeItem} on:tabChange={tabChange}/>
  {#if activeItem === items[0]}
    <p>Poll list component goes here</p>
  {:else if activeItem === items[1]}
    <p>new poll component goes here</p>
  {/if}
</main>
<Footer/>

<style>
  main {
    max-width: 960px;
    margin: 40px auto;
  }
</style>
