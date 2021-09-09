# juliashellutils
Julia shell utilities scripts

```
julia-listp : list Project.toml files (or Manifest.toml)

Usage julia-listp [-h|--help] [-q] [-p|-m|-ph|-pa|-r|-pk]
      -p  : show Projects.toml (default)
      -m  : show Manifests.toml
      -r  : raw path ouput
      -ph : use $HOME instead of ~
      -pa : abs paths : subsistute value of $HOME to ~
      -pk : show paths inside .julia/packages
```

```
julia-list-repo-url : list all external repos used (eg dev'ed or add'ed unregistred packages)

Usage /home/davidj/bin/julia-list-repo-url [-h|--help] [-v]
      -v  : show also source file/line
```
