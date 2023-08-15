<script>
    import { onMount } from 'svelte';
    import Clock from "./Clock.svelte";
    import Startbutton from "./StartButton.svelte";
    import Startmenu from "./StartMenu.svelte";

    let showMenu = false;

    function handleToggle(event) {
        showMenu = event.detail.showMenu;
    }
</script>

{#if showMenu}
<Startmenu />
{/if}
<div class="taskbar">
    <Startbutton on:toggleMenu={handleToggle} />
    <Clock />
</div>

<style lang="scss">
    :root {
        --taskbar-background: linear-gradient(
            to top,
            rgba(21,22,24,.9) 0%,
            rgba(27,28,30,.9) 49%,
            rgba(73,74,76,.9) 50%,
            rgba(135,142,135,.9) 95%,
            rgba(184,178,180,.9) 96%,
            rgba(184,178,180,.9) 99%,
            rgba(27,28,30,.9) 100%
        );
        --taskbar-border: 1px solid;
        --taskbar-border-color: rgba(0,0,0,.1);
        --taskbar-start-indent: 
        3px 0 0 rgba(0,0,0,.8),
        3px 0 3px rgba(255,255,255,.7),
        -3px 0 0 rgba(0,0,0,.8),
        -3px 0 3px rgba(255,255,255,.7);
    
    }
    .taskbar {
        position: absolute;
        width: 100%;
        height: 30px;
        display: flex;
        align-items: center;
        bottom: 0;
        padding: 0 100px;
        background-image: var(--taskbar-background);
        border-top: var(--taskbar-border) var(--taskbar-border-color);
        z-index: 15;
    
        &::before {
            content: '•';
            color: transparent;
            font-size: 10.1rem;
            font-family: serif;
            text-shadow: var(--taskbar-start-indent);
            display: flex;
            justify-content: center;
            align-items:center;
            height: 30px;
            width: 60px;
            position: absolute;
            top: 0;
            left: 5px;
            overflow: hidden;
        }
    }
</style>