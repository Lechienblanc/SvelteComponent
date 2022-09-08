<script>

    let currentTab = 0;

    export let titre1 = ''; 
    export let titre2 = ''; 
    export let titre3 = ''; 
    export let titre4 = '';

    export let article_titre1 = ''; 
    export let article_titre2 = ''; 
    export let article_titre3 = ''; 
    export let article_titre4 = '';

    export let article_content1 = ''; 
    export let article_content2 = ''; 
    export let article_content3 = ''; 
    export let article_content4 = '';

    export let article_img1 = '';
    export let article_img2 = '';
    export let article_img3 = '';
    export let article_img4 = '';

    const setActive = (index) => {
    currentTab = index;
  }
  
  </script>

<div class="container">
    <div class="sidemenu">
        <div class="titre">
            <h1 on:click={
                (() => {
                  setActive(0);
                })} >
                { titre1 }
                </h1>
        </div> 
        <div class="titre">
            <h1 on:click={
                (() => {
                  setActive(1);
                })} >
                { titre2 }
                </h1>
        </div>
        <div class="titre">
            <h1 on:click={
                (() => {
                  setActive(2);
                })} >
                { titre3 }
                </h1>
        </div>
        <div class="titre">
            <h1 on:click={
                (() => {
                  setActive(3);
                })} >
                { titre4 }
                </h1>
        </div>
    </div>

<div class="content">
    {#if currentTab === 0}
    <article>
      <h2>{ article_titre1 }</h2>
      <p>{ article_content1 }</p>
      <img src="{article_img1}" alt="">
    </article>
    {:else if currentTab === 1}
    <article>
      <h2>{ article_titre2 }</h2>
      <p>{ article_content2 }</p>
      <img src="{article_img2}" alt="">
    </article>
    {:else if currentTab === 2}
    <article>
      <h2>{ article_titre3 }</h2>
      <p>{ article_content3 }</p>
      <img src="{article_img3}" alt="">
    </article>
    {:else if currentTab === 3}
    <article>
      <h2>{ article_titre4 }</h2>
      <p>{ article_content4 }</p>
      <img src="{article_img4}" alt="">
    </article>
    {/if}
  </div>
  </div>

<style>

.container{
    border: 1px solid black;
    width: 30vw;
}

.sidemenu{
    display: flex;
}

.titre{
    text-align: center;
    cursor: pointer;
    background-color: lightgrey;
    border: 1px solid black;
    width: 100%;
    padding-top: 10px;
    padding-bottom: 10px;
}

.content{
    padding: 20px;
}

</style>