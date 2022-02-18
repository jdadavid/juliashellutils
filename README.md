# juliashellutils
Julia shell utilities scripts

```
julias : Julia launcher wrapper for using local JuliaSysimage.[dll|so] if its exists and is up to date
Usage : julias : [+h] [+v|+q] [+f] [+J juliax] [julia_options] file.jl [args]
launch Julia with sysimage "JuliaSysimage.[dll|so]" if found
   +h : this help
   +v : verbose
   +q : quiet (no warning about out of date)
   +f : force use of sysimage even if out of date
   +J juliax : use juliax executable for julia
```

```
juliad : launches Julia daemon server (if necessary),  and client, to execute julia file with reduced TTFX
#  wraps excellent DaemonMode by @dmolima (see https://github.com/dmolina/DaemonMode.jl)
#  You must have "using DaemonMode in the project
Usage  : juliad [+h] [+v] [+l] [+k] [+s] [+J juliax] [julia_options] file.jl [args]
    +h : this help
    +v : verbose (vs launching steps)
    +l : list running server and exits
    +k : kill running server and exits
    +s : launch julia with startup file (default is without)
    +J juliax  : use "juliax" as julia executable
Notes:
  - the principle is to lauch one daemon per directory (=project)
  - the script creates a local file '.juliad' which stores the status of a running daemon
  - as of current, status is (port used, julia_args(project, use_startup))
```

```
julia-listp : list Project.toml files (or Manifest.toml)

Usage : julia-listp [-h|--help] [-q] [-p|-m|-ph|-pa|-r|-pk]
      -p  : show Projects.toml (default)
      -m  : show Manifests.toml
      -r  : raw path ouput
      -ph : use $HOME instead of ~
      -pa : abs paths : subsistute value of $HOME to ~
      -pk : show paths inside .julia/packages
```

```
julia-list-repo-url : list all external repos used (eg dev'ed or add'ed unregistred packages)

Usage : julia-list-repo-url [-h|--help] [-v]
      -v  : show also source file/line
```
