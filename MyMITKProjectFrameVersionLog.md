## My Modified MITK Project Frame By SpeedyZJF
***
> ### VersionNote: 
| Item        | Value       | Remark-Demo |
| :---------: | :---------: | :----: |
| First number| MajorVersion| 6      |
| Second number| MinorVersion| 1     |
| Third number| PatchVersion| 0      |
***
- ### Version: 6.1.0:  
支持基本框架（包含GDCM ITK VTK OpenCV Boost Qt5, etc）,已打包MyMITKFrameV6.1.rar，分别在GitHUb，FTP和本地网络共享都有分享和上传；  
其中，通用工程框架名为：MITKFrameV61/Examples/GeneralProjFrm  
如下图D:/MITKviaSpeedy/GeneralProjFrameviaMITKGitHUbScreenshot.png：  
![Frame](https://raw.githubusercontent.com/SpeedyF/MyCloudNoteMarkdownInternetDir/master/GeneralProjFrameviaMITKGitHUbScreenshot.png)
***
- ### Version: 6.1.1:   
    - 已上传本地TortoiseSVN，进行版本控制与管理
    - 增加了MITK默认不会生成的特殊功能模块，即对相应的/MITKFrameV61/CMakeExternals/下的.cmake或者CMakeLists.txt增加如下类似CMake构建选项即可：
    - 以ITK.cmake增加ITKVtkGlue模块为例：（如下图,D:/MITKviaSpeedy/ITKcmake-ITKVtkGlue-Okay.png）
    ![ITKVtkGlue](https://raw.githubusercontent.com/SpeedyF/MyCloudNoteMarkdownInternetDir/master/ITKcmake-ITKVtkGlue-Okay.png)
    - 对应的ASCII内容如下：
    
```
    # /// Below, Tested by SpeedyZJF ///
    list(APPEND additional_cmake_args
    -DBUILD_TESTING:BOOL=ON
	-DModule_ITKVtkGlue:BOOL=ON
	-DVTK_DIR:PATH=${VTK_DIR}
   )
``` 
> 之后Version 6.1.1的版本就加上了ITKVtkGlue中的如下头文件，不会出现之前加上默认找不到的问题了: 
```
    #include "itkImageToVTKImageFilter.h"	// Okay， Fr ITK module/Bridge/ITKVtkGlue
```
***
- ### Version：6.1.2：
……To be coming~~ @ SpeedyZJF



