<script lang="ts">

    // $effect.pre(()=>{
    //     console.log("Random Number effect pre : ", randomNumber);
    // })
    

    let randomNumber = $state(Math.floor(Math.random() * 10));
    let doubleRandomNumber = $derived(randomNumber * 2)


    



    $effect(() => {
        console.log("Random Number : ", randomNumber);
    });





</script>

<h1>Random Number</h1>


<h3>Random NUmber. : {randomNumber}</h3>
<h3>Double Random Number. : {doubleRandomNumber}</h3>

<button onclick={() => randomNumber = Math.floor(Math.random() * 10)}>Randomize</button> 