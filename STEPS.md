1. 修改SfM_SequentialPipeline.py中的K，执行以下脚本
```
$ cd build/software/SfM/
$ python SfM_SequentialPipeline.py [full path image directory] [resulting directory]
$ python SfM_SequentialPipeline.py ~/home/user/data/ImageDataset_SceauxCastle/images ~/home/user/data/ImageDataset_SceauxCastle/Castle_Incremental_Reconstruction

$ python SfM_GlobalPipeline.py [full path image directory] [resulting directory]
```
2. 生成PMVS
```
openMVG_main_openMVG2PMVS -i tutorial_out/reconstruction_global/sfm_data.bin -o tutorial_out/reconstruction_global
```
3. 稠密化，PMVS后一定要加/
```
pmvs2 ./PMVS/ pmvs_options.txt
```

