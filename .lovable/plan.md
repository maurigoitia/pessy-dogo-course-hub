# Comprobación de acceso y destino — resultado (sin cambios de código)

## Resultado
- Destino de este proyecto: repositorio interno de Lovable (privado). La rama de trabajo actual es una rama de edición de Lovable. El repo público `maurigoitia/pessy-dogo-course-hub` responde como público (HTTP 200). Si Git sync está conectado a ese repo, todo lo que se escriba aquí termina publicado. **Destino NO seguro para código de PessyDOGO.**
- Lectura de origen `maurigoitia/PessyDOGO@lovable-stores`: **FALLÓ**. HTTP 401 "Bad credentials" en la conexión "Mauricio's GitHub API" (es una clave API, no OAuth). Hubo un solo reintento, con `/user`, que también dio 401. No se verificó ningún archivo: ni package.json, ni ExportReportModal.tsx, ni PetHomeView.tsx, ni homeDecisionEngine.ts.
- Capacidad del editor: este proyecto corre sobre TanStack Start / Workers y solo tiene Git sync con un repo nuevo. No puede vincularse a una rama existente como `lovable-stores` ni abrir un PR contra ella. Esto es un límite de funcionamiento del editor, no falta de código. Una alternativa válida sin migrar el stack: leer con la conexión privada y devolver cambios como commits o PR a `lovable-stores` desde la API de GitHub, sin pasar por este proyecto ni por el repo público. Para eso hace falta una credencial válida.

## Único paso seguro para avanzar
El propietario actualiza la credencial de "Mauricio's GitHub API" en el formulario seguro de conectores:
https://lovable.dev/dashboard?connectors=&connector=github&workspace=kdr4baAIxJawP74UrYPu

Permiso mínimo: un token fine-grained limitado solo al repo `maurigoitia/PessyDOGO`, con Contents: Read and write, Pull requests: Read and write y Metadata: Read.

## Después de aprobarlo (próximo turno)
1. Leer solo los nombres del árbol de `lovable-stores` y confirmar los 4 archivos.
2. No usar este proyecto ni el repo público como destino. Los cambios se entregan como rama o PR en PessyDOGO a través de la API.
3. Recién entonces, planificar la entrega vertical de Hoy y el PDF.
