# Mi laboratorio de Terminal y Git

- Autor: Paula Paniagua
- Objetivo: contar cuantas pinzas hay en una lista de instrumentos y comprobar si son las 2 que se esperan.
- IA: he usado la IA para que me guiara paso a paso en los ejercicios en caso de tener alguna duda o consulta, o para mejorar la redacción de algunos apartados.

## Ejecucion

Desde la carpeta del repositorio, en Git Bash (Windows):

```bash
py src/recuento_matIA.py
```

Para guardar el resultado en el informe:

```bash
py src/recuento_matIA.py > resultados/informe_matIA.txt
```

## Comandos y analisis

- `>` guarda la salida en un archivo y borra lo que tenia antes. `>>` la añade al final sin borrar nada.
- `|` coge lo que sale de un comando y se lo pasa al siguiente. Por ejemplo, `grep -x "pinza" datos/instrumentos.txt | wc -l` primero busca las lineas que son "pinza" y luego las cuenta: salen 2.
- La tijera no suma porque el programa solo suma 1 cuando el instrumento es "pinza", ya que esa linea esta dentro del `if`. Si es "tijera", se la salta.
- El informe tiene 3 lineas: las pinzas que esperaba (2), las que ha contado el programa (2) y el resultado de compararlas (coincide).
- Guardar es escribir el archivo en el ordenador. `git add` lo prepara para la siguiente version. `git commit` guarda esa version en mi historial. `git push` la sube a GitHub.