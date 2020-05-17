# Genetic Algorithm Reporter

This project is just for automating my tedious assignment in college, where I need to calculate the first 50 generation(with steps) in Genetic Algorithm

the algorithm that I write here is based on "Genetic Algorithm for Solving Simple Mathematical Equality Problem" paper by Denny Hermawanto

## How to use it
Download it from [releases](https://github.com/mfaizudd/GeneticAlgorithmReporter/releases "releases") section

Download .NET Core runtime from [this website](https://dotnet.microsoft.com/download/dotnet-core/3.1 "dotnet") and choose your operating system

and run it in command line:
```
$ GeneticAlgorithmReporter --help

  -f, --filename      Required. Input files to be processed

  -c, --crossover     (Default: 0.25) The rate of crossover

  -m, --mutation      (Default: 0.1) The rate of mutation

  -r, --report        (Default: ) Generate report, specify the name of the report that will be generated (html, txt)

  -g, --generation    (Default: 10) The total generation

  --help              Display this help screen.

  --version           Display version information.
```

Supported input file are .json with this format
```
[
    {"Genes":[2,5,17,1]},
    {"Genes":[10,4,13,14]},
    {"Genes":[12,5,23,2]},
    {"Genes":[20,4,13,14]},
    {"Genes":[10,5,18,3]},
    {"Genes":[20,1,10,6]}
]
```

As for the report argument, you must specify the filename you want to create(e.g. report.txt). The supported formats are html and txt

here's an example:
```
$ GeneticAlgorithmReporter -f chromosomes.json -g 50 -r report.html
```
