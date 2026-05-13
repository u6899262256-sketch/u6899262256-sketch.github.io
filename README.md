<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>0x99_ | Discord & Minecraft Developer</title>
    <style>
        :root {
            --primary: #5865F2;
            --bg-dark: #23272a;
            --bg-darker: #1e2124;
            --text-white: #ffffff;
            --text-gray: #b9bbbe;
            --accent: #faa61a;
            --success: #3ba55c;
        }

        body {
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background-color: var(--bg-darker);
            color: var(--text-white);
            margin: 0;
            line-height: 1.6;
        }

        header {
            background: linear-gradient(rgba(0,0,0,0.8), rgba(0,0,0,0.8)), url('https://images.unsplash.com/photo-1614850523296-d8c1af93d400?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            height: 250px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            border-bottom: 4px solid var(--primary);
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 20px;
        }

        .profile-badge {
            background: var(--primary);
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: bold;
            text-transform: uppercase;
        }

        h1 { font-size: 2.8rem; margin: 10px 0; letter-spacing: 1px; }
        
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 25px;
            margin-top: 40px;
        }

        .card {
            background: var(--bg-dark);
            padding: 25px;
            border-radius: 12px;
            border: 1px solid #36393f;
            transition: all 0.3s ease;
            display: flex;
            flex-direction: column;
        }

        .card:hover { 
            transform: translateY(-8px); 
            border-color: var(--primary);
            box-shadow: 0 10px 20px rgba(0,0,0,0.4);
        }

        /* --- SISTEMA DE MULTI-IMAGEN (SLIDER) --- */
        .slider-container {
            position: relative;
            width: 100%;
            height: 200px;
            margin-bottom: 15px;
            overflow: hidden;
            border-radius: 8px;
            border: 1px solid #4f545c;
            background-color: #1a1c1e;
        }

        .slider-wrapper {
            display: flex;
            transition: transform 0.4s ease-in-out;
            height: 100%;
        }

        .slider-wrapper img {
            min-width: 100%;
            height: 100%;
            object-fit: contain;
            cursor: zoom-in;
        }

        .slider-btn {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            background: rgba(0,0,0,0.6);
            color: white;
            border: none;
            padding: 8px 12px;
            cursor: pointer;
            z-index: 10;
            border-radius: 4px;
        }

        .slider-btn:hover { background: var(--primary); }
        .prev { left: 5px; }
        .next { right: 5px; }

        /* --- SECCIÓN DE FEEDBACK --- */
        .feedback-section {
            margin-top: 60px;
            background: var(--bg-dark);
            padding: 30px;
            border-radius: 12px;
            border: 1px solid #36393f;
        }

        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .testimonial-card {
            background: #2f3136;
            padding: 15px;
            border-radius: 8px;
            border-left: 4px solid var(--success);
        }

        .testimonial-user {
            color: var(--accent);
            font-weight: bold;
            font-size: 0.9rem;
            margin-bottom: 5px;
            display: block;
        }

        .tag {
            background: #2f3136;
            color: var(--accent);
            padding: 4px 10px;
            border-radius: 4px;
            font-size: 0.85rem;
            margin-right: 5px;
            font-family: 'Courier New', Courier, monospace;
            border: 1px solid rgba(250, 166, 26, 0.2);
        }

        .contact-box {
            background: linear-gradient(135deg, var(--primary), #4752c4);
            text-align: center;
            padding: 50px;
            border-radius: 20px;
            margin-top: 60px;
        }

        .btn {
            display: inline-block;
            background: white;
            color: var(--primary);
            padding: 12px 30px;
            border-radius: 8px;
            text-decoration: none;
            font-weight: bold;
            margin: 15px 10px;
            transition: 0.2s;
        }

        .btn:hover { transform: scale(1.05); }

        /* Estilos del Modal */
        #imageModal {
            display: none;
            position: fixed;
            z-index: 9999;
            top: 0; left: 0;
            width: 100%; height: 100%;
            background: rgba(0,0,0,0.92);
            align-items: center;
            justify-content: center;
            cursor: pointer;
        }

        #modalImg {
            max-width: 90%;
            max-height: 85%;
            border: 2px solid var(--primary);
            border-radius: 10px;
        }

    </style>
</head>
<body>

<header>
    <div>
        <span class="profile-badge">Developer & Configurador</span>
        <h1>0x99_</h1>
        <p style="font-size: 1.1rem; color: #dcddde;">Soluciones profesionales para Discord y Minecraft</p>
    </div>
</header>

<div class="container">
    
    <section class="grid">
        <div class="card">
            <h2>🛠️ Habilidades</h2>
            <ul style="list-style: none; padding: 0;">
                <li style="margin-bottom: 10px;">↪ Configuración de <strong>servidores, Proxy , Bungee Etc.</strong>.</li>
                <li style="margin-bottom: 10px;">↪ Desarrollo de <strong>Bots</strong> en Py/JS.</li>
                <li style="margin-bottom: 10px;">↪ Gestión avanzada de <strong>YAML, JavaScript </strong>.</li>
                <li style="margin-bottom: 10px;">↪ Optimizacion de plugins , Configuraciones Unicas , Sistemas etc.</li>
            </ul>
            <div style="margin-top: auto; padding-top: 20px;">
                <span class="tag">Python</span><span class="tag">JS</span><span class="tag">YAML</span>
            </div>
        </div>

        <div class="card">
            <h2>🚀 Bots Personalizados</h2>
            <div class="slider-container" id="slider1">
                <div class="slider-wrapper">
                    <img src="bot de candymc.png" alt="CandyMC 1" class="project-img">
                    <img src="logstickets.png" class="project-img">
                </div>
                <button class="slider-btn prev" onclick="moveSlide('slider1', -1)">&#10094;</button>
                <button class="slider-btn next" onclick="moveSlide('slider1', 1)">&#10095;</button>
            </div>
            <p>Bot oficial con gestión de tickets, base de datos y paneles personalizados.</p>
        </div>

        <div class="card">
            <h2>🎮 Minecraft GUI & Configs</h2>
            <div class="slider-container" id="slider2">
                <div class="slider-wrapper">
                    <img src="image-193.png" alt="Vegas 1" class="project-img">
                    <img src="rankups.png" class="project-img">
                </div>
                <button class="slider-btn prev" onclick="moveSlide('slider2', -1)">&#10094;</button>
                <button class="slider-btn next" onclick="moveSlide('slider2', 1)">&#10095;</button>
            </div>
            <p>Diseño de menús interactivos, sistemas de Rankups y optimización de configuraciones.</p>
        </div>
    </section>

<section class="feedback-section">
        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 40px;">
            
            <div>
                <h2>⭐ Reseñas de Clientes</h2>
                <div class="testimonial-grid" style="grid-template-columns: 1fr;">
                    <div class="testimonial-card">
                        <span class="testimonial-user">@OjoLatam Network</span>
                        <p>"Excelente trabajo con la configuración del servidor, todo muy ordenado."</p>
                    </div>
                    <div class="testimonial-card">
                        <span class="testimonial-user">@CandyMC_Admin</span>
                        <p>"El bot de tickets funciona a la perfección. 100% recomendado."</p>
                    </div>
                </div>
            </div>

            <div class="card" style="border-color: var(--success); background: #2f3136;">
                <h3>✍️ Deja tu Feedback</h3>
                <form action="https://formspree.io/f/xlgoerdy" method="POST" style="display: flex; flex-direction: column; gap: 10px;">
                    <label style="font-size: 0.8rem; color: var(--text-gray);">Tu Usuario de Discord o Nombre:</label>
                    <input type="text" name="name" placeholder="@TuUsuario" required 
                           style="padding: 10px; border-radius: 5px; border: none; background: #1e2124; color: white;">
                    
                    <label style="font-size: 0.8rem; color: var(--text-gray);">Tu Reseña:</label>
                    <textarea name="message" rows="4" placeholder="¿Qué te pareció el servicio?" required
                              style="padding: 10px; border-radius: 5px; border: none; background: #1e2124; color: white; resize: none;"></textarea>
                    
                    <button type="submit" class="btn" style="margin: 10px 0; background: var(--success); color: white; cursor: pointer; border: none;">
                        Enviar Reseña
                    </button>
                </form>
            </div>

        </div>
    </section>

    <section class="contact-box">
        <h2>¿Necesitas un developer?</h2>
        <p><strong>Discord ID:</strong> 0x99_
    </section>

</div>

<footer style="text-align: center; padding: 40px; color: var(--text-gray); font-size: 0.8rem;">
    &copy; 2026 0x99_ | Portafolio Profesional
</footer>

<div id="imageModal" onclick="this.style.display='none'">
    <img id="modalImg" alt="Ampliación">
</div>

<script>
    // --- Lógica del Slider ---
    const slideStates = {};

    function moveSlide(sliderId, direction) {
        const slider = document.getElementById(sliderId);
        const wrapper = slider.querySelector('.slider-wrapper');
        const imagesCount = wrapper.querySelectorAll('img').length;
        
        if (!slideStates[sliderId]) slideStates[sliderId] = 0;
        
        slideStates[sliderId] += direction;

        if (slideStates[sliderId] >= imagesCount) slideStates[sliderId] = 0;
        if (slideStates[sliderId] < 0) slideStates[sliderId] = imagesCount - 1;

        const offset = slideStates[sliderId] * -100;
        wrapper.style.transform = `translateX(${offset}%)`;
    }

    // --- Lógica del Lightbox (Zoom) ---
    const modal = document.getElementById('imageModal');
    const modalImg = document.getElementById('modalImg');

    document.querySelectorAll('.project-img').forEach(img => {
        img.onclick = function(e) {
            e.stopPropagation(); // Evita que el click pase al slider
            modal.style.display = "flex";
            modalImg.src = this.src;
        }
    });
</script>

</body>
</html>
