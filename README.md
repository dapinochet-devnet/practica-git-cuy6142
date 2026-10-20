# practica-git-cuy6142
Repositorio de práctica de Git y GitHub – CUY6142

## Contenido
 
- pokeapi.py: consulta datos de un Pokémon en la API pública PokeAPI.
 
Ejecución: python3 pokeapi.py

- clima.py: consulta el clima actual de una ciudad usando la API de OpenWeather.

Ejecución:
export OPENWEATHER_API_KEY=tu_api_key
python3 clima.py


Agregare mi nombre y le daré commit

Mi nombre es Daniel y Apellido Pinochet :D

## Actividad 2: Rama secundaria, modificación y fusión

Objetivo: crear una rama secundaria, modificar `pokeapi.py` para que el usuario pueda consultar cualquier Pokémon y fusionar los cambios con la rama `main`.

### 1. Preparar el nuevo entorno de trabajo

```bash
cd ~
mkdir actividad2
cd actividad2
git clone https://github.com/dapinochet-devnet/practica-git-cuy6142.git
ls -l
cd practica-git-cuy6142
ls -la
git status
git log --oneline
```

### 2. Crear la rama secundaria y modificar el script

```bash
git checkout -b consulta-pokemon
git branch
nano pokeapi.py
python3 pokeapi.py
git status
git add pokeapi.py
git commit -m "Permite consultar cualquier Pokemon ingresado por el usuario"
git push -u origin consulta-pokemon
```

### 3. Sincronización y fusión con main

```bash
git checkout main
git pull
git merge consulta-pokemon
git push
git log --oneline --graph --all
git status
```

### 4. Validación

```bash
cat pokeapi.py
python3 pokeapi.py
```

Pokémon consultados: `charmander`, `bulbasaur`, `25` (Pikachu) y `pokefalso` (devuelve error 404 controlado). Se sale del programa escribiendo `salir`.
