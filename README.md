<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>El Método Oribio</title>
    <link rel="stylesheet" href="styles/theme.css">
    <link rel="stylesheet" href="styles/components.css">
    <link rel="stylesheet" href="styles/layouts.css">
    <style>
        body {
            overflow: hidden;
            background: #000;
        }
        .slide-deck {
            position: relative;
            width: 100vw;
            height: 100vh;
        }
        .slide {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0;
            pointer-events: none;
            transition: opacity 0.6s ease;
            background: var(--color-marble);
        }
        .slide.active {
            opacity: 1;
            pointer-events: all;
            z-index: 10;
        }
        .nav-controls {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            z-index: 100;
            display: flex;
            gap: 1rem;
        }
        .nav-btn {
            background: rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(0, 0, 0, 0.1);
            color: var(--color-black-soft);
            cursor: pointer;
            padding: 0.5rem 1rem;
            border-radius: 20px;
            font-family: var(--font-body);
            font-size: 0.8rem;
            text-transform: uppercase;
            transition: all 0.2s;
            backdrop-filter: blur(5px);
        }
        .nav-btn:hover {
            background: var(--color-black-soft);
            color: white;
        }
        .slide-counter {
            position: fixed;
            bottom: 2.5rem;
            right: 14rem;
            /* Positioned to the left of nav controls */
            z-index: 100;
            font-family: var(--font-body);
            font-size: 0.8rem;
            color: var(--color-taupe);
        }
        .brand-logo {
            position: fixed;
            bottom: 2rem;
            left: 2rem;
            z-index: 100;
            width: 120px;
            /* Adjust based on actual logo aspect ratio */
            height: auto;
        }
    </style>
</head>
<body>
    <div class="grain-overlay"></div>
    <div class="atelier-line"></div>
    <!-- Logo Container -->
    <!-- logo removed (placeholder deleted to prepare final asset insertion) -->
    <div class="slide-deck">
        <!-- SLIDE 1: WELCOME (Split Hero) -->
        <div class="slide active" id="slide-1">
            <div class="slide-container layout-split">
                <div class="split-content">
                    <h2 class="hero-subtitle">Una enseñanza para volver a la textura</h2>
                    <h1 class="hero-title">El Método<br><i
                            style="font-family: var(--font-body); color: var(--color-olive); font-weight: 700;">Oribio</i></h1>
                    <p class="body-text-lg" style="margin-top: 2rem;">
                        Un ritual simple. Una compañía real. Un journey que se sostiene. No empieza con comprar, empieza
                        con entender.
                    </p>
                </div>
                <div class="split-media">
                    <div
                        style="width: 100%; height: 100%; background: #E8DCC8; display: flex; align-items: center; justify-content: center; overflow: hidden;">
                        <img src="hero-texture.png" alt="Textura Oribio"
                            style="width: 100%; height: 100%; object-fit: cover;">
                    </div>
                </div>
            </div>
        </div>
        <!-- SLIDE 2: MANIFESTO (Full Bleed) -->
        <div class="slide" id="slide-2">
            <div class="slide-container layout-manifesto">
                <h2 class="hero-subtitle" style="color: var(--color-olive);">La Verdad Incómoda</h2>
                <h1 style="font-size: 3.5rem; line-height: 1.2; max-width: 900px; margin: 0 auto 2rem;">
                    Amar tu pelo no se logra de un día al otro.<br>
                    <span style="font-style: italic; color: var(--color-taupe);">No es falta de disciplina. Es falta de
                        método.</span>
                </h1>
                <p class="body-text-lg" style="margin: 0 auto;">
                    Necesitas productos funcionales y el acompañamiento de una marca que cree en lo que ya tienes.
                </p>
            </div>
        </div>
        <!-- SLIDE 3: COMPARISON (Oribio vs Others) - Split Screen with aligned top titles -->
        <div class="slide" id="slide-3">
            <div class="slide-container layout-split-compare">
                <div class="split-titles">
                    <div class="left-title">
                        <h1 style="font-size:1.8rem; margin:0; color:var(--color-olive);">La diferencia no está en los tipos de cabellos o en las necesidades.</h1>
                    </div>
                    <div class="right-title">
                        <!-- right title intentionally left empty; title will appear inside the method card for centered alignment -->
                    </div>
                </div>
                <div class="others">
                    <span class="col-header" style="color: #666; border-color: #ccc;">Otros</span>
                    <h3 style="font-size:1.2rem; margin:0.5rem 0; color:#666; font-weight:700;">Producto suelto</h3>
                    <ul class="chaos-list">
                        <li><strong>Sin momento:</strong> no hay intención clara.</li>
                        <li><strong>Sin dosis:</strong> pesa o no alcanza (ensayo y error).</li>
                        <li><strong>Sin guía:</strong> acumulación de productos sin orden.</li>
                    </ul>
                    <div style="margin-top: 1.2rem;">
                        <div style="position: relative; height: 160px; border: 1px dashed #999; display: flex; align-items: center; justify-content: center; background: transparent;">
                            <span style="font-size: 3rem; color: #ccc;">?</span>
                        </div>
                        <p style="text-align: left; font-size: 0.95rem; margin-top: 1rem; color: #888;">Frustración y desperdicio: los clientes prueban y abandonan, sin ritual ni resultados consistentes.</p>
                    </div>
                </div>
                <div class="method">
                    <h2 class="panel-title">El Método ORIBIO</h2>
                    <p style="font-style: italic; color: var(--color-olive); font-size:1.03rem; margin-top:0;">Es el método integral de productos funcionales con una marca sensorial.</p>
                    <hr style="border:none; height:1px; background: var(--color-taupe-border); margin:0.8rem 0 1rem 0; opacity:0.6;">
                    <h3 style="font-size:1rem; color: var(--color-olive); margin:0 0 0.6rem 0; font-weight:700;">Receta por momentos</h3>
                    <div style="display:grid; grid-template-columns: 1fr; gap:0.6rem;">
                        <div class="recipe-card" style="padding: 0.9rem; border-left: 6px solid var(--color-olive);">
                            <div class="recipe-label">NOCTURNO</div>
                            <div class="recipe-intention" style="font-size: 0.95rem;">Restaurar mientras descansas</div>
                            <p style="font-size: 0.85rem; color: var(--color-taupe); margin: 0.3rem 0;">Fricción de almohada rompe la fibra</p>
                            <div class="dose-item"><span class="dose-label">Producto:</span> <span class="dose-value">Divine Miracle</span></div>
                            <div class="dose-item"><span class="dose-label">Dosis:</span> <span class="dose-value">4-6 gotas</span></div>
                        </div>
                        <div class="recipe-card" style="padding: 0.9rem; border-left: 6px solid var(--color-olive);">
                            <div class="recipe-label">LAVADO</div>
                            <div class="recipe-intention" style="font-size: 0.95rem;">Limpiar y preparar</div>
                            <p style="font-size: 0.85rem; color: var(--color-taupe); margin: 0.3rem 0;">Base limpia para el tratamiento</p>
                        </div>
                        <div class="recipe-card" style="padding: 0.9rem; border-left: 6px solid var(--color-olive);">
                            <div class="recipe-label">POST-LAVADO</div>
                            <div class="recipe-intention" style="font-size: 0.95rem;">Definir el patrón en húmedo</div>
                            <p style="font-size: 0.85rem; color: var(--color-taupe); margin: 0.3rem 0;">Fibra moldeable, momento clave</p>
                            <div class="dose-item"><span class="dose-label">Productos:</span> <span class="dose-value">Sublime + Lino Gel</span></div>
                            <div class="dose-item"><span class="dose-label">Dosis:</span> <span class="dose-value">14-16 gotas + 2-3 pumps</span></div>
                        </div>
                        <div class="recipe-card" style="padding: 0.9rem; border-left: 6px solid var(--color-olive);">
                            <div class="recipe-label">ENTRE-LAVADOS</div>
                            <div class="recipe-intention" style="font-size: 0.95rem;">Fortalecer sin lavar</div>
                            <p style="font-size: 0.85rem; color: var(--color-taupe); margin: 0.3rem 0;">Recuperar brillo y control</p>
                            <div class="dose-item"><span class="dose-label">Producto:</span> <span class="dose-value">Maximum Elixir</span></div>
                            <div class="dose-item"><span class="dose-label">Dosis:</span> <span class="dose-value">1-2 pumps</span></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- SLIDE 4: BUSINESS OPPORTUNITY (Dark Premium) -->
        <div class="slide" id="slide-business">
            <div class="slide-container layout-3col"
                style="background-color: var(--color-black-soft); color: var(--color-ivory);">
                <div style="text-align: center; margin-bottom: 4rem;">
                    <h2 class="hero-subtitle" style="color: var(--color-gold);">Oportunidad</h2>
                    <h1 style="font-size: 3.5rem; color: white;">El Método genera <span
                            style="color: var(--color-gold);">Resultados.</span></h1>
                </div>
                <div class="grid-3col" style="align-items: flex-start; text-align: center;">
                    <!-- Metric 1 -->
                    <div style="padding: 2rem; border: 1px solid var(--color-taupe); border-radius: 8px;">
                        <span
                            style="font-family: var(--font-body); font-size: 5rem; color: var(--color-gold); line-height: 1; display: block; margin-bottom: 1rem; font-weight: 700;">12%</span>
                        <h3 style="font-size: 1.2rem; margin: 0; font-weight: 700; color: white;">Tasa de Recompra</h3>
                        <p style="color: var(--color-sand); font-size: 0.9rem; margin-top: 0.5rem;">Fidelidad asegurada
                            por el hábito.</p>
                    </div>
                    <!-- Metric 2 -->
                    <div style="padding: 2rem; border: 1px solid var(--color-taupe); border-radius: 8px;">
                        <span
                            style="font-family: var(--font-body); font-size: 5rem; color: var(--color-gold); line-height: 1; display: block; margin-bottom: 1rem; font-weight: 700;">+120</span>
                        <h3 style="font-size: 1.2rem; margin: 0; font-weight: 700; color: white;">Reseñas Verificadas
                        </h3>
                        <p style="color: var(--color-sand); font-size: 0.9rem; margin-top: 0.5rem;">Validación social
                            real.</p>
                    </div>
                    <!-- Metric 3 -->
                    <div style="padding: 2rem; border: 1px solid var(--color-taupe); border-radius: 8px;">
                        <span
                            style="font-family: var(--font-body); font-size: 5rem; color: var(--color-gold); line-height: 1; display: block; margin-bottom: 1rem; font-weight: 700;">5%</span>
                        <h3 style="font-size: 1.2rem; margin: 0; font-weight: 700; color: white;">Engagement Rate</h3>
                        <p style="color: var(--color-sand); font-size: 0.9rem; margin-top: 0.5rem;">Comunidad activa y
                            leal.</p>
                    </div>
                </div>
            </div>
        </div>
        <!-- SLIDE 6: 3 MOMENTOS (3 Column) -->
        <div class="slide" id="slide-6">
            <div class="slide-container layout-3col">
                <div style="text-align: center; margin-bottom: 2rem;">
                    <h2 class="hero-subtitle">El Sistema</h2>
                    <h1 style="font-size: 3rem;">Los 3 Momentos<br><span
                            style="font-style: italic; color: var(--color-taupe);">Una ruta por momentos y necesidades,
                            no por reglas.</span></h1>
                </div>
                <div class="grid-3col">
                    <div class="recipe-card" style="height: 100%;">
                        <div class="recipe-label">MOMENTO 01</div>
                        <div class="recipe-intention">Nocturno</div>
                        <p class="recipe-meta" style="line-height:1.6;">Restaurar mientras descansas. Nutrición profunda
                            sin esfuerzo activo.</p>
                        <div class="recipe-result" style="margin-top: auto;">Reparación</div>
                    </div>
                    <div class="recipe-card" style="height: 100%;">
                        <div class="recipe-label">MOMENTO 02</div>
                        <div class="recipe-intention">Post-Lavado</div>
                        <p class="recipe-meta" style="line-height:1.6;">Sellar y definir. El momento crítico para
                            establecer la forma.</p>
                        <div class="recipe-result" style="margin-top: auto;">Definición</div>
                    </div>
                    <div class="recipe-card" style="height: 100%;">
                        <div class="recipe-label">MOMENTO 03</div>
                        <div class="recipe-intention">Entre-Lavados</div>
                        <p class="recipe-meta" style="line-height:1.6;">Brillo y control. Recuperar el "yo" en los días
                            intermedios.</p>
                        <div class="recipe-result" style="margin-top: auto;">Mantención</div>
                    </div>
                </div>
            </div>
        </div>
        <!-- SLIDE 7: NOCTURNO -->
        <div class="slide" id="slide-7">
            <div class="slide-container layout-split">
                <div class="split-media">
                    <div
                        style="width: 100%; height: 100%; background: #2F2F2F; display: flex; align-items: center; justify-content: center; color: white;">
                        <span class="text-caps">[IMG: Divine Miracle en mesa de noche]</span>
                    </div>
                </div>
                <div class="split-content" style="background: var(--color-ivory);">
                    <div class="moment-selector">
                        <div class="moment-item active">NOCTURNO</div>
                        <div class="moment-item">POST-LAVADO</div>
                        <div class="moment-item">ENTRE-LAVADOS</div>
                    </div>
                    <h2 class="hero-subtitle">Producto: Divine Miracle</h2>
                    <h1 style="font-size: 2.5rem; margin-bottom: 1.5rem;">Reparar y Proteger<br><span
                            style="font-style: italic;">mientras duermes.</span></h1>
                    <p style="margin-bottom: 2rem; color: var(--color-taupe);">
                        Esta rutina es necesaria por la fricción de la almohada, que rompe el patrón y despierta el
                        frizz. Necesitamos sellar para reparar la fibra durante la noche.
                    </p>
                    <div class="recipe-card"
                        style="width: 100%; max-width: 100%; box-shadow: none; border: 1px solid var(--color-taupe-border); background: white;">
                        <div class="dose-item">
                            <span class="dose-label">Dosis</span>
                            <span class="dose-value">4–6 Gotas (Todos los días)</span>
                        </div>
                        <div class="dose-item">
                            <span class="dose-label">Zona</span>
                            <span class="dose-value">Medios → Puntas</span>
                        </div>
                        <div class="dose-item">
                            <span class="dose-label">Gesto</span>
                            <span class="dose-value">Calienta en manos</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- SLIDE 8: POST-LAVADO -->
        <div class="slide" id="slide-8">
            <div class="slide-container layout-split">
                <div class="split-media">
                    <div
                        style="width: 100%; height: 100%; background: #E6E0D5; display: flex; align-items: center; justify-content: center; color: #555;">
                        <span class="text-caps">[IMG: Cabello Húmedo Definido]</span>
                    </div>
                </div>
                <div class="split-content" style="background: var(--color-ivory);">
                    <div class="moment-selector">
                        <div class="moment-item">NOCTURNO</div>
                        <div class="moment-item active">POST-LAVADO</div>
                        <div class="moment-item">ENTRE-LAVADOS</div>
                    </div>
                    <h2 class="hero-subtitle">Productos: Sublime + Lino Gel</h2>
                    <h1 style="font-size: 2.5rem; margin-bottom: 1.5rem;">Definir el Patrón<br><span
                            style="font-style: italic;">en húmedo.</span></h1>
                    <p style="margin-bottom: 2rem; color: var(--color-taupe);">
                        El momento en que la fibra está moldeable y delicada. Aquí es donde tenemos que definir la
                        forma.
                    </p>
                    <div class="recipe-card"
                        style="width: 100%; max-width: 100%; box-shadow: none; border: 1px solid var(--color-taupe-border); background: white;">
                        <div class="dose-item">
                            <span class="dose-label">Paso 1: Sublime Renovation</span>
                            <span class="dose-value">14-16 Gotas (Desenredar)</span>
                        </div>
                        <div class="dose-item">
                            <span class="dose-label">Paso 2: Lino Active Gel</span>
                            <span class="dose-value">2-3 Pumps (Definir)</span>
                        </div>
                        <div class="dose-item">
                            <span class="dose-label">Gesto</span>
                            <span class="dose-value">Scrunch (Ondas) / Recto (Liso)</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- SLIDE 9: ENTRE-LAVADOS -->
        <div class="slide" id="slide-9">
            <div class="slide-container layout-split">
                <div class="split-media">
                    <div
                        style="width: 100%; height: 100%; background: #DAB255; display: flex; align-items: center; justify-content: center; color: white;">
                        <span class="text-caps">[IMG: Manos aplicando en seco]</span>
                    </div>
                </div>
                <div class="split-content" style="background: var(--color-ivory);">
                    <div class="moment-selector">
                        <div class="moment-item">NOCTURNO</div>
                        <div class="moment-item">POST-LAVADO</div>
                        <div class="moment-item active">ENTRE-LAVADOS</div>
                    </div>
                    <h2 class="hero-subtitle">Producto: Maximum Elixir</h2>
                    <h1 style="font-size: 2.5rem; margin-bottom: 1.5rem;">Fortalecer y Proteger<br><span
                            style="font-style: italic;">sin lavar.</span></h1>
                    <p style="margin-bottom: 2rem; color: var(--color-taupe);">
                        El clima y el roce apagan la forma. No necesitas lavar, necesitas crear barreras protectoras
                        (anti-humedad) y fortalecer.
                    </p>
                    <div class="recipe-card"
                        style="width: 100%; max-width: 100%; box-shadow: none; border: 1px solid var(--color-taupe-border); background: white;">
                        <div class="dose-item">
                            <span class="dose-label">Dosis</span>
                            <span class="dose-value">1-2 Pumps</span>
                        </div>
                        <div class="dose-item">
                            <span class="dose-label">Zona</span>
                            <span class="dose-value">Puntas y áreas con frizz</span>
                        </div>
                        <div class="dose-item">
                            <span class="dose-label">Gesto</span>
                            <span class="dose-value">Scrunch suave o alisado manual</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- SLIDE 12: DARK PREMIUM -->
        <div class="slide" id="slide-12">
            <div class="slide-container layout-dark layout-split">
                <div class="split-content">
                    <h2 class="hero-subtitle text-gold">Voces del Método</h2>
                    <h1 class="hero-title" style="color: var(--color-ivory);">Resultados<br><span
                            style="font-style: italic;">Humanos.</span></h1>
                    <figure style="margin-top: 3rem;">
                        <blockquote
                            style="font-family: var(--font-body); font-size: 2rem; border-left: 2px solid var(--color-olive); padding-left: 2rem; color: var(--color-sand); font-weight: 400;">
                            "Volver a ver tu textura con orgullo. Menos pelea frente al espejo; más confianza en tu
                            rutina."
                        </blockquote>
                    </figure>
                </div>
                <div class="split-media">
                    <div
                        style="width: 100%; height: 100%; background: #111; display: flex; align-items: center; justify-content: center; color: #444;">
                        <span class="text-caps">[IMG: Retrato en Clave Baja]</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Controls -->
    <div class="slide-counter"><span id="curr-slide">1</span> / 9</div>
    <div class="nav-controls">
        <button class="nav-btn" onclick="prevSlide()">Anterior</button>
        <button class="nav-btn" onclick="nextSlide()">Siguiente</button>
    </div>
    <script>
        let currentSlide = 0;
        const slides = document.querySelectorAll('.slide');
        const counter = document.getElementById('curr-slide');
        function showSlide(index) {
            slides.forEach(s => s.classList.remove('active'));
            slides[index].classList.add('active');
            counter.innerText = index + 1;
        }
        function nextSlide() {
            if (currentSlide < slides.length - 1) {
                currentSlide++;
                showSlide(currentSlide);
            }
        }
        function prevSlide() {
            if (currentSlide > 0) {
                currentSlide--;
                showSlide(currentSlide);
            }
        }
        // Keyboard nav
        document.addEventListener('keydown', (e) => {
            if (e.key === 'ArrowRight') nextSlide();
            if (e.key === 'ArrowLeft') prevSlide();
        });
    </script>
</body>
</html>
