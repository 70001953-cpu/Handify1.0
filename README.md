# 🤚 Handify — Lengua de Señas Peruana (LSP)

> Aplicación web de reconocimiento de señas en tiempo real usando Inteligencia Artificial. Completamente gratuita, open source y sin servidores.

![Handify](https://img.shields.io/badge/version-1.0.0-52b788?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)
![TensorFlow](https://img.shields.io/badge/TensorFlow.js-4.10-orange?style=flat-square)
![Multiplataforma](https://img.shields.io/badge/plataforma-Web%20%7C%20Mobile%20%7C%20Desktop-purple?style=flat-square)

---

## ✨ Características

- 🎥 **Detección en tiempo real** — Reconoce señas LSP directamente desde la cámara
- 🤖 **IA integrada** — TensorFlow.js + MediaPipe HandPose (sin servidor, 100% local)
- 📖 **Diccionario LSP** — Base de datos de 50+ señas con categorías
- 📚 **Modo Aprender** — Guía visual interactiva por categorías
- ✋ **Modo Enseñar** — Agrega tus propias señas al diccionario
- 🔊 **Síntesis de voz** — Escucha las señas detectadas (Web Speech API)
- 🌙 **Modo oscuro** — Tema claro/oscuro persistente
- 📱 **Multiplataforma** — PC, laptop, tablet y celular
- 🔒 **100% Privado** — Sin servidores, sin login, sin tracking

---

## 🗂️ Categorías incluidas

| Categoría | Señas |
|-----------|-------|
| 👋 Saludos | Hola, Adiós, Gracias, Por favor, ¿Cómo estás?... |
| 🔢 Números | 1 al 5 |
| 🏃 Verbos | Comer, Beber, Dormir, Caminar, Hablar, Ver... |
| 🐾 Animales | Perro, Gato, Pájaro, Pez, Caballo, Vaca |
| 👨‍👩‍👧 Familia | Mamá, Papá, Hermano, Hermana, Abuelo, Abuela |
| 🎨 Colores | Rojo, Azul, Verde, Amarillo, Negro, Blanco |

---

## 🚀 Cómo usar

### Opción 1 — GitHub Pages (recomendado)
1. Haz fork de este repositorio
2. Ve a **Settings → Pages**
3. Selecciona `main` branch y carpeta `/root`
4. ¡Listo! Tu URL será `https://tu-usuario.github.io/handify`

### Opción 2 — Local
```bash
git clone https://github.com/tu-usuario/handify.git
cd handify
# Abre index.html en tu navegador
# O usa un servidor local:
npx serve .
# o
python3 -m http.server 8080
```

> ⚠️ **Nota:** Para que funcione la cámara localmente, necesitas usar `localhost` o HTTPS. No funciona con `file://`.

---

## 🧠 Stack Tecnológico

| Tecnología | Uso |
|-----------|-----|
| **TensorFlow.js 4.10** | Motor de IA para detección de manos |
| **MediaPipe HandPose** | Modelo de 21 puntos clave de la mano |
| **Web Speech API** | Síntesis de voz en español |
| **Canvas API** | Renderizado de landmarks en tiempo real |
| **LocalStorage** | Base de datos local del diccionario |
| **HTML5 / CSS3 / JS ES6+** | Sin frameworks, código puro |

---

## 📁 Estructura del proyecto

```
handify/
├── index.html          # App principal
├── css/
│   └── style.css       # Estilos (tema claro/oscuro, responsive)
├── js/
│   ├── db.js           # Base de datos LSP + CRUD LocalStorage
│   ├── detector.js     # Motor de detección IA (TensorFlow)
│   └── app.js          # Controlador principal de la app
└── README.md
```

---

## 🔧 Agregar nuevas señas

### Desde la app (Modo Enseñar)
1. Ve a la pestaña **Detectar**
2. Selecciona modo **📚 Enseñar**
3. Completa el nombre, categoría y descripción
4. Haz clic en **Capturar muestra**

### Desde el código (`js/db.js`)
```javascript
{ 
  id: 's99', 
  name: 'Nueva seña', 
  category: 'Mi categoría', 
  emoji: '🤟', 
  description: 'Descripción del gesto', 
  tips: 'Consejo para hacerlo bien',
  handShape: 'open',  // open, closed, v, thumb, index, flat, pinch...
  custom: false 
}
```

---

## 🌐 Compatibilidad

| Navegador | Soporte |
|-----------|---------|
| Chrome 80+ | ✅ Completo |
| Firefox 78+ | ✅ Completo |
| Safari 14+ | ✅ Completo |
| Edge 80+ | ✅ Completo |
| Chrome Mobile | ✅ Completo |
| Safari iOS | ✅ Con HTTPS |

---

## 🗺️ Roadmap

- [ ] Soporte para alfabeto LSP completo (A-Z)
- [ ] Modo entrenamiento con captura de gestos reales
- [ ] Exportar/importar diccionario personal (JSON)
- [ ] Modo frase completa (combinar señas)
- [ ] Historial persistente entre sesiones
- [ ] PWA / instalable como app
- [ ] Soporte multilenguaje (ASL, BSL)
- [ ] Video tutoriales por seña

---

## 🤝 Contribuir

1. Fork del repositorio
2. Crea tu rama: `git checkout -b feature/nueva-seña`
3. Commit: `git commit -m 'Agrega seña X a la categoría Y'`
4. Push: `git push origin feature/nueva-seña`
5. Abre un Pull Request

---

## 📄 Licencia

MIT © 2024 — Handify

---

<div align="center">
  Hecho con ❤️ para la comunidad sorda peruana 🇵🇪
</div>
