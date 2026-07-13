// Animação ao carregar a página
window.addEventListener("load", () => {
    document.querySelector(".container").style.opacity = "1";
});

// Efeito de clique nos botões
const botoes = document.querySelectorAll(".botao");

botoes.forEach(botao => {

    botao.addEventListener("mousedown", () => {
        botao.style.transform = "scale(.97)";
    });

    botao.addEventListener("mouseup", () => {
        botao.style.transform = "";
    });

    botao.addEventListener("mouseleave", () => {
        botao.style.transform = "";
    });

});

// Efeito ao mover o mouse na foto
const foto = document.querySelector(".foto");

foto.addEventListener("mousemove", () => {
    foto.style.transform = "scale(1.05) rotate(2deg)";
});

foto.addEventListener("mouseleave", () => {
    foto.style.transform = "scale(1)";
});

// Rolagem suave caso adicione mais seções futuramente
document.querySelectorAll("a").forEach(link => {
    link.addEventListener("click", function () {
        document.body.style.opacity = "0.98";
        setTimeout(() => {
            document.body.style.opacity = "1";
        }, 150);
    });
});
