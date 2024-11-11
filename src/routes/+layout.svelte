<script>
    import Newspaper from "$lib/navbar/Newspaper.svelte";
    import Profile from "$lib/navbar/Profile.svelte";
    import Search from "$lib/body/Search.svelte";
</script>

<main>
    <nav>
        <Newspaper />
        <div class="sitename">InsightDairy</div>
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
    justify-content: space-between;
    align-items: center;
    position: relative;
    box-sizing: border-box;
  }
  
  .sitename {
    position: absolute;
    left: 50%;
    font-family: 'insightdairy', sans-serif;
    font-size: 24px;
  transform: translateX(-50%);
}
</style>