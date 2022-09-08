<script>
    let xPos = 50;
    let yPos = 50;
    import Link from './Link.svelte'
</script>
  
  <label for="positionX">X </label>
  <input id="positionX" type="range" min="0" max="36" bind:value="{xPos}" />
  
  <label for="positionY">Y </label>
  <input id="positionY" type="range" min="0" max="74" bind:value="{yPos}" />
  
  <div class="box"  style="left: {xPos}%; top: {yPos}%">
    <Link></Link>
  </div>
  
  <style>
    .box {
      
      
      position: absolute;
    }
  </style>