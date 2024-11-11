<script>
    let searchQuery = '';

    function handleSearch() {
        console.log('Searching for:', searchQuery);
        // Add your search logic here
    }
</script>

<style>
    .search-container {
        display: flex;
        align-items: center;
        /* border: 1px solid #aaa; */
        border-radius: 25px;
        width: 50%;
        padding: 5px 10px;
        background-color: #beffbe4c;
    }

    .search-icon {
        margin-right: 10px;
        width: 20px;
        height: 20px;
    }

    .search-input {
        border: none;
        outline: none;
        flex: 1;
        font-size: 16px;
        background-color: transparent;
        padding: 2px 0; 
        margin: 0; 
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    .search-input::placeholder {
        color: #aaa;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }
</style>

<div class="search-container">
    <svg class="search-icon" aria-labelledby="title desc" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 19.9 19.7">
        <title id="title">Search Icon</title>
        <desc id="desc">A magnifying glass icon.</desc>
        <g class="search-path" fill="none" stroke="#000000">
            <path stroke-linecap="square" d="M18.5 18.3l-5.4-5.4"/>
            <circle cx="8" cy="8" r="7"/>
        </g>
    </svg>
    <input
        type="text"
        class="search-input"
        placeholder="Search something ..."
        bind:value={searchQuery}
        on:input={handleSearch}
    >
</div>