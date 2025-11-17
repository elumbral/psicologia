[index.html](https://github.com/user-attachments/files/23582681/index.html)<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>El Umbral | Psicología del instante</title>
    <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Merriweather:ital,wght@0,400;0,700;1,400&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --primary: #4a5f8f;
            --secondary: #7b6b9e;
            --accent: #9b8fc4;
            --contrast: #5d4e7a;
            --fresh: #6b8cb5;
            --bg-main: #f7f8fc;
            --bg-section: #eef0f7;
            --bg-white: #ffffff;
            --text-dark: #2d2d2d;
            --text-medium: #6a6a6a;
            --border: #d8dae5;
        }
        
        body {
            font-family: 'Merriweather', Georgia, serif;
            color: var(--text-dark);
            background-color: var(--bg-main);
            line-height: 1.75;
        }
        
        /* TEXTURA SUTIL */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0.03;
            z-index: -1;
            background-image: 
                repeating-linear-gradient(0deg, transparent, transparent 2px, var(--text-dark) 2px, var(--text-dark) 4px),
                repeating-linear-gradient(90deg, transparent, transparent 2px, var(--text-dark) 2px, var(--text-dark) 4px);
            pointer-events: none;
        }
        
        /* HEADER */
        header {
            background: var(--bg-white);
            border-top: 6px solid var(--primary);
            border-bottom: 3px solid var(--accent);
            padding: 1.5rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 4px 20px rgba(74, 95, 143, 0.12);
        }
        
        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo-container {
            text-align: left;
        }
        
        .logo {
            font-family: 'Bebas Neue', Arial, sans-serif;
            font-size: 2.2rem;
            font-weight: bold;
            color: var(--primary);
            letter-spacing: 4px;
            line-height: 1;
        }
        
        .logo-divider {
            width: 120px;
            height: 2px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            margin: 0.4rem 0;
        }
        
        .logo-subtitle {
            font-family: 'Merriweather', serif;
            font-size: 0.75rem;
            color: var(--text-medium);
            font-style: italic;
            line-height: 1.4;
            padding-left: 1.5rem;
        }
        
        nav ul {
            display: flex;
            gap: 2.5rem;
            list-style: none;
        }
        
        nav a {
            text-decoration: none;
            color: var(--text-medium);
            font-size: 0.9rem;
            font-family: 'Space Mono', monospace;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: color 0.3s;
            position: relative;
        }
        
        nav a::after {
            content: '';
            position: absolute;
            bottom: -3px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent);
            transition: width 0.3s;
        }
        
        nav a:hover {
            color: var(--primary);
        }
        
        nav a:hover::after {
            width: 100%;
        }
        
        /* HERO */
        .hero {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: var(--bg-white);
            padding: 5rem 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                radial-gradient(circle at 20% 50%, rgba(255,255,255,0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(0,0,0,0.1) 0%, transparent 50%);
            pointer-events: none;
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
        }
        
        .hero h1 {
            font-family: 'Bebas Neue', Arial, sans-serif;
            font-size: 3.5rem;
            margin-bottom: 1rem;
            letter-spacing: 2px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }
        
        .hero p {
            font-size: 1.15rem;
            max-width: 750px;
            margin: 0 auto 2.5rem;
            opacity: 0.95;
            line-height: 1.6;
        }
        
        .edition-badge {
            display: inline-block;
            background: rgba(255,255,255,0.25);
            backdrop-filter: blur(10px);
            padding: 0.75rem 2rem;
            border-radius: 30px;
            font-size: 0.85rem;
            font-family: 'Space Mono', monospace;
            border: 1px solid rgba(255,255,255,0.3);
        }
        
        /* CONTAINER */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 4rem 2rem;
        }
        
        /* SECTION HEADERS */
        .section-header {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-header h2 {
            font-family: 'Bebas Neue', Arial, sans-serif;
            color: var(--primary);
            font-size: 2.8rem;
            letter-spacing: 3px;
            margin-bottom: 0.5rem;
        }
        
        .section-header p {
            color: var(--text-medium);
            font-style: italic;
            font-size: 1rem;
        }
        
        /* ESTANTES */
        .estantes {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2.5rem;
            margin-bottom: 5rem;
        }
        
        .estante {
            background: var(--bg-white);
            border: 3px solid var(--border);
            border-radius: 2px;
            padding: 2.5rem;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }
        
        .estante::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 4px;
            background: linear-gradient(to right, var(--accent), var(--primary));
            transition: left 0.4s;
        }
        
        .estante:hover::before {
            left: 0;
        }
        
        .estante:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 35px rgba(74, 95, 143, 0.25);
            border-color: var(--primary);
        }
        
        .estante-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            filter: grayscale(0.3);
        }
        
        .estante h3 {
            font-family: 'Bebas Neue', Arial, sans-serif;
            color: var(--secondary);
            margin-bottom: 0.75rem;
            font-size: 1.6rem;
            letter-spacing: 1px;
        }
        
        .estante p {
            color: var(--text-medium);
            font-size: 0.95rem;
            margin-bottom: 1.5rem;
        }
        
        .ficha-count {
            display: inline-block;
            background: var(--bg-section);
            color: var(--contrast);
            padding: 0.4rem 1rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-family: 'Space Mono', monospace;
            font-weight: bold;
        }
        
        /* FICHA DESTACADA */
        .ficha-destacada {
            background: var(--bg-white);
            border-left: 8px solid var(--accent);
            border-right: 1px solid var(--border);
            border-top: 1px solid var(--border);
            border-bottom: 1px solid var(--border);
            padding: 3rem;
            margin-bottom: 4rem;
            box-shadow: 0 6px 25px rgba(123, 107, 158, 0.12);
            position: relative;
        }
        
        .ficha-destacada::before {
            content: '"';
            position: absolute;
            top: -20px;
            left: 30px;
            font-size: 8rem;
            color: var(--accent);
            opacity: 0.15;
            font-family: Georgia, serif;
            line-height: 1;
        }
        
        .ficha-destacada h2 {
            font-family: 'Bebas Neue', Arial, sans-serif;
            color: var(--primary);
            margin-bottom: 2rem;
            font-size: 2.5rem;
            letter-spacing: 2px;
        }
        
        .tabs {
            display: flex;
            gap: 0;
            margin-bottom: 2.5rem;
            border-bottom: 3px solid var(--border);
        }
        
        .tab {
            padding: 1rem 1.75rem;
            cursor: pointer;
            border: none;
            background: none;
            font-size: 0.9rem;
            font-family: 'Space Mono', monospace;
            color: var(--text-medium);
            transition: all 0.3s;
            border-bottom: 4px solid transparent;
            margin-bottom: -3px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        
        .tab:hover {
            background: var(--bg-section);
        }
        
        .tab.active {
            color: var(--primary);
            border-bottom-color: var(--primary);
            font-weight: bold;
            background: var(--bg-section);
        }
        
        .tab-content {
            display: none;
            animation: fadeIn 0.5s;
        }
        
        .tab-content.active {
            display: block;
        }
        
        @keyframes fadeIn {
            from { 
                opacity: 0; 
                transform: translateY(15px); 
            }
            to { 
                opacity: 1; 
                transform: translateY(0); 
            }
        }
        
        .tab-content h3 {
            font-family: 'Bebas Neue', Arial, sans-serif;
            color: var(--secondary);
            margin: 2rem 0 1rem;
            font-size: 1.5rem;
            letter-spacing: 1px;
        }
        
        .tab-content ul {
            margin-left: 2rem;
            margin-bottom: 1.5rem;
        }
        
        .tab-content li {
            margin-bottom: 0.75rem;
            padding-left: 0.5rem;
        }
        
        .tab-content li::marker {
            color: var(--accent);
        }
        
        /* STAMP/SELLO */
        .stamp {
            display: inline-block;
            padding: 0.3rem 0.8rem;
            border: 2px dashed var(--primary);
            color: var(--primary);
            font-family: 'Space Mono', monospace;
            font-size: 0.75rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            transform: rotate(-2deg);
            margin: 1rem 0;
            font-weight: bold;
        }
        
        /* EDICIONES (SERENDIPIA) */
        .ediciones-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
            gap: 2.5rem;
        }
        
        .edicion-card {
            background: var(--bg-white);
            border: 3px solid var(--border);
            overflow: hidden;
            transition: transform 0.3s, box-shadow 0.3s;
            position: relative;
        }
        
        .edicion-card:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }
        
        .edicion-header {
            background: var(--primary);
            color: white;
            padding: 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .edicion-header::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
        }
        
        .edicion-numero {
            font-family: 'Bebas Neue', Arial, sans-serif;
            font-size: 3rem;
            font-weight: bold;
            letter-spacing: 2px;
            position: relative;
            z-index: 1;
        }
        
        .edicion-fecha {
            font-family: 'Space Mono', monospace;
            font-size: 0.85rem;
            opacity: 0.9;
            margin-top: 0.5rem;
            position: relative;
            z-index: 1;
        }
        
        .edicion-body {
            padding: 2rem;
        }
        
        .edicion-temas {
            list-style: none;
            font-size: 0.9rem;
        }
        
        .edicion-temas li {
            padding: 0.75rem 0;
            border-bottom: 1px solid var(--border);
            color: var(--text-medium);
            transition: color 0.3s, padding-left 0.3s;
        }
        
        .edicion-temas li:hover {
            color: var(--primary);
            padding-left: 0.5rem;
        }
        
        .edicion-temas li:last-child {
            border-bottom: none;
        }
        
        /* SERVICIOS */
        .servicios {
            background: var(--bg-section);
            padding: 5rem 2rem;
            margin-top: 5rem;
            position: relative;
        }
        
        .servicios::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                repeating-linear-gradient(45deg, transparent, transparent 35px, rgba(74, 95, 143, 0.03) 35px, rgba(74, 95, 143, 0.03) 70px);
            pointer-events: none;
        }
        
        .servicios-grid {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2.5rem;
            position: relative;
            z-index: 1;
        }
        
        .servicio-card {
            background: var(--bg-white);
            padding: 3rem;
            border-left: 6px solid var(--accent);
            border-right: 1px solid var(--border);
            border-top: 1px solid var(--border);
            border-bottom: 1px solid var(--border);
            transition: all 0.3s;
            position: relative;
        }
        
        .servicio-card::after {
            content: '→';
            position: absolute;
            bottom: 2rem;
            right: 2rem;
            font-size: 2rem;
            color: var(--accent);
            opacity: 0;
            transition: all 0.3s;
        }
        
        .servicio-card:hover {
            transform: translateX(8px);
            box-shadow: -5px 5px 20px rgba(74, 95, 143, 0.2);
        }
        
        .servicio-card:hover::after {
            opacity: 1;
            right: 1.5rem;
        }
        
        .servicio-card h3 {
            font-family: 'Bebas Neue', Arial, sans-serif;
            color: var(--primary);
            margin-bottom: 1rem;
            font-size: 1.8rem;
            letter-spacing: 1px;
        }
        
        .servicio-card p {
            color: var(--text-medium);
            margin-bottom: 2rem;
        }
        
        .servicio-cta {
            display: inline-block;
            padding: 0.85rem 1.75rem;
            background: var(--primary);
            color: white;
            text-decoration: none;
            font-family: 'Space Mono', monospace;
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s;
            border: 2px solid var(--primary);
        }
        
        .servicio-cta:hover {
            background: transparent;
            color: var(--primary);
        }
        
        /* FOOTER */
        footer {
            background: var(--text-dark);
            color: white;
            padding: 4rem 2rem 2rem;
            margin-top: 5rem;
            border-top: 5px solid var(--accent);
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            margin-bottom: 3rem;
        }
        
        .footer-section h4 {
            font-family: 'Bebas Neue', Arial, sans-serif;
            color: var(--accent);
            margin-bottom: 1rem;
            font-size: 1.3rem;
            letter-spacing: 2px;
        }
        
        .footer-section p, .footer-section a {
            color: rgba(255,255,255,0.75);
            font-size: 0.9rem;
            text-decoration: none;
            line-height: 1.8;
        }
        
        .footer-section a:hover {
            color: var(--accent);
        }
        
        .colaboradores {
            display: flex;
            flex-wrap: wrap;
            gap: 0.75rem;
            margin-top: 1rem;
        }
        
        .colaborador-badge {
            background: rgba(255,255,255,0.1);
            padding: 0.5rem 1rem;
            border-radius: 3px;
            font-size: 0.8rem;
            font-family: 'Space Mono', monospace;
            border: 1px solid rgba(255,255,255,0.2);
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.15);
            color: rgba(255,255,255,0.5);
            font-size: 0.85rem;
        }
        
        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
                gap: 1rem;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .tabs {
                flex-direction: column;
            }
            
            .tab {
                border-bottom: 1px solid var(--border);
                text-align: left;
            }
            
            .section-header h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-content">
            <div class="logo-container">
                <div class="logo">EL UMBRAL</div>
                <div class="logo-divider"></div>
                <div class="logo-subtitle">
                    Psicología del instante<br>
                    <span style="padding-left: 1.5rem;">Entre el aquí y el ahora... ¡qué!?</span>
                </div>
            </div>
            <nav>
                <ul>
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#estante">Estante 3</a></li>
                    <li><a href="#cafecito">Cafecito</a></li>
                    <li><a href="#consultorio">Consultorio</a></li>
                    <li><a href="#serendipia">Serendipia</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <div class="hero">
        <div class="hero-content">
            <h1>Psicología a la carta</h1>
            <p>No es contenido para scrollear. Es lectura de sala de espera, de café, de domingo tarde. Material denso que permanece, se consulta, se vuelve a leer. Como esas revistas que guardabas y releías.</p>
            <div class="edition-badge">📖 ED. NOV 2025 | Vínculos en tiempos de cambio</div>
        </div>
    </div>

    <div class="container">
        <div class="section-header">
            <h2>Estante 3</h2>
            <p>El archivo permanente. Donde se guardan las fichas que importan.</p>
        </div>
        
        <div class="estantes" id="estante">
            <div class="estante">
                <div class="estante-icon">🧠</div>
                <h3>Clínica</h3>
                <p>Ansiedad, depresión, trauma. Los temas duros abordados con rigurosidad y empatía, sin eufemismos.</p>
                <span class="ficha-count">12 FICHAS</span>
            </div>
            
            <div class="estante">
                <div class="estante-icon">🤝</div>
                <h3>Vínculos</h3>
                <p>Pareja, familia, amistad. Las dinámicas relacionales desde múltiples perspectivas. Lo que se dice y lo que no.</p>
                <span class="ficha-count">15 FICHAS</span>
            </div>
            
            <div class="estante">
                <div class="estante-icon">🌱</div>
                <h3>Autoconocimiento</h3>
                <p>Autoestima, duelo, propósito. Herramientas para el crecimiento que no son autoayuda barata.</p>
                <span class="ficha-count">10 FICHAS</span>
            </div>
            
            <div class="estante">
                <div class="estante-icon">🏙️</div>
                <h3>Psique urbana</h3>
                <p>Trabajo, comunidad, cultura. Cómo los contextos moldean nuestra experiencia. Psicología de la ciudad.</p>
                <span class="ficha-count">8 FICHAS</span>
            </div>
        </div>

        <!-- FICHA DESTACADA -->
        <div class="ficha-destacada">
            <span class="stamp">Ficha Nueva</span>
            <h2>Apego Ansioso</h2>
            
            <div class="tabs">
                <button class="tab active" onclick="showTab(0)">Entrada Rápida</button>
                <button class="tab" onclick="showTab(1)">Desarrollo</button>
                <button class="tab" onclick="showTab(2)">Profundización</button>
            </div>
            
            <div class="tab-content active">
                <p><strong>¿Qué es?</strong> El apego ansioso es un patrón relacional en el que la persona experimenta miedo constante al abandono y busca validación externa de forma recurrente. No es debilidad, es una estrategia aprendida.</p>
                
                <h3>Señales comunes</h3>
                <ul>
                    <li>Necesidad de estar en contacto permanente con la pareja</li>
                    <li>Interpretación de silencios como rechazo</li>
                    <li>Dificultad para tolerar la autonomía del otro</li>
                    <li>Hipervigilancia a señales de desinterés</li>
                </ul>
                
                <h3>Primeros pasos</h3>
                <p>Reconocer el patrón es fundamental. Si te identificás con estas características, considerá explorar su origen (generalmente en vínculos tempranos) y desarrollar estrategias de autoregulación emocional. No es algo que se arregla con fuerza de voluntad.</p>
            </div>
            
            <div class="tab-content">
                <h3>Origen del patrón</h3>
                <p>El apego ansioso suele desarrollarse cuando las figuras de cuidado en la infancia fueron inconsistentes en su disponibilidad emocional. El niño aprendió que para obtener atención debía intensificar sus demandas. Era eso o la indiferencia.</p>
                
                <h3>Mecanismos psicológicos</h3>
                <p>La persona con apego ansioso desarrolla un "sistema de vigilancia" hipersensible, interpretando ambigüedades como amenazas. Esto activa estrategias de hiperactivación: buscar proximidad de forma insistente. Es agotador para todos.</p>
                
                <h3>Caso ilustrativo</h3>
                <p><em>María revisa constantemente su teléfono esperando mensajes de su pareja. Cuando él tarda en responder, experimenta ansiedad intensa y tiende a enviar múltiples mensajes. Interpreta cualquier distracción de su pareja como falta de interés. Sabe que está siendo "intensa" pero no puede evitarlo.</em></p>
                
                <h3>Impacto en relaciones</h3>
                <ul>
                    <li>Genera dinámicas de persecución-distancia (cuanto más persigue, más se aleja el otro)</li>
                    <li>Puede provocar agotamiento en la pareja y confirmar el miedo inicial</li>
                    <li>Dificulta el establecimiento de límites saludables</li>
                    <li>Aumenta la probabilidad de cumplir la profecía del abandono</li>
                </ul>
            </div>
            
            <div class="tab-content">
                <h3>Marco teórico</h3>
                <p>Basado en la Teoría del Apego de John Bowlby y Mary Ainsworth. Investigaciones posteriores de Hazan y Shaver (1987) extendieron estos conceptos a relaciones adultas. No es psicología pop, es ciencia dura.</p>
                
                <h3>Ejercicios prácticos</h3>
                <ol>
                    <li><strong>Registro emocional:</strong> Anotá cuándo aparece la ansiedad vincular y qué pensamientos la acompañan. Sin juzgar, solo observar.</li>
                    <li><strong>Práctica de tolerancia:</strong> Esperá 10 minutos antes de contactar cuando surja el impulso. Aumentá progresivamente.</li>
                    <li><strong>Validación interna:</strong> Escribí tres cualidades tuyas que no dependen de la aprobación externa. Releelas cuando necesites.</li>
                </ol>
                
                <h3>Bibliografía recomendada</h3>
                <ul>
                    <li>Levine, A. & Heller, R. (2010). <em>Attached: The New Science of Adult Attachment</em></li>
                    <li>Johnson, S. (2008). <em>Hold Me Tight: Seven Conversations for a Lifetime of Love</em></li>
                    <li>Wallin, D. (2007). <em>Attachment in Psychotherapy</em></li>
                </ul>
                
                <h3>Recursos profesionales</h3>
                <p>Terapia Focalizada en las Emociones (EFT) y terapia basada en mentalización han mostrado eficacia en trabajo con estilos de apego inseguros. No todos los enfoques sirven para esto.</p>
                
                <p style="margin-top: 2rem; padding: 1.5rem; background: var(--bg-section); border-left: 4px solid var(--fresh); border-radius: 2px;"><strong>Nota de actualización:</strong> Esta ficha se actualiza regularmente con nuevas investigaciones. Última actualización: Noviembre 2025</p>
            </div>
        </div>

        <!-- SERENDIPIA (EDICIONES) -->
        <div class="section-header">
            <h2 id="serendipia">Serendipia</h2>
            <p>Las ediciones mensuales. Encuentros casuales con contenido que buscabas sin saber que buscabas.</p>
        </div>
        
        <div class="ediciones-grid">
            <div class="edicion-card">
                <div class="edicion-header">
                    <div class="edicion-numero">N° 11</div>
                    <div class="edicion-fecha">Noviembre 2025</div>
                </div>
                <div class="edicion-body">
                    <ul class="edicion-temas">
                        <li>→ Vínculos en tiempos de cambio</li>
                        <li>→ Consultorio: soledad elegida vs impuesta</li>
                        <li>→ Caso sin nombre: duelo migratorio</li>
                        <li>→ Nueva ficha: resiliencia real (no la del Instagram)</li>
                        <li>→ Cafecito con Dra. Fernández (UNC)</li>
                    </ul>
                </div>
            </div>
            
            <div class="edicion-card">
                <div class="edicion-header" style="background: #5a7d6f;">
                    <div class="edicion-numero">N° 10</div>
                    <div class="edicion-fecha">Octubre 2025</div>
                </div>
                <div class="edicion-body">
                    <ul class="edicion-temas">
                        <li>→ Ansiedad anticipatoria: el futuro que no llega</li>
                        <li>→ Cafecito: psicoanálisis y política</li>
                        <li>→ Glosario vivo: mentalización</li>
                        <li>→ Reseña: "El cuerpo lleva la cuenta"</li>
                        <li>→ Consultorio: límites con la familia</li>
                    </ul>
                </div>
            </div>
            
            <div class="edicion-card">
                <div class="edicion-header" style="background: #a85b3a;">
                    <div class="edicion-numero">N° 9</div>
                    <div class="edicion-fecha">Septiembre 2025</div>
                </div>
                <div class="edicion-body">
                    <ul class="edicion-temas">
                        <li>→ Burnout: cuando laburar te quema</li>
                        <li>→ Consultorio: ¿renuncio o aguanto?</li>
                        <li>→ Psicología del trabajo precarizado</li>
                        <li>→ Ejercicios de desconexión real</li>
                        <li>→ Cafecito desde Centro de Estudiantes</li>
                    </ul>
                </div>
            </div>
            
            <div class="edicion-card">
                <div class="edicion-header" style="background: #7ba58e;">
                    <div class="edicion-numero">N° 8</div>
                    <div class="edicion-fecha">Agosto 2025</div>
                </div>
                <div class="edicion-body">
                    <ul class="edicion-temas">
                        <li>→ Dependencia emocional: más allá del cliché</li>
                        <li>→ Caso: cuando amar duele (literalmente)</li>
                        <li>→ Nueva ficha: codependencia</li>
                        <li>→ Consultorio: ¿cómo salir de esto?</li>
                        <li>→ Cafecito con terapeuta vincular</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

    <!-- SERVICIOS PROFESIONALES -->
    <div class="servicios">
        <div class="section-header">
            <h2>Más allá de la lectura</h2>
            <p>Cuando necesitás pasar del conocimiento a la experiencia.</p>
        </div>
        
        <div class="servicios-grid">
            <div class="servicio-card">
                <h3>Consultas</h3>
                <p>Atención psicológica online y presencial. Enfoque integrativo: psicoanálisis + herramientas cognitivo-conductuales. Sin soluciones mágicas, con trabajo real.</p>
                <a href="#" class="servicio-cta">Ver modalidades</a>
            </div>
            
            <div class="servicio-card">
                <h3>Talleres</h3>
                <p>Encuentros grupales mensuales sobre temas específicos. Vínculos, ansiedad, autoconocimiento. Espacio de reflexión colectiva, no terapia grupal.</p>
                <a href="#" class="servicio-cta">Próximos talleres</a>
            </div>
            
            <div class="servicio-card">
                <h3>Supervisión</h3>
                <p>Para colegas psicólogos. Espacios de supervisión clínica individual y grupal. Análisis de casos, estrategias, desarrollo profesional. Entre pares.</p>
                <a href="#" class="servicio-cta">Más info</a>
            </div>
        </div>
    </div>

    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h4>Sobre el proyecto</h4>
                <p>El Umbral es una publicación independiente que recupera el espíritu de las revistas de consultorio. Psicología para leer despacio, consultar seguido, guardar y volver. No es contenido desechable.</p>
            </div>
            
            <div class="footer-section">
                <h4>Colaboraciones actuales</h4>
                <p>Este proyecto dialoga con espacios que comparten el compromiso con la difusión responsable del conocimiento psicológico.</p>
                <div class="colaboradores">
                    <span class="colaborador-badge">Radio Universidad</span>
                    <span class="colaborador-badge">Centro Est. Psicología</span>
                    <span class="colaborador-badge">Colectivo Clínica UNC</span>
                    <span class="colaborador-badge">Podcast "Freud Said"</span>
                </div>
            </div>
            
            <div class="footer-section">
                <h4>Contacto</h4>
                <p>info@elumbral.com<br>
                Suscripciones: suscripciones@elumbral.com<br>
                Consultas profesionales: consultas@elumbral.com<br>
                Colaboraciones/prensa: colaboraciones@elumbral.com</p>
            </div>
        </div>
        
        <div class="footer-bottom">
            <p>© 2025 El Umbral — Psicología del instante<br>
            Publicación editorial profesional. No reemplaza atención psicológica individual.</p>
        </div>
    </footer>

    <script>
        function showTab(index) {
            const tabs = document.querySelectorAll('.tab');
            const contents = document.querySelectorAll('.tab-content');
            
            tabs.forEach(tab => tab.classList.remove('active'));
            contents.forEach(content => content.classList.remove('active'));
            
            tabs[index].classList.add('active');
            contents[index].classList.add('active');
        }
    </script>
</body>
</html>
