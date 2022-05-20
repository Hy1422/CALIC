**Generate EPI and CALIC compression:**

`Calic.ipynb` : change the directory name, file size(nums,rows,height)
It will output a .craw file which contains the 2 bits output of CALIC encoding, and a .dat file contains the arithmetic coding bitstream of CALIC 

**Decoding** : 
example: calic8d Test1_3_EPI_PAE5_2.dat Test1_3_EPI_PAE5_2_r.raw
It will output the restore bitstream of EPI, and to reproduce EPI image and dataset, `Calic.ipynb` needs to be executed. 

**Near-lossless Compression**:

```
calic8e [*.raw] [width] [height] [depth] [Peak Absolute Error] [compressed file name]
calic8e Test1_3_EPI_0.raw 9129 720 8 3 Test1_3_EPI_PAE3_0.dat
calic8e Test1_3_EPI_1.raw 9129 720 8 3 Test1_3_EPI_PAE3_1.dat
calic8e Test1_3_EPI_2.raw 9129 720 8 3 Test1_3_EPI_PAE3_2.dat
```

	calic8d Test1_3_EPI_PAE3_0.dat Test1_3_EPI_PAE3_0_r.raw
	calic8d Test1_3_EPI_PAE3_1.dat Test1_3_EPI_PAE3_1_r.raw
	calic8d Test1_3_EPI_PAE3_2.dat Test1_3_EPI_PAE3_2_r.raw

