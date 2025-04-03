🏆 H-2 (ENVIAR UN DIRECTORIO VACIO AL REPOSITORIO REMOTO)

| Hacks   | Details |
|----------|------|
| H-2	    | 	Enviar un directorio vacio al repositorio remoto   |

1. Crear un nuevo repositorio en github nombre:`git_h_2`.

2. Crear un repositorio local
git init

3. Registrar el repositorio remoto con tú repositorio local
git remote add origin (pegar_la_ruta_del_repositorio_local)

4. Verificamos la ruta remota
git remote -v

5. Crear 1 carpeta ó directorio con el nombre de "usuarios"
mkdir usuarios

6. Verificar la creación del directorio
ls -l

7. Ahora si haces un status del stage
git status

8. La carpeta no aparece en el stage, es decir la vez creada, pero en git es como que no la reconoce, esto es debido a que git no hace seguimiento a directorios vacios.
En este momento es necesario elaborar un archivo interno en el directorio "usuarios", pero si por los momentos no queremos agregar nada en ella, pero si tenerla en nuestro repositorio debemos crear un archivo oculto dentro del directorio.
cd usuarios
touch .gitkeep
cd ..
ls -l

9. Examinamos el stage y debemos ver la carpeta ó directorio usuarios disponible para el tracking
git status

10. Agregamos el directorio al stage
git add .

11. Se realiza el commit
git commit -m "feat: add directory usuarios"

12. Verificamos el commit
git log --oneline

13. Crear el ambiente main
git branch -M main

14.Hacer push
git push -u origin main

15.Toca ir al repositorio remoto y ver la carpeta en nuestro repo
