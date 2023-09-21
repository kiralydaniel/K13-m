<template>
    <div>
        <Navbar></Navbar>

        <div class="container mx-auto p-4">
            <slot/>
        </div>
        <ScrollToTopButton></ScrollToTopButton>
        <Footer></Footer>
    </div>
</template>

