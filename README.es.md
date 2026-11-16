# IA bajo tu control

[![Tu IA bajo control](guia/assets/banner-es.jpg)](https://inematds.github.io/ia-sob-seu-controle/guia/es/)

**🇧🇷 [Português](README.md) · 🇺🇸 [English](README.en.md) · 🇪🇸 [Español](README.es.md)**

## Qué es

Kit educativo gratuito de INEMA para elegir dónde funciona tu IA, quién recibe tus datos y cómo verificar una entrega. Inspirado en el análisis de la clase “The 5 Levels of Uncensored AI”, distingue la libertad de respuesta, la privacidad y la precisión. Incluye un análisis original, un ejercicio ficticio con respuesta conocida, una ficha de decisión y un verificador sin conexión. No instala modelos, no llama a API y no sustituye las pruebas de tu configuración real.

## Guía de uso

**https://inematds.github.io/ia-sob-seu-controle/guia/es/**

## Empezar

Python 3.10+ y Git, sin dependencias externas.

```bash
git clone https://github.com/inematds/ia-sob-seu-controle.git
cd ia-sob-seu-controle
python3 -m unittest discover -s tests -v
python3 scripts/conferir.py kit/exemplos/ficha.json
```

El ejemplo empieza incompleto y devuelve `invalida` (código 2). Abre `kit/exemplos/ficha.json` en un editor: completa el modelo y los campos, y marca las evidencias solo después de verificarlas. `revisar` (código 1) indica que hay algo pendiente; `ficha-conferida` (código 0) indica coherencia declarada, no una certificación. Aún hay que leer los avisos. En Windows, `py` puede sustituir a `python3`.

## El proceso, de principio a fin

1. Lee el [análisis](../../docs/ANALISE.md) y elige lo que necesitas.
2. Completa la [ficha](../../kit/exemplos/ficha.json) con la configuración que pretendes usar.
3. Ejecuta la tarea con el [informe ficticio](../../kit/exemplos/relatorio-ficticio.md) en la aplicación de IA que hayas elegido.
4. Entrega los datos y el resultado al [revisor](../../kit/prompts/revisor.md) y compáralos con la referencia.
5. Si necesitas trabajar sin conexión, haz la prueba con la red desconectada después de descargar el modelo.
6. Registra las evidencias y ejecuta el verificador.

## Límites

El verificador solo lee JSON local y valida las decisiones declaradas. No inspecciona la red, el modelo, el hardware ni los archivos del usuario. No mide la calidad de la IA, no garantiza que no haya filtraciones y no instala software. El código es independiente del idioma de la guía; los archivos del kit y sus mensajes están en portugués (en portugués).

## Fuente

[The 5 Levels of Uncensored AI — Jack Roberts](https://youtu.be/FbiOr73tRPk), clase publicada el 15/11/2026. Análisis original y enlaces a la documentación, sin reproducir materiales privados.

MIT para el código y los textos originales de este proyecto. Las marcas y los materiales externos pertenecen a sus respectivos autores.
