# Julia

I switched from MATLAB and Python to Julia. This document specifies my recommended style for Julia code and some improvement tips for MATLAB users. These conventions were collected from a variety of sources including Python's [PEP8](http://legacy.python.org/dev/peps/pep-0008), Julia's [Notes for Contributors](https://github.com/JuliaLang/julia/blob/master/CONTRIBUTING.md), and Julia's [Style Guide](https://docs.julialang.org/en/latest/manual/style-guide/), Invenia's [BlueStyle](https://github.com/invenia/BlueStyle), Ismael's [Naming Guidance](https://github.com/JuliaPraxis/Naming) and QuantEcon's [Style Lecture](https://github.com/QuantEcon/lecture-source-jl/blob/master/style.md).

### Performance Tips

Here are some performance tips for doing large scale nonlinear optimization in Julia. More on Julia's [performance tips](https://docs.julialang.org/en/v1/manual/performance-tips/), fast numerics advice [here](https://julialang.org/blog/2013/09/fast-numeric/), University of California's [note](https://ucidatascienceinitiative.github.io/IntroToJulia/Html/WhyJulia?ref=hackernoon.com).

1. **Devectorization**. C-like speed is obtained by using simple C-like element-wise loop-based approach that *pre-allocates memory*(See [here](https://hackernoon.com/freeing-the-data-scientist-mind-from-the-curse-of-vectorization-julia-to-the-rescue-0c3z308v) and [here](http://kristofferc.github.io/post/vectorization_performance_study/#fn:3) for more examples).
2. **Preallocate memory**. Pre-allocation for arrays that are involved in iterations helps the machine to optimize the code. Otherwise, the array would expand in every iteration.
3. Write **type-stable** code. Make sure types of all variables do not vary over time.
4. **No global variables**(use `const` if must). Treat parameters as `NamedTuple` by using the package `Parameters`. 

### Must-known Packages

- Pkg

  Pkg is a basic but very important package for replicapable research. It provides with excellent package management system. Basic usages please check [here](https://julialang.github.io/Pkg.jl/v1/). For replicapable research, see part 4 for [environments](https://julialang.github.io/Pkg.jl/v1/environments/) and part 10 for [package management](https://julialang.github.io/Pkg.jl/v1/toml-files/). Please check [glossory](https://julialang.github.io/Pkg.jl/v1/glossary/) for related terminology.

- Revise

  
  
  



