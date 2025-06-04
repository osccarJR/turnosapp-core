# Sistema de Asignación de Turnos

Este sistema web desarrollado en **ASP.NET Core MVC 8.0** permite gestionar de forma automática y manual la asignación **semanal** de turnos laborales para los empleados. Utiliza **SQL Server** como base de datos y está preparado para ejecutarse localmente o desplegarse en Azure.

---

## 🧩 Funcionalidades principales

### 👤 Empleados
- Registro de **disponibilidad semanal**, seleccionando:
  - Días laborales disponibles (lunes a viernes).
  - Turno preferido (mañana, tarde o noche).
- Visualización de sus turnos asignados en la semana.
- Reserva manual de turnos disponibles, respetando:
  - Un máximo de 5 turnos por semana.
  - Un solo turno por día.
  - Disponibilidad real del turno (no debe estar ocupado).

---

### 🛠️ Administrador
- Generación automática de turnos semanales:
  - Se asignan turnos a todos los empleados.
  - Se respeta la disponibilidad registrada.
  - A quienes no registraron disponibilidad, se les asignan turnos aleatorios.
- Visualización detallada de todas las asignaciones:
  - Filtros por empleado, turno y semana.
- Eliminación de asignaciones específicas.
- Reinicio semanal, que borra:
  - Asignaciones, disponibilidades y logs.
- Visualización de logs de generación de turnos.

---

## 📥 Acceso al sistema

### 🔐 No se requiere contraseña  
Para iniciar sesión, **solo debes ingresar el correo**. El sistema detecta automáticamente si el usuario es administrador o empleado y redirige al panel correspondiente.

### Correos habilitados:

#### 👨‍💼 Administrador
- `admin@empresa.com`

#### 👩‍💼 Empleados
- `ana@empresa.com`
- `carlos@empresa.com`
- `juan@empresa.com`

---

## 🚀 ¿Cómo usar el sistema?

### 🧑‍💼 Empleado

1. Ingresar con su correo.
2. Registrar disponibilidad semanal (una vez por semana).
3. Consultar los turnos asignados desde **Mis Turnos**.
4. En caso de no tener turnos asignados, puede reservar manualmente los disponibles.

---

### 👨‍💼 Administrador

1. Ingresar con el correo del administrador.
2. Generar asignaciones semanales desde el panel principal.
3. Visualizar asignaciones semanales y aplicar filtros.
4. Eliminar asignaciones específicas si es necesario.
5. Consultar los logs de generación.
6. Reiniciar la semana cuando sea necesario.

---

## 🛠️ Tecnologías utilizadas

- ASP.NET Core MVC 8.0  
- Entity Framework Core  
- SQL Server  
- Razor Pages + Bootstrap 5  
- C#  

---

## 📌 Reglas y restricciones

- Solo se puede generar **una asignación semanal** por vez.
- Cada empleado puede tener **máximo 5 turnos por semana**.
- Solo **un turno por día** por empleado.
- Los turnos se asignan de acuerdo con la disponibilidad registrada, y de forma aleatoria si no se registra ninguna.
