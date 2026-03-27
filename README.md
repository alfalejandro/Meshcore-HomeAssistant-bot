# Meshcore-HomeAssistant-bot
Bot comunitario para la malla MeshCore. Comandos de utilidad y estadísticas

# 🤖 MeshCore Community Bot

Este repositorio contiene la configuración de **Home Assistant** para el bot comunitario de la malla.

## 📡 Características
- **Canal de operación:** 6 (Data/Bot)
- **Delay de cortesía:** 1 segundo en todas las respuestas para evitar colisiones.

## 🛠️ Comandos Disponibles
* `.help`: Resumen de acciones 
* `.ping o .test`: Info de latencia y ruta.
* `.quien [byte]`: Identifica un nodo por su ID de ruta.

( < 133 caracteres).

## 📊 Estadísticas Automáticas
El bot envía un reporte diario a las **22:00h** con el tráfico de mensajes y los nodos nuevos detectados durante el día.
Si recibe un nodo con menos del 30% de batería, envía una alerta.
