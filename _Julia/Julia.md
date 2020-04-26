# Julia

I switch from MATLAB and Python to Julia. This document specifies my recommended style for Julia code and some improvement tips for MATLAB users. These conventions were collected from a variety of sources including Python's [PEP8](http://legacy.python.org/dev/peps/pep-0008), Julia's [Notes for Contributors](https://github.com/JuliaLang/julia/blob/master/CONTRIBUTING.md), and Julia's [Style Guide](https://docs.julialang.org/en/latest/manual/style-guide/), Invenia's [BlueStyle](https://github.com/invenia/BlueStyle), Ismael's [Naming Guidance](https://github.com/JuliaPraxis/Naming) and QuantEcon's [Style Lecture](https://github.com/QuantEcon/lecture-source-jl/blob/master/style.md).

### Performance Tips

1. No need for vectorization. Use simple C-like loops and obtain C-like speed(See [Daniel Moura's blog](https://hackernoon.com/freeing-the-data-scientist-mind-from-the-curse-of-vectorization-julia-to-the-rescue-0c3z308v) for a simple investigation).

