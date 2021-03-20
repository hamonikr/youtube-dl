# youtube-dl

- youtube-dl(2021.02.10) 을 하모니카에서 사용할 수 있도록 패키지한 버전
- 기본으로 제공되는 버전은 자체 업데이트를 제공하지 않기 때문에 현재 다운로드 불가능

* upstream : https://github.com/rbrito/pkg-youtube-dl


## How to build

1) prepare gpg key for build team
2) download source from github
```
# build dependancy
sudo apt install dh-exec dh-python flake8 pandoc

# download upstream source
wget https://github.com/rbrito/pkg-youtube-dl/archive/refs/tags/upstream/2021.02.10.tar.gz -O ./youtube-dl/youtube-dl_2021.02.10.orig.tar.gz

# debian package build with gpg sign
cd youtube-dl/pkg-youtube-dl
dpkg-buildpackage --sign-key=9FA298A1E42665B8
```