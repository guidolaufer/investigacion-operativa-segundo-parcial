# Investigación Operativa · Segundo Parcial (UADE)

Portal estático de estudio, con estilos **integrados en cada archivo HTML**: funciona directamente desde la raíz de GitHub Pages sin instalar nada ni depender de la carpeta `assets/`.

## Abrir el portal

- Local: abrir `index.html`.
- GitHub Pages: Settings → Pages → Deploy from a branch → `main` → `/ (root)`.
- URL esperada: https://guidolaufer.github.io/investigacion-operativa-segundo-parcial/

## Contenido

1. Inventarios (`inventarios.html`): EOQ básico, protección, agotamiento, producción gradual, descuentos, ejercicios originales 3 y 4 y caso MediSupply.
2. Teoría de colas (`colas.html`): M/M/1, M/M/K, capacidad limitada, población finita, ejercicios 1 y 2 y caso MediSupply.
3. Decisiones (`decisiones.html`): Maximax, Wald, Laplace, Hurwicz, Savage, VE, VEIP, Bayes; ejercicios 5 y 6.
4. Simulación (`simulacion.html`): Monte Carlo, doble servidor y ejercicio original 7.
5. Formulario explicado (`formulario.html`): selector de fórmulas, supuestos y unidades.
6. Práctica (`practica.html`): ejercicios nuevos con soluciones desplegables.
7. Simulacro (`simulacro.html`): cuatro problemas para entrenar.
8. Documentos de referencia (`material-original/`): los archivos aportados por el estudiante, con sus posibles omisiones.

## Actualización desde una Mac

Si ya tenés el repositorio clonado y el ZIP en `~/Downloads`, estos comandos reemplazan los HTML y README pero **no borran** tus archivos originales:

```sh
cd ~/investigacion-operativa-segundo-parcial
unzip -o ~/Downloads/IO_Segundo_Parcial_Estudio_Completo.zip
# Revisá qué cambió:
git status --short
git add index.html inventarios.html colas.html decisiones.html simulacion.html formulario.html practica.html simulacro.html README.md .nojekyll
git commit -m "Ampliar teoria, guias y ejercicios resueltos del segundo parcial"
git push origin main
```

Si usás el ZIP **solo-web**, igualmente contiene todos los HTML, README y `.nojekyll`; mantené intacta `material-original/` en GitHub.

## Criterio pedagógico y limitaciones

Se basa en el documento de ejercicios original, el formulario de la cátedra y las fotos del caso MediSupply. La explicación teórica y los ejercicios creados para practicar son material de apoyo generado adicionalmente, no una transcripción del docente. Hay datos faltantes en el inciso 2(c) y una hipótesis explícita en 6(c), y la simulación 7 depende de la convención inversa exponencial elegida. No confundir promedio teórico con muestras de Monte Carlo de tres clientes.


## Entrenador interactivo offline (nuevo)

- Abrir `entrenador.html`: **20 recorridos** y **129 preguntas** de opción múltiple con corrección, pistas y resolución completa.
- Las cuatro categorías son inventarios, teoría de colas, decisiones y simulación Monte Carlo.
- Funciona **sin internet** porque el HTML incluye todas las preguntas, sus respuestas y los estilos/scripts. No requiere servidor, librerías, cuentas ni solicitudes de red.
- Se guarda el progreso en `localStorage` del mismo navegador y dispositivo, cuando el navegador lo permite. Desde un archivo local puede estar limitado en algunos navegadores; incluso entonces los ejercicios siguen funcionando en la sesión.
- Los 20 modelos cubren: EOQ, stock de seguridad, almacenamiento máximo, lote fijo, agotamiento, EPQ, descuentos, compra+producción, M/M/1, M/M/K, capacidad finita, fuente finita, Maximax/Wald/Laplace, Savage, Hurwicz, valor esperado, Bayes, Monte Carlo discreto, simulaciones con uno y dos servidores.
- Algunos casos son ejemplos didácticos creados para esta guía; otros se basan en ejercicios de la cátedra y están identificados. Los datos no especificados se declaran como supuestos.

### Publicación segura en el repo existente

Para actualizar solo la web, descomprimir `IO_Entrenador_Interactivo_Offline.zip` en la raíz del repositorio GitHub (al mismo nivel de `index.html`) y hacer `git add -A && git commit -m "Agregar entrenador interactivo offline" && git push origin main`. No borrar `material-original/`.

### Sin conexión

Si vas a estar **sin internet real**, descargá y descomprimí los archivos en tu computadora o celular *antes* de quedarte sin conexión. GitHub Pages es un sitio remoto; visitar una URL de GitHub Pages no garantiza acceso desconectado. Abrí el archivo `entrenador.html` localmente.
