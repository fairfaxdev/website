<script>
    import Recentapps from "./RecentApps.svelte";
    import Startlinks from "./StartLinks.svelte";
</script>

<div class="startmenu">
    <Recentapps />
    <Startlinks />
</div>

<style lang="scss">
    :root {
        --start-menu: rgba(0,0,0,.7);
        --start-menu-glass: linear-gradient(
            to top,
            rgba(50, 50, 50, 0.75),
            rgba(0, 0, 0, 0.75) 50%,
            rgba(100, 100, 100, 0.75)
        );
        --start-radius: 6px;
        --start-border-color: rgba(0, 0, 0, 0.7);
    }
    .startmenu {
        border: 1px solid var(--start-border-color); 
        overflow: visible; 
        display: inline-block;
        border-top-left-radius: var(--start-radius);
        border-top-right-radius: var(--start-radius);
        position: absolute;
        bottom: 30px;
        left: 0;
        z-index: 15;
        box-shadow: inset 0 0 1px #fff;
        background-color:var(--start-menu);
        background: var(--start-menu-glass);
        backdrop-filter: blur(1.5px);
    }
</style>