---
Fecha_creación: 2024-08-25
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---
# Entonor virtual Con Pyenv
1. `curl https://pyenv.run | bash`
```bash
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"


#reiniciamos
source ~/.bashrc  # o ~/.zshrc, dependiendo de tu shell
```
2. instalamos:
	- Version de python que necesitamos `pyenv install 3.9.2`
	- Para crear un entorno virtual, usa el siguiente comando
		- `pyenv virtualenv 3.9.2 nombre_del_entorno`
	- Para activar el entorno virtual, usa el siguiente comando
		- `pyenv activate nombre_del_entorno`
	- pyenv deactivate
# Entorno virtual con [[Poetry]]
version:3.11.4
1. 
```python
pip install langchain
pip install jupyter lab
pip install python-dotenv
```

4. Archivos ocultos carpeta config con variables de entorno.