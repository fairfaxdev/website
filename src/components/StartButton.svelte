<script>
    import { createEventDispatcher } from 'svelte';

    const dispatch = createEventDispatcher();
    let showMenu = false;

    function toggleMenu() {
        showMenu = !showMenu;
        dispatch('toggleMenu', { showMenu });
    }
</script>

<button class="start-button" on:click={() => toggleMenu()}>
    <div class="windows-icon">
        <svg class="icon-shadow" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path
            fill="#f8682c"
            d="M9.302 1.415c-1.184.02-2.592.32-4.341 1.044l-2.283 7.949c1.846-.761 3.311-1.114 4.537-1.1a7.596 7.596 0 0 1 4.37 1.593l2.296-7.92c-1.26-.855-2.607-1.599-4.58-1.566"
            />
            <path
            fill="#91c300"
            d="m15.052 3.826-2.256 7.949c2.016 1.367 4.44 2.494 8.907.493L24 4.333h-.042c-4.651 1.931-6.906.846-8.907-.507"
            />
            <path
            fill="#00b4f1"
            d="M6.617 10.77c-1.184.018-2.591.315-4.335 1.034L0 19.779c4.65-1.93 6.863-.803 8.878.55l2.326-7.99c-1.26-.855-2.613-1.6-4.586-1.57"
            />
            <path
            fill="#ffc300"
            d="m12.401 13.114.011.008.003-.008zm.011.008-2.294 7.898c2.015 1.367 4.256 2.453 8.906.522l2.297-7.92c-4.641 1.927-6.882.85-8.909-.5"
            />
        </svg>
    </div>
</button>

<style lang="scss">
:root {
    --start-gradient: linear-gradient(
        to bottom,
        #051b55 50%,
        #74ecfd
    );
    --start-shadow: inset 0 0 2px rgba(0,0,0,.5);
    --start-overlay-gradient: radial-gradient(
        circle,
        rgba(255,255,255,.5) 50%,
        rgba(255,255,255,0)
    );
    --icon-gradient: radial-gradient(
        rgba(255,255,255,.5) 25%,
        rgba(255,255,255,0) 50% 
    );
}
.start-button {
    all: unset;
    position: absolute;
    left: 15px;
    top: -5px;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background-image: var(--start-gradient);
    overflow: hidden;
    box-shadow: var(--start-shadow);
    filter: contrast(1.2);
    z-index: 10;
    
    &::after {
        content: '';
        position: absolute;
        left:0;
        top: -50%;
        display: inline-block;
        width: 100%;
        height: 100%;
        background-image: var(--start-overlay-gradient);
    }
    &:hover {
        filter: contrast(1.5);
    }
    &:active {
        filter: brightness(.9)contrast(1.5);
    }
}
.windows-icon {
    position: absolute;
    inset: 6px;

    &::after {
        content: '';
        position: absolute;
        background-image: var(--icon-gradient);
        mix-blend-mode: overlay;
        inset: 0;
        display: inline-block;
        z-index: 15;
    }
}
.icon-shadow {
    filter: drop-shadow(1px 2px 3px #000000)
}
</style>