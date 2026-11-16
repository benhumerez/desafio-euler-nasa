# Simulador NASA 1962 — Métodos Numéricos

Aplicación educativa para comparar Euler explícito, Heun, RK4 y la solución analítica de un modelo vertical simplificado de cohete.

## Ejecutar
1. Descomprimir el proyecto.
2. Abrir `index.html` en Chrome, Edge o Firefox.
3. Modificar los parámetros y pulsar **Ejecutar simulación**.

No necesita instalar dependencias ni conexión a Internet.

## Modelo
m dv/dt = T - mg - kv
dv/dt = a - b v, donde a = T/m - g y b = k/m
dy/dt = v

Condiciones iniciales: v(0)=0, y(0)=0.

Solución analítica:
v(t) = (a/b)(1 - exp(-bt))
y(t) = (a/b)t - (a/b²)(1 - exp(-bt))

Para k=0 se utiliza el caso límite v(t)=a*t; y(t)=0.5*a*t².

## Métodos
- Euler explícito para velocidad y posición.
- Heun (Euler mejorado).
- Runge-Kutta de cuarto orden (RK4).
- Solución analítica para comparación.

## Publicar en GitHub Pages
1. Crear un repositorio público en GitHub.
2. Subir `index.html` y `README.md`.
3. Ir a Settings > Pages.
4. En Build and deployment, seleccionar Deploy from a branch.
5. Elegir `main` y `/ (root)`, guardar.
6. GitHub mostrará la URL pública de la página.

## Limitaciones
Modelo académico: masa, empuje, gravedad y coeficiente de resistencia constantes; movimiento vertical; resistencia lineal. No representa el modelo oficial de ningún lanzamiento NASA ni sirve para diseño aeroespacial real.
