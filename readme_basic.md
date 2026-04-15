# Chatbot Multi-Modelo Local

## Requisitos

- [LM Studio](https://lmstudio.ai/) instalado
- 8 GB de RAM mínimo
- Navegador moderno (Chrome, Firefox, Edge)

---

## Pasos para hacerlo funcionar

### 1. Instalar LM Studio
Descargalo desde [lmstudio.ai](https://lmstudio.ai/) e instalalo normalmente.

### 2. Descargar un modelo
Dentro de LM Studio, buscá `qwen3-1.7b` con el ícono de lupa y hacé clic en **Download**.

### 3. Iniciar el servidor
1. Ir a la sección **Local Server** (ícono `<->` en el panel izquierdo).
2. Seleccionar el modelo descargado.
3. Hacer clic en **Start Server**.

### 4. Habilitar CORS
En el mismo panel del servidor, activar el toggle **"Enable CORS"**.
Sin esto, el chatbot no puede conectarse.

### 5. Abrir el chatbot
Abrí `chatbot.html` directamente en el navegador.
Si el indicador dice **"Conectado"** en verde, está todo listo.

---

## Agregar un modelo nuevo

Abrí `chatbot.html` y agregá una línea en el `<select>`:

```html
<option value="id-exacto-del-modelo-en-lmstudio">Nombre visible</option>
```

El ID exacto lo ves en LM Studio al seleccionar el modelo en el panel del servidor.

---

## Problemas comunes

| Problema | Solución |
|----------|----------|
| Indicador rojo "Desconectado" | Abrí LM Studio y hacé clic en Start Server |
| Error en consola del navegador | Verificá que CORS esté activado |
| Respuesta vacía | Asegurate de que haya un modelo cargado en el servidor |
