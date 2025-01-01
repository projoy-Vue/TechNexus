<template>
    <nav class="navbar">
        <!-- Logo -->
        <div class="logo">
            <a href="/">TechNexus</a>
        </div>

        <!-- Hamburger Menu Icon (Mobile) -->
        <div class="hamburger" @click="toggleMenu">
            <i :class="isMenuOpen ? 'fas fa-times' : 'fas fa-bars'"></i>
        </div>

        <!-- Navigation Links -->
        <ul :class="{ 'nav-active': isMenuOpen }" class="nav-links">
            <li><a href="/">Home</a></li>
            <li class="dropdown">
               <RouterLink to="/services">Services</RouterLink>
                <!-- Dropdown for Services -->
                <ul class="dropdown-content">
                    <li><a href="#">Managed IT Services</a></li>
                    <li><a href="#">Cybersecurity</a></li>
                    <li><a href="#">Cloud Solutions</a></li>
                    <li><a href="#">Software Development</a></li>
                </ul>
            </li>
            <li><a href="#">Industries</a></li>
            <li><RouterLink to="/CaseStudies">Resources</RouterLink></li>
            <li class="dropdown">
                <a href="#"> Resources </a>
                <!-- Dropdown for Resources -->
                <ul class="dropdown-content grid">
                    <div class="grid-item">
                        <div class="col">
                            <h4>Insights</h4>
                            <li><a href="#">Latest IT Insights</a></li>
                            <li><a href="#">Cybersecurity Tips</a></li>
                            <li><a href="#">Cloud Migration Guide</a></li>
                        </div>
                        <div class="col">
                            <h4>Downloadable Content</h4>
                            <li><a href="#">Blog</a></li>
                            <li><a href="#">White Papers</a></li>
                            <li><a href="#">Podcasts</a></li>
                        </div>
                    </div>
                </ul>
            </li>
            <li><a href="#">About Us</a></li>
            <li class="dropdown">
                <a href="#">Contact</a>
                <!-- Dropdown for Contact -->
                <ul class="dropdown-content grid">
                    <div class="grid-item">
                        <div class="col">
                            <h4>Address</h4>
                            <li><a href="#">TechNexus Solutions, 123 IT Park Ave, City, Country</a></li>
                        </div>
                        <div class="col">
                            <h4>Phone</h4>
                            <li><a href="#">+1 123-456-7890</a></li>
                        </div>
                        <div class="col">
                            <h4>Email</h4>
                            <li><a href="mailto:XKqXw@example.com">XKqXw@example.com</a></li>
                        </div>
                    </div>
                </ul>
            </li>
        </ul>

        <!-- CTA Button -->
        <a class="cta-btn" href="#">Get a Free Consultation</a>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            isMenuOpen: false,
        };
    },
    methods: {
        toggleMenu() {
            this.isMenuOpen = !this.isMenuOpen;
        },
    },
};
</script>

<style scoped>
/* Navbar Base Styles */
ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 30px;
    background-color: #1e1e1e;
    color: white;
    font-family: 'Arial', sans-serif;
    position: relative;
}

.logo a {
    color: white;
    font-size: 1.7rem;
    font-weight: bold;
    text-decoration: none;
}

/* CTA Button */
.cta-btn {
    background-color: #ff6b6b;
    color: white;
    padding: 10px 20px;
    border-radius: 5px;
    text-decoration: none;
    transition: background-color 0.3s ease;
    font-size: 1.1rem;
}

.cta-btn:hover {
    background-color: #ff5252;
}

/* Hamburger Menu (Mobile) */
.hamburger {
    display: none;
    cursor: pointer;
    font-size: 1.8rem;
}

.fas.fa-times,
.fas.fa-bars {
    color: white;
}

/* Navigation Links */
.nav-links {
margin-left: 40px;
    display: flex;
    list-style: none;
    gap: 20px;
    align-items: center;
    transition: transform 0.3s ease;
}

.nav-links li {
    position: relative;
}

.nav-links a {
    color: white;
    text-decoration: none;
    font-size: 1.1rem;
    padding: 8px;
    transition: color 0.3s ease;
}

.nav-links a:hover {
    color: #ff6b6b;
}

/* Dropdown Menu */
.dropdown-content {
    display: none;
    position: absolute;
    top: 100%;
    left: 0;
    background-color: #333;
    padding: 15px;
    border-radius: 5px;
    min-width: 300px;
    z-index: 1000;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.dropdown:hover .dropdown-content {
    display: block;
}

.grid-item {
    width: 500px;
    display: flex;
    gap: 20px;
}

.dropdown-content li {
    margin-bottom: 10px;
}

.dropdown-content a {
    color: white;
    display: block;
    padding: 8px 10px;
    transition: background-color 0.3s ease;
    font-size: 0.8rem;
}

.dropdown-content a:hover {
    background-color: #444;
}

/* Grid Layout for Dropdowns */
.grid {
    display: flex;
    gap: 30px;
}

.col {
    flex: 1;
}

.col h4 {
    color: #ff6b6b;
    margin-bottom: 10px;
}

/* Responsive Design for Mobile */
@media (max-width: 768px) {
    .hamburger {
        display: block;
    }
.grid-item{
    display: none;
}
    .nav-links {
        position: absolute;
        top: 60px;
        right: 0;
        width: 100%;
        height: calc(100vh - 60px);
        background-color: #b42e2e;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        transform: translateX(100%);
        transition: transform 0.3s ease-in-out;
        z-index: 999;
    }

    .nav-links.nav-active {
        transform: translateX(0);
    }

    .nav-links li {
        margin: 20px 0;
    }

    .cta-btn {
        display: none;
    }

    .dropdown-content {
        position: static;
        padding: 0;
        box-shadow: none;
        min-width: unset;
    }

    .dropdown-content li {
        margin-bottom: 5px;
    }
}

/* Responsive Design for Larger Screens */
@media (min-width: 769px) {
    .nav-links {
        justify-content: flex-end;
    }

    .dropdown-content {
        display: none;
        position: absolute;
        top: 100%;
        left: 0;
        background-color: #333;
        padding: 10px 15px;
        border-radius: 5px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    }

    /* .dropdown:hover .dropdown-content {
        display: block;
    } */

    .dropdown-content li {
        margin-bottom: 10px;
    }

    .cta-btn {
        margin-left: auto;
    }
}
</style>