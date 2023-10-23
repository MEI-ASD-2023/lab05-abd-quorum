# Lab 05: Distributed Register

In this lab, you will modify the distributed system that you created in the first phase of the project, to build a distributed register application (see [Lecture Four](https://clip.fct.unl.pt/utente/eu/fun%E7%E3o/doc%EAncia/unidade/actividade/documentos?tipo_de_per%EDodo_lectivo=s&tipo_de_documento_de_unidade=0ac&ano_lectivo=2024&per%EDodo_lectivo=1&institui%E7%E3o=97747&unidade_curricular=10644&submit=documentos:d&d_detalhar=402063) based on an [ABD quorum](./slides/lab05-slides.pdf).

Your application consists of a variable `value`. All nodes can both write to and read from the value of the register. Therefore, the high-level application that a client interacts with for a given process should contain the following API:

```python
def write(t,x) # writes the value `x` to the local copy of `value` in each node, corresponding to the tag `t`.
def read() # reads the current setting `value` from the local state
```

## Tasks

1. Implement the `write` and `read` replica operations, as specified in the ABD Quorum, see the [slides](./slides/lab05-slides.pdf) or the [paper](http://www.cse.huji.ac.il/course/2004/dist/p124-attiya.pdf) for more details.
2. Modify the application part of your process to accept user input (via command line, HTTP, or otherwise) and implement the required API.
3. Measure experimentally how long it takes for `write` and `read` operations be processed within your system.
