# StudyPlanner 

## “Esta aplicación busca optimizar la organización académica mediante un sistema automatizado de priorización de tareas, utilizando arquitectura cliente-servidor y programación orientada a objetos.”


Una aplicación web para gestionar tareas académicas con:

- Registro de usuario

- Crear materias

- Agregar tareas

- Prioridad automática

- Alertas por vencimiento

- Estado (Pendiente / En progreso / Finalizada)

- Base de datos real

- Backend en Java

- Frontend dinámico con JS (DOM)

- POO bien aplicada

🧠 Arquitectura recomendada (Simple y funcional)
Backend → Java (Spring Boot idealmente)

API REST

CRUD de tareas

CRUD de materias

Conexión a base de datos (PostgreSQL o MySQL)

Frontend

HTML estructurado

CSS moderno (responsive)

JavaScript con fetch()

Manipulación del DOM

Validaciones

Base de datos

Tablas básicas:

🗂️ Tabla Usuario

id

nombre

email

password

📚 Tabla Materia

id

nombre

usuario_id

📝 Tabla Tarea

id

titulo

descripcion

fecha_entrega

estado

prioridad

materia_id

🧩 Parte POO en Java

Clases:

Usuario
Materia
Tarea

Con:

atributos privados

getters y setters

constructores

relaciones (OneToMany)

Eso en sustentación suma muchísimos puntos.

🌸 Funcionalidades clave (para que sea completo pero realizable)
1️⃣ Registro e inicio de sesión simple

(No necesitas JWT súper complejo si no hay tiempo)

2️⃣ Crear tarea

Formulario HTML → JS → fetch() → Java → BD

3️⃣ Mostrar tareas dinámicamente

JS recibe JSON y construye tarjetas con DOM:

function mostrarTareas(tareas) {
    const contenedor = document.getElementById("lista");
    contenedor.innerHTML = "";

    tareas.forEach(tarea => {
        const card = document.createElement("div");
        card.innerHTML = `
            <h3>${tarea.titulo}</h3>
            <p>${tarea.descripcion}</p>
        `;
        contenedor.appendChild(card);
    });
}

Eso demuestra manejo real del DOM.

🔥 Parte inteligente (que te hace ver top)

Que el sistema calcule prioridad automáticamente:

En Java:

if (diasRestantes <= 2) {
    tarea.setPrioridad("ALTA");
}

Y en frontend lo pintas rojo con CSS si es alta.

🎨 Diseño recomendado (simple pero profesional)

Dashboard limpio

Barra lateral

Cards para tareas

Colores suaves (azul académico + amarillo foco 👀)

🗺️ Plan realista contra el tiempo

Día 1 → BD + Backend base
Día 2 → CRUD funcional
Día 3 → Frontend + conexión
Día 4 → Diseño + validaciones
Día 5 → Ajustes y pruebas

💎 Luego actualización futura

Ahí sí:

Python

APIs externas

Notificaciones

IA que sugiera horarios

