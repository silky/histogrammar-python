Python implementation of Histogrammar
=====================================

See [histogrammar.org](http://histogrammar.org) for a complete introduction to Histogrammar.

This is a pure Python implementation for Python versions 2.6, 2.7, and 3.4.

Installation
============

Histogrammar has a standard Python install script. Run

```bash
python setup.py install
```

with `sudo` if superuser permissions are needed or `--home=~` to install in a home directory. The latter option requires an appropriate `PYTHONPATH`.

This package has no explicit dependencies, though it can use back-ends like Numpy and front-ends like Matplotlib and Bokeh if they are on your system. If not, you'll get an `ImportError` at the time you try to call these methods.

Status
======

![Build status](https://travis-ci.org/histogrammar/histogrammar-python.svg)

The tests are thorough.

   * `original.py` were written during development to test all features as they were added.
   * `autogenerated.py` is from the language-independent testing suite ([histogrammar-multilang](https://github.com/histogrammar/histogrammar-multilang)), which provides greater coverage, value-explicitness in the test script, and cross-language agreement.
   * `testnumpy.py` tests numerical agreement between the conventional implementation and the Numpy implementation, which are very different. Also tests much larger datasets and infinity/NaN handling.
     * contrary to its name, `testnumpy.py` also compares its implementation with the literal code given in [the specification](http://histogrammar.org/docs/specification/) as well.

Primitive implementation is mature. CUDA implementation has begun.

| Primitive         | Pure Python | Numpy | ROOT/Cling | CUDA GPU   |
|:------------------|:------------|:------|:-----------|:-----------|
| Count             | done        | done  | done       |            |
| Sum               | done        | done  | done       | done       |
| Average           | done        | done  | done       |            |
| Deviate           | done        | done  | done       |            |
| Minimize          | done        | done  | done       |            |
| Maximize          | done        | done  | done       |            |
| Bag               | done        | done  | done       | impossible |
| Bin               | done        | done  | done       |            |
| SparselyBin       | done        | done  | done       | impossible |
| CentrallyBin      | done        | done  | done       |            |
| IrregularlyBin    | done        | done  | done       |            |
| Categorize        | done        | done  | done       | impossible |
| Fraction          | done        | done  | done       |            |
| Stack             | done        | done  | done       |            |
| Select            | done        | done  | done       |            |
| Limit             | done        | done  | done       |            |
| Label             | done        | done  | done       |            |
| UntypedLabel      | done        | done  | done       |            |
| Index             | done        | done  | done       |            |
| Branch            | done        | done  | done       |            |
