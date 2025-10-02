# 🏎️ Formula SAE Electric - Astro Landing Page

Una landing page moderna y de alto rendimiento para equipos de Formula SAE Electric, construida con **Astro** para máxima velocidad y eficiencia.

## ⚡ Características

- **🚀 Ultra Rápido**: Construido con Astro para carga instantánea
- **📱 100% Responsive**: Optimizado para todos los dispositivos
- **🎨 Diseño Moderno**: UI/UX inspirado en las mejores prácticas de 2024
- **♿ Accesible**: Cumple con estándares WCAG
- **🔍 SEO Optimizado**: Meta tags y estructura semántica
- **🎭 Animaciones Suaves**: Efectos visuales sin comprometer rendimiento
- **🧩 Componentes Modulares**: Fácil mantenimiento y escalabilidad

## 🛠️ Stack Tecnológico

- **[Astro](https://astro.build/)** - Framework web moderno
- **TypeScript** - Tipado estático
- **CSS Vanilla** - Estilos puros sin dependencias
- **Componentes .astro** - Arquitectura basada en componentes

## 📁 Estructura del Proyecto

```
formula-sae-astro/
├── src/
│   ├── components/
│   │   ├── sections/         # Secciones principales
│   │   │   ├── Hero.astro
│   │   │   ├── About.astro
│   │   │   ├── Team.astro
│   │   │   ├── Sponsors.astro
│   │   │   └── Contact.astro
│   │   └── ui/              # Componentes de UI
│   │       ├── Navigation.astro
│   │       └── Footer.astro
│   ├── layouts/
│   │   └── Layout.astro     # Layout principal
│   └── pages/
│       └── index.astro      # Página de inicio
├── public/
│   ├── images/              # Imágenes y assets
│   └── icons/               # Iconos y favicons
├── astro.config.mjs         # Configuración de Astro
├── tsconfig.json           # Configuración TypeScript
└── package.json            # Dependencias del proyecto
```

## 🚀 Inicio Rápido

### Requisitos Previos
- **Node.js** (v18 o superior)
- **npm** o **yarn**

### Instalación

1. **Clona el repositorio**
   ```bash
   git clone [url-del-repositorio]
   cd formula-sae-astro
   ```

2. **Instala las dependencias**
   ```bash
   npm install
   ```

3. **Inicia el servidor de desarrollo**
   ```bash
   npm run dev
   ```

4. **Abre tu navegador**
   ```
   http://localhost:4321
   ```

## 📝 Scripts Disponibles

```bash
# Desarrollo
npm run dev          # Servidor de desarrollo
npm run start        # Alias para dev

# Producción
npm run build        # Construir para producción
npm run preview      # Vista previa de la build

# Otros
npm run astro        # CLI de Astro
```

## 🎨 Personalización

### Colores
Los colores están definidos como variables CSS en `src/layouts/Layout.astro`:

```css
:root {
  --primary-color: #011E54;    /* Azul principal del equipo */
  --primary-dark: #000d2e;     /* Azul oscuro */
  --primary-light: #1a3d7a;    /* Azul claro */
  --secondary-color: #FAFBFD;  /* Fondo claro */
  --accent-color: #CDD4E1;     /* Acento gris-azul */
}
```

### Contenido
Cada sección es un componente independiente que puedes personalizar:

- **Hero**: `src/components/sections/Hero.astro`
- **Acerca de**: `src/components/sections/About.astro`
- **Equipo**: `src/components/sections/Team.astro`
- **Sponsors**: `src/components/sections/Sponsors.astro`
- **Contacto**: `src/components/sections/Contact.astro`

### Agregar Imágenes
1. Coloca las imágenes en `public/images/`
2. Úsalas con rutas absolutas: `/images/tu-imagen.jpg`

```astro
<img src="/images/formula-car.jpg" alt="Vehículo Formula SAE" />
```

## 🧩 Componentes

### Hero Section
Sección principal con métricas del equipo:

```astro
<Hero
  title="Engineering the Future"
  subtitle="Tu mensaje personalizado aquí"
/>
```

### Navegación
Navegación fixed con scroll suave:

```astro
<Navigation />
```

### Secciones
Cada sección es un componente autocontenido con sus propios estilos.

## 👥 Colaboración en Equipo

### Estructura Recomendada
1. **Developer 1**: Componentes Hero y About
2. **Developer 2**: Componentes Team y Sponsors
3. **Developer 3**: Contact y Footer
4. **Developer 4**: Layout y estilos globales
5. **Developer 5**: Optimización y deployment

### Flujo de Trabajo Git
```bash
# 1. Crear rama para nueva feature
git checkout -b feature/nueva-funcionalidad

# 2. Hacer cambios y commit
git add .
git commit -m "feat: agregar nueva funcionalidad"

# 3. Push y pull request
git push origin feature/nueva-funcionalidad
```

### Convenciones

#### Componentes Astro
- Nombres en PascalCase: `HeroSection.astro`
- Props tipadas con TypeScript
- Estilos scoped cuando sea posible

#### CSS
- Variables CSS para valores reutilizables
- Mobile-first approach
- Usar las variables de color del design system

## 🚀 Deployment

### Vercel (Recomendado)
```bash
npm i -g vercel
vercel
```

### Netlify
1. Conecta tu repositorio de GitHub
2. Build command: `npm run build`
3. Publish directory: `dist`

### GitHub Pages
```bash
npm run build
# Sube el contenido de /dist a tu repositorio
```

### Servidor Personalizado
```bash
npm run build
# Sirve el contenido de /dist con cualquier servidor web
```

## 📊 Performance

### Optimizaciones Incluidas
- **Zero JS por defecto**: Astro renderiza HTML estático
- **Lazy loading**: Componentes se cargan cuando se necesitan
- **CSS optimizado**: Estilos críticos inline, resto lazy
- **Imágenes optimizadas**: Formato y tamaño apropiados

### Lighthouse Score Objetivo
- **Performance**: 95+
- **Accessibility**: 95+
- **Best Practices**: 95+
- **SEO**: 95+

## 🔧 Configuración Avanzada

### SEO
Personaliza el SEO en `src/layouts/Layout.astro`:

```astro
<Layout
  title="Tu Título"
  description="Tu descripción personalizada"
/>
```

### Analytics
Agrega Google Analytics en el layout:

```astro
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
```

### PWA (Opcional)
Para convertir en PWA, agrega:
- Service Worker
- Manifest.json
- Iconos appropriados

## 🐛 Troubleshooting

### Problemas Comunes

1. **Error de importación**
   ```bash
   # Verifica las rutas de importación
   # Usa aliases definidos en tsconfig.json
   ```

2. **Estilos no se aplican**
   ```bash
   # Verifica que el CSS esté en el componente correcto
   # Usa is:global para estilos globales
   ```

3. **JavaScript no funciona**
   ```bash
   # Verifica que uses <script> no <script is:inline>
   # Para scripts del cliente
   ```

## 🤝 Contribuir

1. Fork el proyecto
2. Crea una rama para tu feature
3. Commit tus cambios
4. Push a la rama
5. Abre un Pull Request

### Tipos de Commit
- `feat:` Nueva funcionalidad
- `fix:` Corrección de bugs
- `docs:` Actualización de documentación
- `style:` Cambios de formato
- `refactor:` Refactorización
- `perf:` Mejoras de performance

## 📄 Licencia

Este proyecto está bajo la Licencia MIT.

## 📞 Soporte

- **Issues**: [GitHub Issues](https://github.com/tu-repo/issues)
- **Documentación**: [Astro Docs](https://docs.astro.build/)
- **Comunidad**: [Astro Discord](https://astro.build/chat/)

---

**¡Buena suerte en la competición Formula SAE Electric! 🏎️⚡**

Built with ❤️ using [Astro](https://astro.build/)