<script>
    import { onMount } from "svelte";

    let displayTime;

    function getCurrentTime() {
    const now = new Date();
    let hours = now.getHours();
    let minutes = now.getMinutes();
    const ampm = hours >= 12 ? "PM" : "AM";
    hours = hours % 12;
    hours = hours ? hours : 12;
    minutes = minutes < 10 ? "0" + minutes : minutes;
    return `${hours}:${minutes} ${ampm}`;
    }

    function updateTime() {
    const currentTime = getCurrentTime();
    displayTime.innerHTML = currentTime;
    }

    onMount(() => {
    displayTime = document.querySelector(".clock");
    updateTime();
    setInterval(updateTime, 1000);
    });
</script>

<span class="clock" />

<style lang="scss">
.clock {
    position: absolute;
    font: var(--font);
    color: #ffffff;
    right: 15px;
    top: 20%;
    cursor: default;
}
</style>