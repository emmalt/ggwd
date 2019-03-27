# ggwd: generate gravitational-wave data

The purpose of this repository is to provide a starting point for **generating realistic synthetic gravitational-wave data** which can then be used, for example, as training data for machine learning experiments.

More specifically, the methods provided here will help you with the simulation of GW signals from compact binary coalescences (e.g., binary black hole mergers), adding these signals into a pieces of background noise (either synethetic or real LIGO background recordings) and applying standard post-processing steps (e.g., whitening and band-passing) to results.

**Disclaimer**: The scripts in this repository are mostly just convenience wrappers around functionalities provided by the great and mighty [PyCBC software package](https://pycbc.org/) (which itself relies in parts on the [LIGO Algorithm Library](https://wiki.ligo.org/Computing/DASWG/LALSuite)).



## Quickstart

As of now, this project is not a "proper" Python package, but only a collection of scripts, which don't need to be installed. Simply clone the repository:

```
git clone git@github.com:timothygebhard/ggwd.git
```

Ensure your Python environment fulfills all the requirements specified in `requirements.txt` (ideally, simply use a fresh virtual environment). **Please note that due to the dependence on PyCBC, this code only works with Python 2.7!** Now, you should be able to generate your first data sample by simply running:

```
python generate_sample.py
```

This will some default values generate a small demo sample file in the `./output` directory. Please check out the documentation to see how to adjust the configuration to your needs, and, for example, also generate samples using real LIGO recordings as the background noise.

You can then use the `view_sample.py` script to inspect the results, which should look something like this:

![](./docs/userguide/images/sample_with_injection.png)



## Documentation

The documentation for all code, including detailed guides describing, for example, how to control the details of the sample generation process through customized configuration files, can be build simply by running `make html` in the `./docs` directory. The result will be placed in the `./docs/build/html` directory.



## Contributing to this project

Contributions to this project are very welcome! If you have found any issues with the code, or would like to contribute to add further functionality, please do not hesitate to get in touch, open an issue on GitHub, or directly send a pull request!



## Authors & License

The code in this repository is developed by [Timothy Gebhard](https://github.com/timothygebhard) and [Niki Kilbertus](https://github.com/nikikilbertus). It is distributed under the GPL-3.0 license (see LICENSE file for details), which means in particular that it is provided *as is*, without any warranty, liability, or guarantees regarding its correctness.
