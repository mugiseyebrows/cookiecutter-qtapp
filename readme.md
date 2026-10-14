# cookiecutter-qtapp

cookiecutter Qt application template

# use

1) Install cookiecutter
```bash
pip install cookiecutter
```

2) Generate project
```bash
cookiecutter https://github.com/mugiseyebrows/cookiecutter-qtapp.git
```

3) Build
```bash
cmake -G Ninja -B Debug -DCMAKE_BUILD_TYPE=Debug -DCMAKE_PREFIX_PATH=path/to/libs
cmake --build Debug

cmake -G Ninja -B Release -DCMAKE_BUILD_TYPE=Release -DCMAKE_PREFIX_PATH=path/to/libs
cmake --build Release
```