<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Impacto do COVID-19 (2019-2023)</title>
<style>
/* === Reset e estilo base === */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}

body {
    background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
    color: #f0f0f0;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 40px 20px;
}

h1 {
    font-size: 2.5rem;
    margin-bottom: 40px;
    text-align: center;
    background: linear-gradient(90deg, #f7971e, #ffd200);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

/* === Container === */
.accordion-container {
    width: 100%;
    max-width: 900px;
}

/* === Gavetas de texto === */
.accordion {
    background: rgba(255, 255, 255, 0.05);
    margin-bottom: 15px;
    border-radius: 15px;
    overflow: hidden;
    backdrop-filter: blur(10px);
    box-shadow: 0 8px 20px rgba(0,0,0,0.4);
    transition: transform 0.3s ease;
}

.accordion:hover {
    transform: translateY(-3px);
}

.accordion-header {
    padding: 20px 25px;
    font-size: 1.2rem;
    font-weight: 600;
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    align-items: center;
    transition: background 0.3s, color 0.3s;
    background: linear-gradient(135deg, #ff416c, #ff4b2b);
    border-radius: 15px 15px 0 0;
}

.accordion-header:hover {
    background: linear-gradient(135deg, #ff6a88, #ff8e53);
}

.accordion-content {
    max-height: 0;
    overflow: hidden;
    padding: 0 25px;
    background: rgba(255,255,255,0.05);
    backdrop-filter: blur(5px);
    transition: max-height 0.5s ease, padding 0.3s ease;
}

.accordion-content p {
    padding: 20px 0;
    line-height: 1.7;
    font-size: 1rem;
}

/* Sinal de abrir/fechar */
.accordion-header::after {
    content: '+';
    font-size: 1.5rem;
    transition: transform 0.3s ease;
}

.accordion.active .accordion-header::after {
    content: '-';
}

.accordion.active .accordion-content {
    padding: 20px 25px;
    max-height: 500px;
}

/* === Animação suave na entrada === */
.accordion-content p {
    opacity: 0;
    transform: translateY(10px);
    animation: fadeIn 0.5s forwards;
}

.accordion.active .accordion-content p {
    animation-delay: 0.2s;
}

@keyframes fadeIn {
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* === Responsividade === */
@media (max-width: 600px) {
    h1 {
        font-size: 2rem;
    }
    .accordion-header {
        font-size: 1rem;
        padding: 15px 20px;
    }
    .accordion-content p {
        font-size: 0.95rem;
    }
}
</style>
</head>
<body>

<h1>Como o COVID-19 Abalou o Mundo (2019-2023)</h1>

<div class="accordion-container">
    <div class="accordion">
        <div class="accordion-header">2019: Surgimento do COVID-19</div>
        <div class="accordion-content">
            <p>O coronavírus foi identificado pela primeira vez em Wuhan, China, causando casos de pneumonia viral. Inicialmente parecia um surto local, mas logo se espalhou pelo mundo.</p>
        </div>
    </div>

    <div class="accordion">
        <div class="accordion-header">2020: A Pandemia Global</div>
        <div class="accordion-content">
            <p>Em março de 2020, a OMS declarou pandemia. Lockdowns, quarentenas e restrições de viagens se tornaram globais. A economia sofreu forte impacto e sistemas de saúde ficaram sobrecarregados.</p>
        </div>
    </div>

    <div class="accordion">
        <div class="accordion-header">2021: Vacinas e Novas Variantes</div>
        <div class="accordion-content">
            <p>O início das vacinas trouxe esperança, mas variantes como Delta e Gamma aumentaram os desafios. Trabalho remoto, educação online e saúde mental viraram prioridades.</p>
        </div>
    </div>

    <div class="accordion">
        <div class="accordion-header">2022: Retomada Gradual</div>
        <div class="accordion-content">
            <p>Com vacinação em massa, muitas restrições foram suavizadas. Turismo e economia começaram a se recuperar, mas desigualdade de acesso às vacinas ainda gerou impacto desigual entre países.</p>
        </div>
    </div>

    <div class="accordion">
        <div class="accordion-header">2023: Legado e Reflexões</div>
        <div class="accordion-content">
            <p>O mundo passou a repensar políticas de prevenção de pandemias e valorizou ciência e tecnologia. Lições sociais, econômicas e de solidariedade global marcaram o período pós-pandemia.</p>
        </div>
    </div>
</div>

<script>
const accordions = document.querySelectorAll('.accordion');

accordions.forEach(acc => {
    acc.addEventListener('click', () => {
        acc.classList.toggle('active');
    });
});
</script>

</body>
</html>
