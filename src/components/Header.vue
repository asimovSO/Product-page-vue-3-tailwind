<template>
    <header class="header container flex justify-between items-center py-7 border-b border-dashed border-slate-400">
        <div class="cursor-pointer">
            <img src="/img/logo.png" alt="Logo">
        </div>
        <div class="flex items-center gap-6">
            <div class="search">
                <img src="/icons/search.svg" alt="search">
            </div>
            <div class="categories hidden md:block">
                <span>Categories</span>
            </div>
            <div class="auth md:flex items-center gap-2 hidden">
                <img src="/icons/profile.svg" alt="I">
                <span>Sign in</span>
            </div>
            <div class="favorites hidden md:block">
                <img src="/icons/heart.svg" alt="Favorite">
            </div>
            <div class="cart">
                <img src="/icons/cart.svg " alt="Cart" >
            </div>
            <div class="burger md:hidden">
                <img src="/icons/burger.svg" alt="Menu">
            </div>
        </div>
    </header>
</template>
<style scoped>
.header > * {
    cursor: pointer;
}
</style>