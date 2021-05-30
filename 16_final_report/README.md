###### 21M31275 Yuki Maruyama

```
module load gcc/10.2.0 intel-mpi/19.9.304
mpicxx report.cpp -fopt-info-vec-optimized -march=native -O3 -fopenmp
mpirun -np 16 ./a.out
```

good pattern
```
21M31275@r2i2n0:~/classes/2021HPSC/hpc_lecture_2021/16_final_report> mpicxx report.cpp -march=native -O3 -fopenmp && mpirun -np 16 ./a.out
kc:512, nc:64, mc:128, nr:64, mr:32
N    : 2048
comp : 0.046039 s
comm : 0.008006 s
total: 0.054045 s (317.881190 GFlops)
error: 0.000258
```