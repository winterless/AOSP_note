**DOWNLOAD AOSP**  

```
mkdir ~/bin
PATH=~/bin:$PATH
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
chmod a+x ~/bin/repo
repo init -u https://mirrors.tuna.tsinghua.edu.cn/git/AOSP/platform/manifest -b XXX
repo sync -c -j4
XXX from https://source.android.com/setup/start/build-numbers#source-code-tags-and-builds
清华的源快点：https://mirrors.tuna.tsinghua.edu.cn/help/AOSP/
```

**BUILD AOSP**  
```
source build/envsetup.sh
lunch aosp_arm64-eng
make -j8
```
