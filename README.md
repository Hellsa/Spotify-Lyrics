# 🎵 Discord Spotify Lyrics Status

[![Node.js](https://img.shields.io/badge/Node.js-18%2B-339933?style=flat-square&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![Discord](https://img.shields.io/badge/Discord-Selfbot-5865F2?style=flat-square&logo=discord&logoColor=white)](https://discord.com)
[![Spotify](https://img.shields.io/badge/Spotify-API-1DB954?style=flat-square&logo=spotify&logoColor=white)](https://developer.spotify.com)
[![License](https://img.shields.io/badge/License-MIT-darkred?style=flat-square)](LICENSE)

> Sincroniza el estado de Discord con la letra en tiempo real de lo que escuchas en Spotify.  
> **Modo terminal visual** con figlet + colores personalizables.  
> **Anti‑ban pasivo** implementado por defecto.

## 📦 Features

- **Discord Status Sync**  
  Actualiza tu `custom status` con la línea actual de la canción.  
  Rotación automática cada 2‑3 segundos + jitter aleatorio.

- **Terminal Lyrics Mode**  
  Salida visual con letras ASCII (figlet) y color RGB modulable.  
  Modos incluidos: Arcoíris, Cian Neón, Matrix Verde, Rosa Neón.

- **Anti‑Ban Layer**  
  - Headers reales de navegador (User‑Agent rotativo).  
  - Cooldown dinámico entre 2 y 3 segundos.  
  - Jitter de ±500ms para simular latencia humana.  
  - No se usa API no oficial de Discord (solo `custom status`).

## 🛠️ Requirements

- Node.js **18.x** o superior
- npm o yarn
- Cuenta de Discord (**token de usuario**, no de bot)
- Aplicación en [Spotify Developer Dashboard](https://developer.spotify.com/dashboard) (Client ID + Secret)

## 🚀 Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/Hellsa/discord-spotify-lyrics.git
cd discord-spotify-lyrics
2. Install dependencies
bash
npm install
3. Environment configuration
Copia el archivo de ejemplo y edítalo:

bash
cp .env.example .env
Rellena los siguientes campos:

env
# Discord (user token, no bot token)
DISCORD_TOKEN=your_discord_user_token_here

# Spotify API credentials
SPOTIFY_CLIENT_ID=your_client_id
SPOTIFY_CLIENT_SECRET=your_client_secret
⚠️ Advertencia
El uso de tokens de usuario en Discord viola sus Términos de Servicio.
Este proyecto es solo para fines educativos. Úsalo bajo tu propia responsabilidad.

4. Run the script
bash
npm run start
⚙️ Modes & Customization
Al ejecutar el script se abrirá un menú interactivo con estas opciones:

Modo	Descripción
1. Discord Lyrics Status	Envía la letra actual a tu estado personalizado. Silencioso y pasivo.
2. Terminal Lyrics Mode	Muestra la letra en la consola con estilo visual. Ideal para streaming o segunda pantalla.
Terminal Mode settings
Color schemes: Arcoíris, Cian, Verde Matrix, Rosa.

Fonts: Standard, Big, Mini (recomendado para líneas largas).

📁 Project Structure
text
.
├── src/
│   ├── discord/      # Conexión y actualización de estado
│   ├── spotify/      # Cliente de Spotify Web API
│   ├── terminal/     # Figlet + colores + renderizado
│   └── utils/        # Anti‑ban, delays, jitter
├── .env.example
├── index.js
├── package.json
└── README.md
🧪 Troubleshooting
Problema	Posible solución
Invalid token	Verifica que el token de Discord sea de usuario (empieza por ND... o MD...). No uses token de bot.
Spotify 401	Regenera tu Client Secret en el dashboard de Spotify.
No se ve el estado en Discord	Revisa que tengas activada la opción Mostrar actividad actual en Ajustes de Discord > Actividad.
Letras demasiado largas	Cambia la fuente a Mini desde el menú.
📄 License & Contributions
Este proyecto se distribuye bajo la licencia MIT.
Ver el archivo LICENSE para más detalles.

Las contribuciones externas son bienvenidas mediante Pull Requests.

Al contribuir, aceptas que tu código pase a ser MIT licensed.

Para cambios grandes, abre primero un Issue para discutirlos.

👤 Author
Hellsa – GitHub

Hecho con ❤️ y caffeine. No afiliado a Discord Inc. ni a Spotify AB.