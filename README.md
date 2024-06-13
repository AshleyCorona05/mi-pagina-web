# mi-pagina-web
document.addEventListener("DOMContentLoaded", function() {
    const links = document.querySelectorAll("nav ul li a");
    const sections = document.querySelectorAll("section");

    links.forEach(link => {
        link.addEventListener("click", function(event) {
            event.preventDefault();
            const targetId = this.getAttribute("href").substring(1);
            sections.forEach(section => {
                if (section.getAttribute("id") === targetId) {
                    section.scrollIntoView({ behavior: "smooth" });
                }
            });
        });
    });
});
