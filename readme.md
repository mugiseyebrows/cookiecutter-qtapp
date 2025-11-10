# cookiecutter-qtapp

cookiecutter Qt app template

# use

1) Install cookiecutter
```bash
pip install cookiecutter
```

2) Generate project
```bash
cookiecutter https://github.com/mugiseyebrows/cookiecutter-qtapp.git --no-input project_name=MyApp copyright="John Doe"
```

3) Build
```bash
cd MyApp
mkdir Debug
cd Debug
cmake -G Ninja -DCMAKE_BUILD_TYPE=Debug ..
ninja
```