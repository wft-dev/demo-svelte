<script lang="ts">
  let searchText :any = ''

  const getSearchTextFn = (e:any) => {
    if(e.target.value.length > 0){
      searchText = e.target.value
    }else{
      searchText = ''
    }

    console.log(searchText)
  }





 
</script>


<div class="header">
  <div> 
    <p><a href="">BG</a></p>
  </div>
  <div class="searchText">
    <input type="search" on:keyup={(e:any)=>getSearchTextFn(e)} placeholder="Search...!">
  </div>
</div>


<style>
    .header{
        margin: 0px;
        padding: 10px;
        background: aliceblue;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    .header a{
        text-decoration: none;
        font-weight: 500    ;
        color: blaack;
    }
    .searchText{
        width: 300px;
    }
</style>