jh-transportes/
 ├── angular.json
 ├── package.json
 ├── tsconfig.json
 └── src/
     ├── index.html
     ├── main.ts
     └── app.component.ts<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <title>JH Transportes</title>
  <base href="/" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
</head>
<body>
  <app-root></app-root>
</body>
</html>import { bootstrapApplication } from '@angular/platform-browser';
import { AppComponent } from './app.component';

bootstrapApplication(AppComponent).catch(err => console.error(err));import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  standalone: true,
  template: `
    <header>
      <h1>JH Transportes</h1>
      <p>Transporte con equipos de frío</p>
    </header>

    <section class="hero">
      <h2>Logística en la que podés confiar</h2>
      <p>Soluciones de transporte refrigerado para tu negocio</p>
    </section>

    <section>
      <h2>Servicios</h2>
      <p>
        Transporte en camiones con frío, garantizando que tu carga llegue segura.
      </p>
    </section>

    <section>
      <h2>Apoyamos a las empresas que están creciendo</h2>
      <p>
        Sabemos lo que significa empezar. Por eso, si tu empresa es nueva o está
        en expansión, comunicate con nosotros: podemos armarte una propuesta
        especial para que tengas un transporte confiable desde el día uno.
      </p>
    </section>

    <footer>
      <p>📞 +54 9 11 5633 0148</p>
      <p>📧 jhtransportes1@hotmail.com</p>
      <a class="btn" href="https://wa.me/5491156330148" target="_blank">WhatsApp</a>
      <p style="margin-top: 1rem">
        © 2025 JH Transportes - Todos los derechos reservados
      </p>
    </footer>
  `,
  styles: [`
    header {
      background: #004aad;
      color: white;
      padding: 1rem;
      text-align: center;
    }
    .hero {
      background: #e9f2ff;
      padding: 2rem;
      text-align: center;
    }
    section {
      padding: 1.5rem;
    }
    footer {
      background: #222;
      color: white;
      text-align: center;
      padding: 1rem;
    }
    .btn {
      display: inline-block;
      margin-top: .5rem;
      padding: .5rem 1rem;
      background: #25D366;
      color: white;
      text-decoration: none;
      border-radius: 5px;
    }
  `]
})
export class AppComponent {}npm install
npm run build