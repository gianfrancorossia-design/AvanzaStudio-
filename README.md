<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Avanza Studio | Soluciones Estratégicas y Digitales para tu Negocio</title>

    <style>
        :root {
            --primary: #4C0519;
            --accent: #A8133C;
            --text-light: #FFFFFF;
            --text-dark: #2A1218;
            --bg-light: #FAF5F6;
            --card-bg: #FFFFFF;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }

        body {
            background-color: var(--bg-light);
            color: var(--text-dark);
            line-height: 1.6;
        }

        header {
            background-color: #23020B;
            color: var(--text-light);
            padding: 1.2rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 15px rgba(35, 2, 11, 0.4);
            border-bottom: 1px solid rgba(255, 255, 255, 0.15);
        }

        .logo {
            font-size: 1.6rem;
            font-weight: 700;
            color: var(--text-light);
            letter-spacing: -0.5px;
            text-shadow: 0 0 1px rgba(255,255,255,0.3);
        }

        .logo span {
            color: #FF3366;
        }

        nav a {
            color: var(--text-light);
            text-decoration: none;
            margin-left: 2rem;
            font-weight: 500;
            transition: color 0.3s ease;
            cursor: pointer;
        }

        nav a:hover {
            color: #FF3366;
        }

        .hero {
            background: linear-gradient(
                135deg,
                #23020B 30%,
                #4C0519 65%,
                #830A2B 100%
            );
            color: var(--text-light);
            padding: 5rem 5% 6rem 5%;
            text-align: center;
            border-bottom: 3px solid #A8133C;
        }

        .hero h1 {
            font-size: 2.8rem;
            margin-bottom: 1rem;
            line-height: 1.2;
            color: #FFFFFF;
            text-shadow: 0 2px 12px rgba(0, 0, 0, 0.3);
        }

        .hero h1 span {
            color: #FF4D79;
            text-shadow: 0 0 25px rgba(255, 77, 121, 0.4);
        }

        .hero-subtitle {
            font-size: 1.2rem;
            max-width: 750px;
            margin: 0 auto 1.2rem auto;
            color: #FFE4EC;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            text-shadow: 0 1px 4px rgba(0,0,0,0.3);
        }

        .hero p {
            font-size: 1.15rem;
            max-width: 750px;
            margin: 0 auto 2.5rem auto;
            color: #FFFFFF;
            font-weight: 400;
            text-shadow: 0 1px 6px rgba(0, 0, 0, 0.3);
        }

        .btn {
            background-color: #A8133C;
            color: #FFFFFF;
            padding: 0.9rem 2.2rem;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 700;
            transition:
                transform 0.3s ease,
                box-shadow 0.3s ease,
                background-color 0.3s ease;
            display: inline-block;
            border: 1px solid rgba(255, 255, 255, 0.25);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
            cursor: pointer;
        }

        .btn:hover {
            transform: translateY(-2px);
            background-color: #C2184B;
            box-shadow: 0 6px 20px rgba(194, 24, 75, 0.5);
        }

        .services {
            padding: 5rem 5%;
            max-width: 1250px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.4rem;
            color: var(--primary);
            margin-bottom: 0.8rem;
        }

        .section-description {
            text-align: center;
            max-width: 700px;
            margin: 0 auto 3.5rem auto;
            color: #70424A;
            font-size: 1.05rem;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
        }

        .service-card {
            background: var(--card-bg);
            padding: 2.5rem;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(76, 5, 25, 0.05);
            border-top: 4px solid var(--accent);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .service-card:hover {
            transform: translateY(-6px);
            box-shadow: 0 10px 25px rgba(76, 5, 25, 0.1);
        }

        .service-content {
            margin-bottom: 1.5rem;
        }

        .service-card h3 {
            font-size: 1.4rem;
            color: var(--primary);
            margin-bottom: 1rem;
            line-height: 1.3;
        }

        .service-card p {
            color: var(--text-dark);
            font-size: 0.98rem;
            line-height: 1.6;
        }

        .service-price {
            font-weight: 700;
            color: var(--accent);
            font-size: 1.05rem;
            text-align: left;
            margin-top: auto;
            padding-top: 1rem;
            border-top: 1px solid #F0DCE2;
        }

        .contact {
            background: linear-gradient(
                135deg,
                #830A2B 0%,
                #4C0519 50%,
                #23020B 100%
            );
            color: var(--text-light);
            padding: 5rem 5%;
            text-align: center;
            border-top: 3px solid #A8133C;
        }

        .contact h2 {
            color: #FFFFFF;
            margin-bottom: 1rem;
            text-shadow: 0 2px 10px rgba(0,0,0,0.3);
        }

        .contact p {
            margin-bottom: 2rem;
            font-size: 1.15rem;
            color: #FFFFFF;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            text-shadow: 0 1px 6px rgba(0,0,0,0.3);
        }

        .modal-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(35, 2, 11, 0.75);
            z-index: 2000;
            justify-content: center;
            align-items: center;
            padding: 1rem;
            backdrop-filter: blur(4px);
        }

        .modal-overlay.active {
            display: flex;
        }

        .modal-container {
            background: #FFFFFF;
            width: 100%;
            max-width: 550px;
            border-radius: 12px;
            padding: 2.5rem;
            position: relative;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
            border-top: 5px solid var(--accent);
            animation: modalFadeIn 0.3s ease;
            max-height: 90vh;
            overflow-y: auto;
        }

        @keyframes modalFadeIn {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .modal-close {
            position: absolute;
            top: 1.2rem;
            right: 1.5rem;
            font-size: 1.8rem;
            color: var(--primary);
            cursor: pointer;
            background: none;
            border: none;
            font-weight: 700;
            line-height: 1;
        }

        .modal-container h3 {
            color: var(--primary);
            font-size: 1.8rem;
            margin-bottom: 0.5rem;
        }

        .modal-container p {
            color: #70424A;
            font-size: 0.95rem;
            margin-bottom: 1.5rem;
        }

        .form-group {
            margin-bottom: 1.2rem;
            text-align: left;
        }

        .form-group label {
            display: block;
            font-weight: 600;
            color: var(--primary);
            margin-bottom: 0.4rem;
            font-size: 0.9rem;
        }

        .form-group input {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #D1B3BC;
            border-radius: 6px;
            font-size: 1rem;
            color: var(--text-dark);
            outline: none;
            transition: border-color 0.3s ease;
        }

        .form-group input:focus {
            border-color: var(--accent);
            box-shadow: 0 0 0 3px rgba(168, 19, 60, 0.15);
        }

        .services-checkboxes {
            display: flex;
            flex-direction: column;
            gap: 0.6rem;
            margin-top: 0.5rem;
            background: var(--bg-light);
            padding: 1rem;
            border-radius: 6px;
            border: 1px solid #E2C4D0;
        }

        .checkbox-label {
            display: flex;
            align-items: center;
            gap: 0.6rem;
            font-size: 0.9rem;
            color: var(--text-dark);
            cursor: pointer;
            font-weight: normal !important;
            margin-bottom: 0 !important;
        }

        .checkbox-label input {
            width: 18px;
            height: 18px;
            accent-color: var(--accent);
            cursor: pointer;
        }

        .modal-container .btn {
            width: 100%;
            margin-top: 1rem;
            cursor: pointer;
        }

        footer {
            background-color: #170107;
            color: #E2C4D0;
            text-align: center;
            padding: 2.2rem 1rem;
            font-size: 0.9rem;
            border-top: 1px solid rgba(255,255,255,0.08);
        }

        .footer-links {
            margin-top: 0.6rem;
            display: flex;
            justify-content: center;
            gap: 1.2rem;
            flex-wrap: wrap;
            align-items: center;
        }

        .footer-links a {
            color: #FF80A1;
            text-decoration: none;
            transition: color 0.3s ease;
            cursor: pointer;
        }

        .footer-links a:hover {
            color: #FFFFFF;
            text-decoration: underline;
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.1rem;
            }

            nav {
                display: none;
            }

            .services-grid {
                grid-template-columns: 1fr;
            }

            .service-card {
                padding: 1.8rem;
            }

            .modal-container {
                padding: 1.5rem;
            }
        }
    </style>
</head>

<body>
    <header>
        <div class="logo">Avanza<span>Studio</span></div>

        <nav>
            <a href="#inicio">Inicio</a>
            <a href="#servicios">Servicios</a>
            <a href="#contacto" class="openModalBtn">Contacto</a>
        </nav>
    </header>

    <section id="inicio" class="hero">
        <div class="hero-subtitle">
            Soluciones Tecnológicas en tiempos tecnológicos
        </div>

        <h1>
            Impulsa tu negocio <span>al siguiente nivel</span>
        </h1>

        <p>
            Potenciamos tu negocio combinando estrategia comercial, software a
            medida y aceleración digital para transformar operaciones, optimizar
            recursos y convertir oportunidades en resultados medibles, con
            soluciones flexibles y adaptadas a cada proyecto.
        </p>

        <button class="btn openModalBtn">
            Contáctanos
        </button>
    </section>

    <section id="servicios" class="services">
        <h2 class="section-title">Nuestros Servicios</h2>

        <p class="section-description">
            Soluciones integrales diseñadas para resolver dolores estratégicos,
            digitales y operativos en las micro, pequeñas y medianas empresas.
        </p>

        <div class="services-grid">
            <div class="service-card">
                <div class="service-content">
                    <h3>Desarrollo Web y Soluciones Digitales</h3>

                    <p>
                        Diseñamos e implementamos sitios web estratégicos,
                        rápidos y optimizados para convertir visitantes en
                        clientes. Creamos plataformas modernas y adaptables que
                        fortalecen la presencia digital de tu negocio y
                        automatizan la captura de prospectos.
                    </p>
                </div>

                <div class="service-price">
                    Precio desde $79.990 CLP
                </div>
            </div>

            <div class="service-card">
                <div class="service-content">
                    <h3>Consultoría y Estrategia Comercial</h3>

                    <p>
                        Evaluamos, diseñamos y optimizamos la estructura
                        comercial de tu empresa. Analizamos tus procesos de
                        venta, precios y canales de distribución para identificar
                        oportunidades de crecimiento, mejorar el rendimiento
                        operativo y maximizar la rentabilidad.
                    </p>
                </div>
            </div>

            <div class="service-card">
                <div class="service-content">
                    <h3>Automatización de Procesos y Software a Medida</h3>

                    <p>
                        Desarrollamos herramientas digitales y software comercial
                        personalizado para eliminar tareas repetitivas y conectar
                        tus sistemas de gestión. Simplificamos la operación diaria
                        de tu empresa para reducir errores, optimizar recursos y
                        ahorrar tiempo clave.
                    </p>
                </div>
            </div>

            <div class="service-card">
                <div class="service-content">
                    <h3>Reactivación y Gestión Integral de Proyectos</h3>

                    <p>
                        Destrabamos y ejecutamos proyectos clave que tu empresa
                        tiene detenidos por falta de tiempo o capacidad técnica.
                        Asumimos la gestión estratégica y la implementación
                        digital para transformar ideas postergadas en activos
                        rentables y operativos en tiempo récord.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <section id="contacto" class="contact">
        <h2 class="section-title">
            ¿Listo para transformar tu negocio?
        </h2>

        <p>
            Hablemos sobre tu proyecto o esas ideas que aún no has podido
            implementar. Descubre cómo podemos convertirlas en soluciones
            concretas para tu negocio.
        </p>

        <button class="btn openModalBtn">
            Cuéntanos tu proyecto
        </button>
    </section>

    <footer>
        <p>
            &copy; 2026 Avanza Studio. Todos los derechos reservados.
        </p>

        <div class="footer-links">
            <a class="openModalBtn">Contáctenos</a>
            <span>•</span>

            <a href="mailto:gian-franco.rossi@ugm.cl">
                gian-franco.rossi@ugm.cl
            </a>

            <span>•</span>

            <a href="mailto:tomas.lama@ugm.cl">
                tomas.lama@ugm.cl
            </a>
        </div>
    </footer>

    <div class="modal-overlay" id="contactModal">
        <div class="modal-container">
            <button class="modal-close" id="closeModalBtn">
                &times;
            </button>

            <h3>Hablemos de tu proyecto</h3>

            <p>
                Completa tus datos y selecciona los servicios de tu interés.
                Nos pondremos en contacto contigo a la brevedad.
            </p>

            <form id="contactForm">
                <div class="form-group">
                    <label for="nombre">Nombre completo</label>

                    <input
                        type="text"
                        id="nombre"
                        name="nombre"
                        required
                        placeholder="Ej. Carlos Pérez"
                    >
                </div>

                <div class="form-group">
                    <label for="telefono">Teléfono</label>

                    <input
                        type="tel"
                        id="telefono"
                        name="telefono"
                        required
                        placeholder="Ej. +56 9 1234 5678"
                    >
                </div>

                <div class="form-group">
                    <label for="correo">Correo electrónico</label>

                    <input
                        type="email"
                        id="correo"
                        name="correo"
                        required
                        placeholder="tu@empresa.cl"
                    >
                </div>

                <div class="form-group">
                    <label>¿Qué servicios te interesan?</label>

                    <div class="services-checkboxes">
                        <label class="checkbox-label">
                            <input
                                type="checkbox"
                                name="servicio"
                                value="Desarrollo Web y Soluciones Digitales"
                            >
                            Desarrollo Web y Soluciones Digitales
                        </label>

                        <label class="checkbox-label">
                            <input
                                type="checkbox"
                                name="servicio"
                                value="Consultoría y Estrategia Comercial"
                            >
                            Consultoría y Estrategia Comercial
                        </label>

                        <label class="checkbox-label">
                            <input
                                type="checkbox"
                                name="servicio"
                                value="Automatización de Procesos y Software a Medida"
                            >
                            Automatización de Procesos y Software a Medida
                        </label>

                        <label class="checkbox-label">
                            <input
                                type="checkbox"
                                name="servicio"
                                value="Reactivación y Gestión Integral de Proyectos"
                            >
                            Reactivación y Gestión Integral de Proyectos
                        </label>
                    </div>
                </div>

                <button type="submit" class="btn">
                    Enviar Solicitud
                </button>
            </form>
        </div>
    </div>

    <script>
        const modal = document.getElementById('contactModal');
        const openModalBtns = document.querySelectorAll('.openModalBtn');
        const closeModalBtn = document.getElementById('closeModalBtn');
        const contactForm = document.getElementById('contactForm');

        openModalBtns.forEach(btn => {
            btn.addEventListener('click', event => {
                event.preventDefault();
                modal.classList.add('active');
            });
        });

        closeModalBtn.addEventListener('click', () => {
            modal.classList.remove('active');
        });

        modal.addEventListener('click', event => {
            if (event.target === modal) {
                modal.classList.remove('active');
            }
        });

        contactForm.addEventListener('submit', event => {
            event.preventDefault();

            alert(
                '¡Gracias por contactar a Avanza Studio! ' +
                'Hemos recibido tus datos y los servicios seleccionados. ' +
                'Nos comunicaremos pronto.'
            );

            contactForm.reset();
            modal.classList.remove('active');
        });
    </script>
</body>
</html> 

