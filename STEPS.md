1. �޸�SfM_SequentialPipeline.py�е�K��ִ�����½ű�
```
$ cd build/software/SfM/
$ python SfM_SequentialPipeline.py [full path image directory] [resulting directory]
$ python SfM_SequentialPipeline.py ~/home/user/data/ImageDataset_SceauxCastle/images ~/home/user/data/ImageDataset_SceauxCastle/Castle_Incremental_Reconstruction

$ python SfM_GlobalPipeline.py [full path image directory] [resulting directory]
```
2. ����PMVS
```
openMVG_main_openMVG2PMVS -i tutorial_out/reconstruction_global/sfm_data.bin -o tutorial_out/reconstruction_global
```
3. ���ܻ���PMVS��һ��Ҫ��/
```
pmvs2 ./PMVS/ pmvs_options.txt
```

