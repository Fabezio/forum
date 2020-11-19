<!-- <p>dialog</p> -->
<script>
  import User from './User.svelte'
  export let sentence;
  // export let user;
  console.log(sentence)
</script>

<!-- {#each dialog as sentence} -->
<div class="sentence">

    <div><User user={sentence.user} /> {sentence.said}</div>
    
    {#if sentence.interloc == true}
    {#each sentence.answers as answer}
      <!-- content here -->
      
      <svelte:self sentence={answer} />
      {/each}
    <!-- content here -->
  
    <!-- else content here -->
    {/if}
  <!-- content here -->
<!-- {/each} -->

</div>


<style>
    .sentence {
        margin-left: 20px;
        padding: 7px;
        /* border-top: 1px solid grey; */
        
    }
    .bold {
       font-weight: bold; 
    }
</style>