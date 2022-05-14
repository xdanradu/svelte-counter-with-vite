<script lang="ts">
    import axios from 'axios';

    let posts = [];
    const getData = () => {
        axios.get('https://jsonplaceholder.typicode.com/posts').then(
            results => {
                posts = results.data;
            }
        );
    }
</script>

<button on:click={getData}>Get posts from mock server
</button>

<ul>
    {#each posts as post}
        <li>
            {post.title}
        </li>
    {/each}
</ul>
