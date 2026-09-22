1. restrict logical core, 
```
os.environ["OMP_NUM_THREADS"] = "16"
os.environ["OMP_DYNAMIC"] = "FALSE"  # do not reduce threads
os.environ["MKL_NUM_THREADS"] = "1"
os.environ["OPENBLAS_NUM_THREADS"] = "1"
os.environ["NUMEXPR_NUM_THREADS"] = "1"
```
use `np.show_config()` can check which math library (`openblas` or `blis`) use in this environment.