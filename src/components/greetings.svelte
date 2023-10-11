<script>
    export let data

    let arr = 0;
    
    function clickIt() {
        arr += 1; 
    }

</script>

    <h1>Welcome to svelte learning</h1>
    <button on:click = {clickIt}> 
        Clicked {arr}
        {arr === 1 ? 'time' : 'times'}

    </button>
    <div>{data}</div>