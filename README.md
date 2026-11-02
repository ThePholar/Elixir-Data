# Política de Privacidad y Términos de Servicio de Elixir Data

**Última actualización:** 2 de noviembre de 2026  
**Desarrollador:** ThePholar  
**Contacto:** polarxd@icloud.com | Telegram: @thepholar  

Bienvenido a **Elixir Data**. Esta aplicación ha sido diseñada bajo una arquitectura **100% Offline-First**, priorizando la privacidad absoluta, la transparencia técnica y el control total del usuario sobre su dispositivo.

---

## 1. Principio Fundamental: Privacidad y Procesamiento Local

Elixir Data opera de manera estrictamente local:
* **Sin servidores externos:** La aplicación no cuenta con servidores centrales, bases de datos remotas ni puntos de conexión a la nube.
* **Cero rastreadores:** No se implementan kits de desarrollo de software (SDK) de analíticas, publicidad invasiva, rastreo de comportamiento ni herramientas de telemetría de terceros.
* **Sin recopilación de datos personales:** Elixir Data no solicita, registra, lee ni procesa información de identificación personal, listas de contactos, cuentas de usuario, fotos, ubicación geográfica ni contenido de navegación web.

---

## 2. Permisos del Sistema y Justificación Técnica

Para ofrecer métricas de consumo de red en tiempo real y resúmenes periódicos, Elixir Data requiere los siguientes permisos de Android:

### a) Acceso a Estadísticas de Uso (`PACKAGE_USAGE_STATS`)
* **Finalidad:** Este permiso especial permite que la aplicación consulte la API nativa de Android (`NetworkStatsManager`) para calcular la cantidad de bytes transferidos (subida y bajada) a través de las interfaces de Datos Móviles y Wi-Fi.
* **Uso:** Se utiliza exclusivamente para generar los resúmenes acumulados del ciclo mensual actual y del historial de meses pasados.
* **Protección:** Esta información se procesa y presenta únicamente en pantalla dentro del dispositivo. Jamás se comparte ni se transmite al exterior.

### b) Servicio en Primer Plano (`FOREGROUND_SERVICE` y `FOREGROUND_SERVICE_DATA_SYNC`)
* **Finalidad:** Mantener el monitor de tráfico activo en memoria para actualizar el contador de velocidad cada segundo.
* **Visibilidad:** Este servicio se ejecuta con una notificación persistente visible en la barra de estado y en la cortina de notificaciones, garantizando que el usuario siempre esté al tanto de que el monitor se encuentra en funcionamiento.

### c) Notificaciones (`POST_NOTIFICATIONS`)
* **Finalidad:** Requerido en versiones modernas de Android (Android 13 y superiores) para mostrar el indicador de velocidad en tiempo real y la alerta en caso de que el usuario supere su límite de datos móviles configurado voluntariamente.

### d) Iniciar al Encender el Dispositivo (`RECEIVE_BOOT_COMPLETED`)
* **Finalidad:** Permite que el servicio de monitoreo en segundo plano se reanude de manera automática tras reiniciar el teléfono, siempre y cuando la opción esté activada en los ajustes de la aplicación.

---

## 3. Almacenamiento de Preferencias

Cualquier configuración que establezcas (como el límite mensual de datos móviles, el encendido automático o el tema visual) se guarda de manera segura dentro del almacenamiento privado de la aplicación (`SharedPreferences`) en tu propio dispositivo. Al desinstalar la aplicación, todos estos parámetros se eliminan de forma permanente e irrecuperable.

---

## 4. Términos de Uso

1. **Uso de la Aplicación:** Elixir Data se distribuye con el propósito de brindar una herramienta de utilidad técnica para auditar y monitorear el consumo de red del propio usuario.
2. **Nivel de Servicio:** Las mediciones de velocidad y tráfico se basan en las lecturas provistas directamente por el sistema operativo Android. Si bien las APIs utilizadas son de alta precisión, los cálculos de tu operador de telefonía móvil pueden variar ligeramente según sus ciclos de facturación o políticas de redondeo.
3. **Licencia:** Elixir Data es proporcionada por ThePholar bajo un esquema de uso personal sin garantías implícitas, operando de conformidad con las políticas de privacidad locales.

---

## 5. Modificaciones a la Política

Cualquier cambio menor o actualización necesaria para adaptarse a nuevas normativas del sistema operativo Android se reflejará directamente en este repositorio público con la fecha de revisión correspondiente.

---

## 6. Canales de Contacto

Si tienes dudas técnicas, sugerencias o consultas sobre esta política de privacidad, puedes comunicarte a través de los canales oficiales del desarrollador:

* **Correo electrónico:** [polarxd@icloud.com](mailto:polarxd@icloud.com)
* **Telegram:** [@thepholar](https://t.me/thepholar)
* **Signal:** polar.2077

