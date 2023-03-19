<script>
export default {
    name: 'AppHeader'
};
</script>

<template>
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container-fluid">
            <span class="navbar-brand" href="#">Portfolio</span>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item d-flex">
                        <RouterLink to="/" class="nav-link">Home</RouterLink>
                        <RouterLink to="/project/:id" class="nav-link">Project</RouterLink>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>