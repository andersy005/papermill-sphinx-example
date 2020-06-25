# papermill-sphinx-example

## Usage

```bash
> tree -L 3 notebooks/                             (papermill-sphinx) 12:38:16
notebooks/
└── animated-polar-plot.ipynb

0 directories, 1 file
```

- Execute parameterized notebooks

```bash
> preapermill --parameter-file prepapermill.yaml notebooks/animated-polar-plot.ipynb
Executing: 100%|████████████████████████████| 14/14 [00:44<00:00,  3.19s/cell]
Executing: 100%|████████████████████████████| 14/14 [00:40<00:00,  2.87s/cell]
```

```bash
>tree  -L 3 notebooks/                            ((papermill-sphinx) 12:44:56
notebooks/
├── animated-polar-plot.ipynb
└── output
    ├── animated-polar-plot_start_date_2010-01-01_end_date_2015-01-03.ipynb
    └── animated-polar-plot_start_date_2016-01-01_end_date_2020-01-03.ipynb

1 directory, 3 files
```

- Generate Sphinx documentation

```bash
make html
```

- Preview generated HTML webpage

```bash
open _build/html/index.html
```
