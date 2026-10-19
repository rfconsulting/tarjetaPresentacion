# Tarjeta de presentación — RF Consulting

Tarjeta de presentación digital de **Richard Flores**, consultor de sistemas e integración empresarial en **RF Consulting**.

El sitio comunica una propuesta de valor concreta —integrar sistemas administrativos con facturación electrónica para reducir el doble registro— y ofrece accesos directos para iniciar una conversación por WhatsApp, guardar el contacto y consultar los perfiles profesionales.

## Características

- Diseño responsive para escritorio y dispositivos móviles.
- Enlace directo a WhatsApp con un mensaje inicial predefinido.
- Descarga del contacto en formato vCard (`.vcf`).
- Accesos a correo electrónico, teléfono y sitio web.
- Enlaces a LinkedIn y GitHub.
- Navegación por teclado y estilos visibles de enfoque.
- Respeto por la preferencia del sistema para reducir animaciones.
- Implementación estática, sin dependencias ni proceso de compilación.

## Tecnologías

- HTML5 semántico.
- CSS3, Grid y Flexbox.
- Google Fonts: Bricolage Grotesque.
- vCard 3.0 para guardar el contacto.

## Estructura del repositorio

```text
tarjetaPresentacion/
├── assets/
│   ├── css/
│   │   └── styles.css          # Diseño, colores y adaptación responsive
│   └── img/
│       ├── logo.png            # Isotipo de RF Consulting
│       ├── logo_horizontal.png # Logotipo utilizado en la tarjeta
│       └── perfil.jpg          # Fotografía de perfil
├── index.html                  # Página principal
├── richard-flores.vcf          # Contacto descargable
└── README.md                   # Documentación del proyecto
```

## Ejecución local

El proyecto no requiere instalación. Puede abrirse `index.html` directamente en el navegador, aunque se recomienda servirlo mediante HTTP para reproducir el comportamiento de producción.

Con Python 3:

```bash
python -m http.server 4173
```

Después, abre [http://localhost:4173](http://localhost:4173) en el navegador.

## Personalización

### Información y enlaces

Edita `index.html` para modificar:

- Nombre, cargo y propuesta de valor.
- Correo electrónico, teléfono y sitio web.
- Número y mensaje inicial de WhatsApp.
- Perfiles de LinkedIn y GitHub.

El número de WhatsApp debe escribirse en formato internacional, sin espacios ni el símbolo `+`:

```html
https://wa.me/50761555815
```

### Contacto descargable

Actualiza `richard-flores.vcf` cuando cambie algún dato personal o profesional. Los campos del archivo deben coincidir con la información visible en la tarjeta.

### Identidad visual

Los colores principales están definidos como variables al inicio de `assets/css/styles.css`:

```css
:root {
  --navy: #020617;
  --cyan: #22d3ee;
}
```

Reemplaza los archivos de `assets/img/` conservando sus nombres, o actualiza las rutas correspondientes en `index.html`.

## Verificación antes de publicar

Comprueba lo siguiente después de cada cambio:

1. La tarjeta no presenta desplazamiento horizontal en móvil.
2. El botón de WhatsApp abre la conversación con el número correcto.
3. `Guardar contacto` descarga una vCard válida.
4. Los enlaces de correo, teléfono, sitio web y redes apuntan al destino correcto.
5. Las imágenes incluyen texto alternativo adecuado.
6. El foco del teclado permanece visible en todos los enlaces.

## Despliegue

Al ser un sitio estático, puede publicarse en GitHub Pages, Cloudflare Pages, Netlify, Vercel o cualquier servidor web convencional. El directorio raíz del repositorio funciona como directorio público y no necesita un comando de compilación.

## Repositorio

[github.com/rfconsulting/tarjetaPresentacion](https://github.com/rfconsulting/tarjetaPresentacion)

## Autor

**Richard Flores — RF Consulting**

- Sitio: [rfcpty.com](https://rfcpty.com)
- LinkedIn: [floresmrichardj](https://www.linkedin.com/in/floresmrichardj/)
- GitHub: [rfconsulting](https://github.com/rfconsulting)
