<script>
 export let leftSideLogo = "https://pbs.twimg.com/profile_images/1498367008789905413/C61plwJx_400x400.jpg"
 export let rightSideLogo = ""
 export let title = "Nomad twitter"
 export let link ='https://twitter.com/Nomad_eSport'
 export let backgroundcolor = ''
 

 
</script>

<div>
    <div> 

    <input type="url" bind:value={link} placeholder="enter your link"> 
    <input type="url" bind:value={leftSideLogo} placeholder="enter your leftside logo"> 
    <input type="text" bind:value={title} placeholder="enter your title">
    <input type="url" bind:value={rightSideLogo} placeholder="enter your right side logo"> 
    <input bind:value={backgroundcolor} placeholder="enter your color"> 

</div>
    
<a href={link || "https://twitter.com/"} class="title"> <div class="link-card wa-link" style:background-color={backgroundcolor || 'blue'}  >
    
    {#if  leftSideLogo !== ''}
    <img src={leftSideLogo || "https://pbs.twimg.com/profile_images/1498367008789905413/C61plwJx_400x400.jpg"} alt="" width="52px" class="space" height="52px"/>
    {/if}
     <p class="wa-title-ml wa-title-only wa-space wa-icon-margin" >{title}</p>
    
</div></a>{#if rightSideLogo !== ''}
    <img src={rightSideLogo} alt='' width="52px" class='space' height="52px"/>
    {/if}
</div>



<style>
.link-card{
  border-radius: 12px;
  min-height: 68px;
  box-shadow: 0 4px 8px rgb(50 50 50 / 20%);
  border-width: 0;
  overflow: hidden;
  display: flex;
  justify-content: stretch;
  align-items: center;
  
}
input {
  width: 15%;
  padding: 12px 20px;
  margin: 8px 0;
  box-sizing: border-box;
}

.space {
    padding: 10px;
}

.wa-space {
  flex-grow: 1;
}

a{
    all: unset;
}



.wa-link {
  cursor: pointer;
}
</style>
