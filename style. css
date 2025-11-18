// Hamburger Menu Toggle
const hamburger = document.querySelector(".hamburger");
const navLinks = document.querySelector(".nav-links");

hamburger.addEventListener("click", () => {
  navLinks.classList.toggle("active");
});

// Active Section Highlight & Scroll Fade-in
const sections = document.querySelectorAll("section");
const options = {
  threshold: 0.3
};
const observer = new IntersectionObserver(function(entries, observer){
  entries.forEach(entry => {
    if(entry.isIntersecting){
      entry.target.classList.add("show");
      const id = entry.target.getAttribute("id");
      document.querySelectorAll("nav a").forEach(link => {
        link.classList.remove("active-link");
        if(link.getAttribute("href").includes(id)){
          link.classList.add("active-link");
        }
      });
    }
  });
}, options);

sections.forEach(section => {
  observer.observe(section);
});
