# Descripciones Procedurales del Sistema

## 1.Llenado de ficha de reporte de sesión 
*Responsable:* Terapeuta  

### Happy Path
   1. El usuario inicia sesión con sus credenciales válidas.
   2. Navega al expediente del paciente correspondiente.
   3. Selecciona la opción “Agregar reporte de sesión”.
   4. Se presenta un formulario con campos como:
      - Fecha de sesión  
      - Diagnóstico o motivo  
      - Intervenciones aplicadas  
      - Recomendaciones  
      - Observaciones adicionales
   5. Llena todos los campos requeridos.
   6. El sistema valida los datos.
   7. Guarda el reporte asociado al expediente.
   8. Muestra confirmación del registro exitoso.

### Excepciones
   - *Campos vacíos:* El sistema impide guardar si hay campos vacios.
   - *Formato inválido:* Se muestra un mensaje de error.  
   - *Error de red:* Se notifica el fallo y se sugiere reintentar.



## 2. Imprimir documentos del expediente
*Responsable:* Administrador  

### Happy Path
   1. El administrador accede al módulo de expedientes.
   2. Selecciona el expediente deseado.
   3. Visualiza el contenido del expediente
   4. Selecciona la opción de imprimir.
   6. Confirma e imprime.
   7. El documento es enviado a la impresora.

### Excepciones
   - *Sin documentos:* Se indica que no hay documentos para imprimir.  
   - *Error de impresión: Se despliega mensaje de error.  
   - *Permisos insuficientes: Se restringe la función.

---

## 3. Gestión del estado del expediente
*Responsable:* Administrador  

### Happy Path
   1. El administrador abre el expediente.
   2. Visualiza el estado actual.
   3. Selecciona “Modificar estado”.
   4. Elige un nuevo estado:  
      - En espera  
      - Activo  
      - Finalizado
   5. El sistema guarda el cambio.
   6. Confirma visualmente la actualización.

### Excepciones
   - *Cambio no permitido:* Se impide reactivar un expediente finalizado. 

---

## 4. Visualización del checklist del expediente
*Responsable:* Administrador  

### Happy Path
   1. El usuario accede al expediente.
   2. Se muestra checklist con documentos requeridos.
   3. Cada ítem indica:  
      - (X) Completado  
      - ( ) Pendiente
   4. El sistema actualiza el checklist según se vayan cumpliendo.

### Excepciones
   - *Falta de documentos: Se marcan en rojo.  
   - *Expediente cerrado:* El checklist no es editable.

---

## 5. Carga de archivos al expediente
*Responsable: Terapeuta

### Happy Path
   1. El terapeuta accede al expediente.
   2. Selecciona “Cargar documento”.
   3. Abre el explorador de archivos.
   4. Elige un archivo válido (.pdf, .jpg, .png).
   5. Se carga y asocia al expediente.
   6. Se registra en bitácora.
   7. Muestra notificación de éxito.

### Excepciones
   - *Tipo de archivo no valido Se cancela la carga en caso de ser un documento en formato no valido
   - *Archivo muy grande: Se rechaza el archivo.  
   - *Permisos insuficientes:* Se impide el acceso.

---

## 6. Archivar expedientes finalizados
*Responsable:* Administrador  

### Happy Path
   1. Accede a expedientes expedientes.
   2. Selecciona el expediente a archivar.
   3. El sistema valida que está completo.
   4. Lo mueve a “Archivados”.
   5. Bloquea futuras ediciones.
   6. Registra la acción.

### Excepciones
   - *Ya archivado: Se evita la acción duplicada.  
   - *Documentos faltantes:* Se impide archivar.  
   - *Error técnico:* Se muestra mensaje y opción de reintento.