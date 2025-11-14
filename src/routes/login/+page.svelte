    <script lang="ts">
        import { goto } from "$app/navigation";




        let email: string;
        let password: string;
        let error : string;


        const submitFN= async()=>{

            if(!email || !password){
                error = "Please fill in all fields"
                return
            }

            console.log(email, password)
            if(email && password){
                goto("/")
            }
        }

        
    </script>



<div class="container">
    <h1>Login Page</h1>

    <form on:submit|preventDefault={submitFN}>
        <label>
		Email
		<input name="email" type="email" bind:value={email}>
        </label>
        <label>
            Password
            <input name="password" type="password" bind:value={password}>
        </label>
        <button disabled={!email || !password} type="submit">Login</button>
        {#if error}
            <p>{error}</p>
        {/if}
    </form>






    <!-- <form on:submit|preventDefault={handleLogin}>
    <input type="email" placeholder="Email" bind:value={email} />
    <input type="password" placeholder="Password" bind:value={password} />
    <button type="submit">Login</button>
  </form> -->

</div>