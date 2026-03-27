🚀 Guía de Instalación desde Cero

Para que este bot funcione en tu red MeshCore, sigue estos pasos en el orden indicado:
1. Preparar Home Assistant con HACS

Si aún no tienes HACS (Home Assistant Community Store), es el primer paso obligatorio para instalar integraciones personalizadas:

    Instala el complemento Terminal & SSH desde la tienda oficial de Home Assistant.

    Ejecuta el comando de instalación de HACS

    Reinicia Home Assistant y añade la integración de HACS desde Ajustes > Dispositivos y servicios.

2. Instalar la integración de MeshCore

Una vez tengas HACS:

    Ve a HACS > Integraciones y pulsa en los tres puntos (arriba a la derecha).

    Selecciona Repositorios personalizados.

    Pega la URL del repositorio oficial de MeshCore para Home Assistant.

    Una vez añadido, instálalo y reinicia de nuevo Home Assistant.

3. Conectar tu Nodo (Hardware)

El bot necesita "oír" la radio. Tienes dos opciones principales:

    Vía Serial (USB): Conecta tu radio (T-Beam, Heltec, etc.) al puerto USB del equipo donde corre Home Assistant.

    Vía Red (Wi-Fi/Ethernet): Si tu nodo está en la misma red local, asegúrate de que tenga habilitada la comunicación por API/JSON.

Ve a Ajustes > Dispositivos y servicios > Añadir integración y busca MeshCore. Sigue los pasos para vincular tu nodo específico.
4. Crear los Ayudantes (Helpers)

El bot necesita "memoria" para las estadísticas. Ve a Ajustes > Ayudantes y crea:

    Número: mesh_mensajes_dia (0 a 10000).

    Número: mesh_nodos_nuevos_dia (0 a 500).

5. Configurar el Código del Bot

    Abre tu archivo automations.yaml (puedes usar el complemento File Editor o VS Code).

    Copia y pega el código de este repositorio.

    Importante: Revisa que el channel_idx sea el que uses para datos en tu zona.

    Guarda y pulsa en Herramientas para desarrolladores > YAML > Automatizaciones para recargar los cambios sin reiniciar.

⚠️ Notas de Seguridad

    Delay: El código incluye un delay: 00:00:01 (1 segundo). No lo quites; es vital para que la radio tenga tiempo de pasar de modo recepción a transmisión sin colisionar con otros mensajes.
