# 📱 Centro de Cumplimiento y Políticas - Asistente de Personas MÍA (Prodeman S.A.)

Este repositorio contiene el **Centro de Políticas de Cumplimiento Legal** para la aplicación **Asistente de Personas MÍA**, un chatbot conversacional integrado mediante la API Cloud de WhatsApp Business para atender consultas del área de Recursos Humanos de **Prodeman S.A.**

El portal ha sido diseñado para funcionar como un sitio estático e independiente, ideal para ser publicado de forma pública, gratuita y segura a través de **GitHub Pages**, cumpliendo estrictamente con los requisitos de verificación exigidos por **Meta Developers**.

---

## 🎨 Concepto Visual y UI
El diseño del portal implementa los lineamientos corporativos detallados en el documento de identidad visual de Prodeman:
* **Estilo Principal:** *Glassmorphism Premium* en Modo Oscuro (fondos semi-transparentes, desenfoque de fondo mediante `backdrop-filter: blur(16px)`, bordes suaves iluminados y sombras profundas).
* **Color Primario (Acento):** Rojo Prodeman (`#8c333d`).
* **Tipografía:** *Inter* importada desde Google Fonts para una legibilidad óptima sobre fondos difuminados.

---

## 📂 Estructura del Repositorio

La estructura del proyecto está organizada para soportar rutas amigables y limpias sin extensiones `.html` al publicarse:

```
/ (raíz del repositorio)
├── index.html                  # Portal principal y landing del Centro de Políticas
├── privacy/
│   └── index.html              # Política de Privacidad (accesible mediante /privacy)
├── terms/
│   └── index.html              # Términos y Condiciones de Uso (accesible mediante /terms)
└── src/
    ├── styles.css              # Hoja de estilos globales (Glassmorphism + Branding)
    └── assets/
        └── MIA Icon.png        # Icono identificatorio del chatbot MÍA
```

---

## 🚀 Guía de Despliegue en GitHub Pages

Para publicar este portal de políticas en pocos pasos y obtener las URLs públicas HTTPS obligatorias para Meta:

1. **Subir el código a GitHub:**
   Crea un nuevo repositorio público en GitHub (ej. `politicas-mia`) y empuja esta estructura de archivos a la rama principal (`main` o `master`).

2. **Habilitar GitHub Pages:**
   * Ve a la pestaña **Settings** (Configuración) de tu repositorio en GitHub.
   * En el menú lateral izquierdo, haz clic en **Pages**.
   * En la sección *Build and deployment*, bajo **Source**, selecciona **Deploy from a branch**.
   * Bajo **Branch**, selecciona tu rama principal (ej. `main`) y la carpeta raíz `/ (root)`.
   * Presiona **Save** (Guardar).

3. **Verificar URL:**
   Tras unos segundos, GitHub generará tu URL pública con protocolo HTTPS seguro. El formato de la URL será:
   ```text
   https://<tu-usuario-o-organizacion>.github.io/<nombre-del-repositorio>/
   ```

---

## ⚙️ Configuración en Meta Developers (WhatsApp Cloud API)

Una vez desplegado el portal, debes registrar los enlaces HTTPS en la consola de configuración de tu aplicación de Meta:

1. Ingresa a [Meta for Developers](https://developers.facebook.com/) e inicia sesión.
2. Selecciona la aplicación correspondiente al **Asistente de Personas MÍA**.
3. En el menú lateral, dirígete a **Configuración** > **Básica**.
4. Completa los siguientes campos obligatorios para pasar la revisión de Meta:
   * **URL de la política de privacidad:** 
     `https://<tu-usuario>.github.io/<tu-repositorio>/privacy/`
   * **URL de las condiciones del servicio:** 
     `https://<tu-usuario>.github.io/<tu-repositorio>/terms/`
5. Guarda los cambios. Con esta configuración estructurada en directorios, Meta validará los enlaces correctamente sin redirecciones ni requerimiento de login.

---

## 📄 Resumen de los Documentos Legales

### 1. Política de Privacidad
* **Objetivo:** Informar con transparencia sobre el tratamiento de datos personales en el chatbot.
* **Aspectos clave:** Detalla la recopilación de número de teléfono y contenido de consultas, el rol de Meta como intermediario técnico, los derechos ARCO de acceso y supresión, y el almacenamiento seguro.
* **Declaración expresa:** **No se venden datos** ni se utilizan con fines comerciales o de publicidad externa no consentida.

### 2. Términos y Condiciones de Uso
* **Objetivo:** Definir las reglas de interacción y límites de responsabilidad.
* **Aspectos clave:** Carácter puramente informativo de las consultas (no reemplaza asesoría profesional), flujo de atención automatizada y escalado a soporte humano, y causales de suspensión por uso indebido.

---

## 📬 Contacto y Soporte Legal
Para cualquier duda, actualización legislativa o solicitud de ejercicio de derechos ARCO:
* **Responsable:** Prodeman S.A.
* **Contacto del Área de Personas:** [rrhh@prodeman.com.ar](mailto:rrhh@prodeman.com.ar)