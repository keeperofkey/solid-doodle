<nav>
    <a href="/">Home</a>
    <a href="/install">Install</a>
</nav>

<slot />

<style>
    nav {
        background: #fff;
        padding: 1rem;
        border-radius: 0.5rem;
        box-shadow: 0 0.25rem 0.5rem rgba(0, 0, 0, 0.1);
    }

    nav a {
        color: #333;
        text-decoration: none;
        font-family: sans-serif;
        font-size: 1rem;
        font-weight: bold;
        padding: 0.5rem;
    }

    nav a:hover {
        background: #eee;
        border-radius: 0.25rem;
    }
</style>
