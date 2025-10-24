# Php-project

# 🎬 Próxima Película de Marvel (MCU)

Aplicación web simple en PHP que muestra información sobre la próxima película del Universo Cinematográfico de Marvel (MCU) utilizando la API de [whenisthenextmcufilm.com](https://whenisthenextmcufilm.com/).

## 📋 Descripción

Este proyecto consume una API pública para obtener y mostrar:
- **Título** de la próxima película de Marvel
- **Póster** oficial
- **Fecha de estreno**
- **Días restantes** hasta el estreno con mensajes personalizados en español
- **Siguiente producción** en la línea de tiempo de Marvel

## 🚀 Características

- ✨ Diseño responsive con [Pico CSS](https://picocss.com/)
- 🌓 Soporte para modo claro y oscuro automático
- 🎯 Mensajes dinámicos según la proximidad del estreno:
  - "Hoy se estrena" (día del estreno)
  - "Mañana se estrena" (1 día antes)
  - "Se estrena esta semana" (menos de 7 días)
  - "Se estrena este mes" (menos de 30 días)
  - "Se estrena en X días" (más de 30 días)
- 🏗️ Arquitectura orientada a objetos con PHP 8+
- 📦 Separación de responsabilidades (clases, funciones, templates)


## 🛠️ Requisitos

- PHP 8.0 o superior
- Extensión `php-json` habilitada
- Conexión a internet (para consumir la API)

## 📦 Instalación y Uso

```bash
# Clona el repositorio
git clone <url-del-repositorio>
cd nextmcu-movie

# Inicia un servidor PHP local
php -S localhost:8000

# Abre tu navegador en
# http://localhost:8000
```

## 🌐 API Utilizada

**Endpoint:** `https://whenisthenextmcufilm.com/api`

**Ejemplo de respuesta:**

```json
{
  "title": "Thunderbolts*",
  "release_date": "2025-05-02",
  "days_until": 190,
  "poster_url": "https://...",
  "overview": "A group of supervillains...",
  "following_production": {
    "title": "The Fantastic Four: First Steps"
  }
}
```


## 📝 Notas Técnicas

- Utiliza `declare(strict_types=1)` para tipado estricto en PHP
- Implementa el patrón de diseño Factory con `fetch_and_create_movie()`
- Usa `match` expressions (PHP 8+) para lógica condicional más limpia
- Renderizado de templates mediante `extract()` y `require`

## 📄 Licencia

Este proyecto es de código abierto y está disponible bajo la licencia MIT.

## 🙏 Créditos

- API proporcionada por [When is the next MCU film?](https://whenisthenextmcufilm.com/)
- Framework CSS: [Pico CSS](https://picocss.com/)
- Datos de películas: Marvel Studios


```bash
# Reportar un bug
gh issue create --title "Bug: descripción" --body "Detalles del problema"
```

