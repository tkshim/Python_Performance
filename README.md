1. install memory_profiler
#pip install -U memory_profiler


2. check memory performance
```py
python -m memory_profiler memtest01.py 
Filename: memtest.py

Line #    Mem usage    Increment   Line Contents
================================================
     4   11.094 MiB   11.094 MiB   @profile
     5                             def main():
     6   11.102 MiB    0.008 MiB       l = 0

python -m memory_profiler memtest02.py 
Filename: memtest02.py

Line #    Mem usage    Increment   Line Contents
================================================
     4   10.992 MiB   10.992 MiB   @profile
     5                             def main():
     6   18.633 MiB    7.641 MiB       l = [0] * 1000000

python -m memory_profiler memtest03.py 
Filename: memtest03.py

Line #    Mem usage    Increment   Line Contents
================================================
     4   10.961 MiB   10.961 MiB   @profile
     5                             def main():
     6 2607.359 MiB 2596.398 MiB       l = [0] * 1000000000
```py

![Performance Difference](https://github.com/tkshim/Picture/blob/master/diff_perform_python.png)
