# SOC-tables
сравнительная таблица SOCs для выбора HW для умного дома на OpenHub

сейчас стоит cubiboard2 -тупит очень сильно.


Allwinner A20 Antutu v3.3 on the device with a total score of 4266 points

amlogic s912  Antutu 37517/41185


 
пробуем разобратся с производительностью JAVA
есть тест https://math.nist.gov/scimark2/download_java.html
запускается 



## НА ThinkPad X1 JOGA 1st (i7-6600U 2,6/2,81GHz) 

```
java -cp scimark2lib.jar jnt.scimark2.commandline

SciMark 2.0a

Composite Score: 1688.469775749008
FFT (1024): 1037.003922398661
SOR (100x100):   1098.2929458166686
Monte Carlo : 695.8792955218945
Sparse matmult (N=1000, nz=5000): 1579.1807546450868
LU (100x100): 4031.991960362729

java.vendor: Oracle Corporation
java.version: 1.8.0_144
os.arch: amd64
os.name: Windows 10
os.version: 10.0
```


```
java -cp scimark2lib.jar jnt.scimark2.commandline -large

SciMark 2.0a

Composite Score: 1185.6395044767428
FFT (1048576): 174.90549413430116
SOR (1000x1000):   962.8955046732282
Monte Carlo : 713.4497192039823
Sparse matmult (N=100000, nz=1000000): 1370.357941655649
LU (1000x1000): 2706.5888627165527

java.vendor: Oracle Corporation
java.version: 1.8.0_144
os.arch: amd64
os.name: Windows 10
os.version: 10.0
```


## cubieboard 2
https://openbenchmarking.org/result/1806275-AR-CUBIEBOAR05


```
root@cubieboard2:~# java -cp scimark2lib.jar jnt.scimark2.commandline

SciMark 2.0a

Composite Score: 48.08651648734924
FFT (1024): 30.27354564385959
SOR (100x100):   84.48592425032193
Monte Carlo : 16.76883219160037
Sparse matmult (N=1000, nz=5000): 44.9122806782721
LU (100x100): 63.99199967269221

java.vendor: Oracle Corporation
java.version: 1.8.0_191
os.arch: arm
os.name: Linux
os.version: 4.14.81-sunxi
```

```
 root@cubieboard2:~# java -cp scimark2lib.jar jnt.scimark2.commandline -large

SciMark 2.0a

Composite Score: 31.792022537212553
FFT (1048576): 7.6719542441047786
SOR (1000x1000):   78.53122438787184
Monte Carlo : 16.718700802299082
Sparse matmult (N=100000, nz=1000000): 22.408962133772683
LU (1000x1000): 33.629271118014366

java.vendor: Oracle Corporation
java.version: 1.8.0_191
os.arch: arm
os.name: Linux
os.version: 4.14.81-sunxi

```
