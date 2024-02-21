1. 修改SfM_SequentialPipeline.py中的K，执行以下脚本
```
$ cd build/software/SfM/
$ python SfM_SequentialPipeline.py [full path image directory] [resulting directory]
$ python SfM_SequentialPipeline.py ~/home/user/data/ImageDataset_SceauxCastle/images ~/home/user/data/ImageDataset_SceauxCastle/Castle_Incremental_Reconstruction

$ python SfM_GlobalPipeline.py [full path image directory] [resulting directory]
```
2. 生成OPENMVS
```
.\openMVG_main_openMVG2openMVS.exe -i E:\test\openMVG\build\software\SfM\0cup\output\reconstruction_sequential\sfm_data.bin -o E:\test\openMVG\build\software\SfM\0cup\output\reconstruction_sequential\mvs\scene.mvs -d E:\test\openMVG\build\software\SfM\0cup\output\reconstruction_sequential\mvs\undistortedImages
```
3. 稠密化
```
cd OpenMVS_Windows_x64
copy undistortedImages to here
DensifyPointCloud.exe mvs\scene.mvs 
ReconstructMesh.exe mvs\scene_dense.mvs 
RefineMesh.exe mvs/scene_dense.mvs -m mvs/scene_dense_mesh.ply -o mvs/scene_dense_mesh_refine.mvs
TextureMesh.exe mvs/scene_dense.mvs -m mvs/scene_dense_mesh.ply -o mvs/scene_dense_mesh_texture.mvs
```

