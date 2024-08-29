# llm_JoseLuis
Repositorio de prueba para implementar LLM y una aplicación web.

Repositorio de trabajo con modelos de lenguaje largo usando ollama
# 1. Instalación

Cómo primer paso descargamos [ollama](https://ollama.com/download/linux) de su página web, y ejecutamos el siguiente comando:
 
 ````bash
 $ curl -fsSL https://ollama.com/install.sh | sh
 ```` 
# 2. Ejecutar el servidor

Ejecutar el servidor de API REST de ollama con el siguiente comando:

````bash
$ ollama serve
````

## 3. Descargar un modelo

En la página de ollama descarga un [modelo](https://ollama.com/library) utilizando el siguiente comando:

````bash
$ ollama run tinyllama
````

## 4. Reliazar un request a la API REST con stream

Para realizar una consulta utilizamos el comando curl como se muestra en el siguiente ejemplo:

````bash
curl -X POST http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?"
}'
````

## 5. Reliazar un request sin stream

Para realizar una consulta a la API REST sin stream se hace de la siguiente forma:

````bash
curl -X POST http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?",
  "stream": false
}'
````

## 6. Formas de guardas cambios al Readme.md

git add .

git commit -m "UPDATED README.md"

git push -u origin main


