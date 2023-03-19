<script>

export default {
    name: 'ProjectCard',
    props: { project: Object }
};
</script>

<template>
    <main class="container">
        <div class="card my-5">
            <div class="card-header">
                <h3>{{ project.title }}</h3>
            </div>
            <div class="card-body">
                <p>{{ project.content }}</p>
            </div>
            <div class="card-footer d-flex justify-content-between align-items-center">
                <div>
                    <span class="me-3">{{ project.category.label }}</span>
                    <span>{{ project.lenguages[0].label }}</span>
                </div>
                <RouterLink :to="{ name: 'show', params: { id: project.id } }" class="btn btn-primary">vedi</RouterLink>
            </div>
        </div>
    </main>
</template>