<script>
  export let slidecontainer = ''; 
  export let title = '';
</script>


<div class="slidecontainer">
  <p class="title is-4">{ title }</p>
  <input type="range" min="1" max="100" value="50" class="slider" id="myRange">
</div>
