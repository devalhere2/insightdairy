<script>
    import Newspaper from "$lib/navbar/Newspaper.svelte";
    import Profile from "$lib/navbar/Profile.svelte";
    import Search from "$lib/navbar/Search.svelte";
</script>

<main>
    <nav>
        <div class="newspaper">
            <Newspaper />
        </div>
        <div class="site-name">InsightDairy</div>
        <div class="search-bar">
            <Search />
        </div>
        <Profile />
    </nav>
</main>
<slot />  
  <style>
    @font-face {
    font-family: 'insightdairy';
    src: url('/Anton.ttf') format('truetype');
  }
    nav {
        height: 60px;
        border-bottom: 1px solid #ccc;
        display: flex;
        align-items: center;
        position: relative;
        box-sizing: border-box;
    }
    
    .newspaper {
        flex: 1;
    }
    .site-name {
        position: absolute;
        left: 50%;
        font-family: 'insightdairy', sans-serif;
        font-size: 24px;
        transform: translateX(-50%);
    }

    .search-bar {
        width: 300px;

    }

</style>