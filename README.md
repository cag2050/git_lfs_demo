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

### 注意点
1. 使用中发现，必须先将.gitattributes文件进行更新、提交（Commit）和推送（Push），然后再对大文件进行Add、Commit、Push，即要分两次Push才能成功上传大文件。
2. 如果将.gitattributes的更新和大文件的Add、Commit、Push合并为一次Commit和Push，则Push依然会失败，提示不能上传大文件！
3. 出处：https://www.bbsmax.com/A/obzbLM1y5E/

资料 | 说明
--- | ---
官方网站 | https://git-lfs.com/
git lfs help |
GitHub限制上传单个大于100M的大文件 | https://www.bbsmax.com/A/obzbLM1y5E/


