<nav>
    <a href="/">Home</a>
    <a href="/install">Install</a>
    <a href="/joya">Joya</a>
</nav>

<slot />

<style>
    nav {
        background: #fff;
        padding: 1rem;
        border-radius: 0.5rem;
        box-shadow: 0 0.25rem 0.5rem rgba(0, 0, 0, 0.1);
        position: fixed;
    }

    nav a {
        color: #333;
        text-decoration: none;
        font-family: monospace;
        font-size: 1rem;
        font-weight: bold;
        padding: 0.5rem;
    }

    nav a:hover {
        background: #eee;
        border-radius: 0.25rem;
    }
</style>
