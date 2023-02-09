### Git Large File Storage (LFS)使用
1. git push时报错：
```
remote: warning: File libavformat.a is 52.56 MB; this is larger than GitHub's recommended maximum file size of 50.00 MB
remote: warning: GH001: Large files detected. You may want to try Git Large File Storage - https://git-lfs.github.com.
```
2. git lfs install
3. git lfs track "libavformat.a"
4. 上面步骤会产生文件：.gitattributes，需要提交到版本库
5. git add .
6. git commit -m 'fls'
7. git push

资料 | 说明
--- | ---
官方网站 | https://git-lfs.com/
git lfs help | 



