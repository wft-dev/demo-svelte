<script lang="ts">
    let text = $state('')

</script>




<h1>
    Helo <span class="textGrey">{text.toUpperCase()}</span>
</h1>
<input type="text" bind:value={text}>

<style>
 .textGrey{
     color: grey;
 }
</style>

<!-- <h1>10th viideo : 8:50</h1> -->