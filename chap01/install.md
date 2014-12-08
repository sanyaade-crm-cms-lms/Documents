Chương 1: Cài đặt Git
===

## Cặt đặt Git
Trước khi bắt đầu sử dụng Git, việc đầu tiên chúng ta phải làm là cài đặt nó. Có rất nhiều cách để cài đặt GIT, nhưng tất cả chúng được nhóm vào 2 cách chính:
- Cài đặt từ mã nguồn
- Cài đặt từ gói có sẵn trên hệ điều hành của bạn.

### Cài đặt từ mã nguồn:
Mỗi cách cài đặt sẽ có những ưu và nhược điểm khác nhau. Với cài đặt từ mã nguồn thì bạn sẽ luôn có một phiên bản mới nhất với nhiều cải tiến hữu ích về giao diện người dùng nhưng bạn sẽ phải quản lý các biến môi trường, cũng như là các phụ thuộc của gói. Để cài đặt được GIT, bạn cần một số thư viện như curl, zlib, openssl, expat và libiconv.
Nếu như bạn đang sử dụng một hệ điều hành được xây dựng trên nền debian, bạn có thể sử dụng lệnh sau để cài đặt tất cả các phụ thuộc của GIT:

`$ sudo apt-get install libcurl4-gnutls-dev libexpat1-dev gettext libz-dev libssl-dev`

Sau khi đã cài đặt xong tất cả các thư viện cần thiết, bước tiếp theo là tải phiên bản mới nhất của GIT từ website:
`http://git-scm.com/download`

Sau đó biên dịch và cài đăt:
```
$ tar -zxf git-x.x.x.x.tar.gz
$ cd git-x.x.x.x
$ make prefix=/usr/local all
$ sudo make prefix=/usr/local install
```

### Cài đặt trên Linux:
Nếu như bạn muốn cài đặt Git trên Linux thông qua một chương trình cài đặt, bạn có thể làm điều này thông qua phần mềm quản lý gói đi kèm với hệ điều hành của bạn. Với Fedora là yum, các hệ điều hành dựa trên nền debian là apt-get hay gentoo là emerge. Nếu bạn sử dụng Fedora, thì câu lệnh cài đặt sẽ là:

`$ sudo yum install git-core`

Hay với Ubuntu:

`$ sudo apt-get install git`

### Cài đặt trên Mac
Có 2 cách cài đặt trên Mac. Cách đơn giản nhất là sử dụng chương trình cài đặt có hỗ trợ giao diện, bạn có thể tải về từ trang SourceForge.

`http://sourceforge.net/projects/git-osx-installer/`


<Image to display>
Chương trình cài đặt Git cho Mac OS X

Một cách khác để cài đặt Git trên Mac là sử dụng MacPorts (http://www.macports.org). Nếu như bạn đã cài đặt MacPorts, Git có thể được cài đặt thông qua lệnh sau:

`$ sudo port install git-core`

### Cài đặt trên Window
Cài đặt Git trên Window thực sự đơn giản. Dự án msysGit cung cấp một cách cài đặt Git dễ dàng hơn. Đơn giản bạn chỉ cần tải tệp tin exe từ GitHub và chạy:

`http://msysgit.github.com/`

Sau khi nó được cài đặt, bạn có cả 2 phiên bản: command-line (bao gồm SSH) và bản giao diện chuẩn.

Chú ý khi sử dụng Git trên Window, bạn nên dùng Git bằng công cụ có sẵn: msysGit Shell (kiểu Unix), nó cho phép bạn sử dụng các lệnh phức tạp sau này.

Okay, đến đây các bạn đã cài đặt xong Github trên hệ điều hành của mình. Bài tiếp theo, chúng ta sẽ đi cấu hình cơ bản cho việc sử dụng Git.

