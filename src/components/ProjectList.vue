<script>

export default {
    name: 'ProjectList',
    props: { projects: Array }
};
</script>

<template>
    <main class="container">
        <div class="my-5">
            <ul>
                <li v-for="project in projects" :kay="project.id">
                    {{ project.title }}
                </li>
            </ul>
        </div>
    </main>
</template>