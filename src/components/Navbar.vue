<template>
    <header class="header" id="header">
        <nav class="nav container">
            <a href="#" class="nav__logo">
                <i class="ri-leaf-line nav__logo-icon"></i> Baghicha
            </a>

            <div class="nav__menu" id="nav-menu">
                <ul class="nav__list">
                    <li class="nav__item" @click="assignActive(1)">
                        <a href="#home" class="nav__link active-link">Home</a>
                    </li>
                    <li class="nav__item" @click="assignActive(2)">
                        <a href="#about" class="nav__link">About</a>
                    </li>
                    <li class="nav__item" @click="assignActive(3)">
                        <a href="#products" class="nav__link">Products</a>
                    </li>
                    <li class="nav__item" @click="assignActive(4)">
                        <a href="#faqs" class="nav__link">FAQs</a>
                    </li>
                    <li class="nav__item" @click="assignActive(5)">
                        <a href="#contact" class="nav__link">Contact Us</a>
                    </li>
                </ul>

                <div class="nav__close" @click="hideMobileMenu" id="nav-close">
                    <i class="ri-close-line"></i>
                </div>
            </div>

            <div class="nav__btns">
                <!-- Theme change button -->
                <i class="ri-moon-line change-theme" id="theme-button"></i>

                <div class="nav__toggle" @click="showMobileMenu" id="nav-toggle">
                    <i class="ri-menu-line"></i>
                </div>
            </div>
        </nav>
    </header>
</template>

<script setup>

    let previousActive = 1;

    function showMobileMenu() {
        const navMenu = document.getElementById('nav-menu');
        navMenu.classList.add('show-menu');
    }

    function hideMobileMenu() {
        const navMenu = document.getElementById('nav-menu');
        navMenu.classList.remove('show-menu');
    }

    const navLink = document.querySelectorAll('.nav__link')

    function linkActionForMobile(){
        const navMenu = document.getElementById('nav-menu');
        navMenu.classList.remove('show-menu');
    }

    function assignActive(id) {
        if (id != this.previousActive) {
            const elements = document.getElementsByClassName('nav__link');
            if (document.getElementsByClassName('active-link')) {
                for(let el of elements) {
                    if (el.classList.contains('active-link')) {
                        el.classList.remove('active-link');
                    }
                }
            }
            elements[id-1].classList.add('active-link');
            this.previousActive = id;
        }
        this.linkActionForMobile();
    }

</script>
