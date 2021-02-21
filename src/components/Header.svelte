<script>
    export let name = '';

    let selected = false;
    const navItems = ['Dashboard', 'Settings'];

    function selectNavItem(navItem) {
        name = navItem;
        selected = false;
    }
</script>

<style>
    .header {
        background-color: #0d0e10;
        box-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        padding: 8px;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 42px;
        z-index: 99;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .header .nav-toggle {
        text-align: center;
        font-weight: bolder;
        background-color: transparent;
        border: 0;
        border-radius: 4px;
        margin-right: 8px;
        width: 32px;
        height: 32px;
        transition: all;
        transition-duration: 300ms;
    }
    .header .nav-toggle:hover, .header .nav-toggle.selected {
        background-color: #0d86ff;
        cursor: pointer;
    }
    .header .nav-toggle.selected {
        transform: rotate(90deg);
    }
    .header h1 {
        font-weight: normal;
        font-size: 24px;
    }
    .navigation-items {
        position: absolute;
        top: 42px;
        margin-top: -142px;
        left: 0;
        background-color: #000;
        width: 100%;
        padding: 8px;
        z-index: 98;
        transition: all;
        transition-duration: 300ms;
    }
    .navigation-items.selected {
        margin-top: 0;
    }
    .navigation-items .navigation-item {
        padding: 8px;
        font-size: 18px;
        width: 100%;
        border-radius: 4px;
        margin: 8px 0;
    }
    .navigation-items .navigation-item:hover, .navigation-items .navigation-item.selected {
        background-color: #0d86ff;
        cursor: pointer;
    }
</style>

<div class="header">
    <button class="nav-toggle" class:selected on:click={() => selected = !selected}>| | |</button> <h1>{name}</h1>
</div>
<div class="navigation-items" class:selected>
    {#each navItems as navItem}
        <div class="navigation-item" class:selected={name === navItem} on:click={() => {selectNavItem(navItem)}}>{navItem}</div>
    {/each}
</div>