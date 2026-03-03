# Mnist Web

Aplicación web interactiva que permite configurar, entrenar y evaluar una red neuronal densamente conectada para la clasificación de dígitos manuscritos (MNIST), bajo una arquitectura desacoplada frontend-backend orientada a experimentación en Machine Learning.

---

## Proyecto Completo

Este repositorio corresponde únicamente al `frontend` del sistema.

La interfaz consume una API desarrollada en Django REST Framework encargada del entrenamiento del modelo, validación y generación de métricas de desempeño.

Video demostración: [Mnist Web - Video](https://www.youtube.com/watch?v=nCE3aq7qerM)  
Repositorio Backend: [Mnist Web - Backend](https://github.com/shaitansix/Mnist_Web-Backend)  
Repositorio Frontend: [Mnist Web - Frontend](https://github.com/shaitansix/Mnist_Web-Frontend)  

---

## Arquitectura del Sistema

Descripción general de la arquitectura del proyecto:

- **Frontend:** React + Vite
- **Backend:** Django REST Framework
- **Modelo de ML:** Red neuronal densa implementada con Keras
- **Dataset:** MNIST
- **DevOps / Herramientas:** Docker, Git, GitHub 

### Descripción adicional

El sistema sigue una arquitectura cliente-servidor donde el frontend permite configurar dinámicamente la arquitectura y los hiperparámetros del modelo antes de enviar la solicitud de entrenamiento al backend mediante HTTP.

Una vez entrenado el modelo, el usuario puede evaluar su desempeño utilizando imágenes del conjunto de prueba o dibujando manualmente un dígito en la interfaz para que el modelo lo clasifique en tiempo real.

El frontend gestiona el estado de configuración, resultados de entrenamiento e inferencia, renderizando dinámicamente métricas como accuracy y predicciones generadas por el modelo.

---

## Funcionalidades Principales

- Configuración dinámica de arquitectura (1 o 2 capas ocultas con 1 a 10 neuronas por capa).
- Ajuste de hiperparámetros: épocas, batch size, función de activación y tasa de aprendizaje.
- Definición configurable del tamaño de conjunto de prueba (test size).
- Entrenamiento del modelo bajo demanda desde la interfaz.
- Visualización del accuracy del modelo tras el entrenamiento.
- Inferencia sobre imágenes pertenecientes al conjunto de test.
- Clasificación en tiempo real de dígitos dibujados manualmente por el usuario.
- Comunicación frontend-backend mediante solicitudes HTTP asincrónicas.

---

## Aspectos Técnicos Destacados

- Integración de modelo de Deep Learning en arquitectura web desacoplada.
- Configuración dinámica de hiperparámetros desde interfaz gráfica.
- Entrenamiento del modelo mediante endpoints REST controlados.
- Implementación de flujo completo: entrenamiento → evaluación → inferencia.
- Procesamiento de imágenes dibujadas por el usuario para su clasificación.
- Separación clara entre lógica de ML (backend) y capa de presentación (frontend).
- Manejo de estado en React para representar configuraciones, métricas y resultados de predicción.
- Arquitectura extensible para experimentar con distintas configuraciones de red neuronal.

---

## Opciones de Despliegue

### Usando Docker

#### 1. Descargar la imagen
```bash
docker pull shaitansix/mnist_web-client:1
```

#### 2. Crear y ejecutar el contenedor
```bash
docker run --name mnist_web-client -e VITE_API_URL=http://localhost:8000 -p 5173:5173 shaitansix/mnist_web-client:1
```

#### 3. Acceder a la aplicación
```bash
http://localhost:5173/
```

### Usando git clone

#### 1. Crear carpeta de trabajo

#### 2. Clonar repositorio
```bash
git clone https://github.com/shaitansix/Mnist_Web-Frontend.git
cd Mnist_Web-Frontend
```

#### 3. Instalar dependencias
```bash
npm install
```

#### 4. Configurar variables de entorno
Crear un archivo `.env.development` en la raíz del proyecto:
```bash
VITE_API_URL=http://localhost:8000
```

#### 5. Ejecutar servidor de desarrollo
```bash
npm run dev
```

#### 6. Acceder a la aplicación
```bash
http://localhost:5173/
```
