Cấu hình với GIT
===

## Cấu hình
Đến bây giờ, Git đã có trên hệ thống của bạn, có thể bạn sẽ muốn tùy biến môi trường cho Git.

Git cung cấp sẵn git config cho phép bạn xem và chỉnh sửa các biến cấu hình để quản lý toàn bộ các khía cạnh của Git cũng như giao diện hoạt động của nó.

- `/etc/gitconfig` : Chứa giá trị cho tất cả người dùng và kho chứa trên hệ thống. Nếu bạn sử dụng `--system` khi chạy git config, thao tác đọc và ghi sẽ được thực hiện trên tập tin này.
- `~/.gitconfig` : Riêng biệt cho tài khoản của bạn. Bạn có thể chỉ định Git đọc và ghi trên tập tin này bằng cách sử dụng `--global`.
- tập tin config trong thư mục Git (.git/config) của bất kỳ kho chứa nào mà bạn đang sử dụng: Chỉ áp dụng riêng cho một kho chứa. Mỗi cấp sẽ ghi đè các giá trị của cấp trước nó, vì thế các giá trị trong .git/config sẽ "chiến thắng" các giá trị trong `/etc/gitconfig`.

Trên Windows, Git sử dụng tập tin .gitconfig trong thư mục $HOME (%USERPROFILE% trên môi trường Windows), cụ thể hơn đó là C:\Documents and Settings\$USER hoặc C:\Users\$USER, tuỳ thuộc vào phiên bản Windows đang sử dụng ($USER là %USERNAME% trên môi trường Windows)


### Danh tính của bạn

Việc đầu tiên bạn nên làm khi cấu hình Git là chỉ định tên tài khoản và địa chỉ e-mail của mình. Điều này rất quan trọng vì mỗi Git sẽ sử dụng chúng cho mỗi lần commit, những thông tin này được gắn bất di bất dịch vào các commit:

`$ git config --global user.name "NgaNguyenDuy"`
`$ git config --global user.email kyo1508@gmail.com`

Ở đây chúng ta đã sử dụng `--global` tức là chúng ta đã cấu hình cho toàn bộ hệ thống của mình, điều đó cũng có nghĩa là chúng ta chỉ phải làm việc này duy nhất một lần. Nhưng nếu tùy từng project của mình, có thể bạn phải sử dụng tên hay email khác, bạn có thể cấu hình lại cho riêng project đó bằng cách chạy các câu lệnh trên thư mục project của bạn muốn cấu hình và quan trọng là phải bỏ option --global đi.

### Trình Soạn thảo (Editor)

Danh tính của bạn đã được xác nhận, bạn có thể lựa chọn trình soạn thảo mặc định sử dụng để soạn thảo các dòng lệnh. Mặc định, Git sử dụng trình soạn thảo mặc định của hệ điều hành thường là vi hoặc vim. Nếu bạn muốn sử dụng một trình soạn thảo khác, ví dụ như tôi sử dụng Emacs:

`$ git config --global core.editor emacs`

### Công cụ so sánh (Diff)

Một lựa chọn hữu ích khác mà bạn có thể muốn thay đổi đó là chương trình so sánh sự thay đổi để giải quyết các trường hợp xung đột (merge) nội dung. Ví dụ bạn muốn sử dụng vimdiff:

`$ git config --global merge.tool vimdiff`

Ngoài ra còn rất nhiều các công cụ khác như kdiff3, tkdiff, meld, xxdiff, emerge, vimdiff, gvimdiff, ecmerge, và opendiff. Chúng ta sẽ thảo luận thêm về các công cụ này trong các chương sau.

### Kiểm Tra Cấu Hình

Sau khi bạn đã cấu hình toàn bộ Git cho hệ thống của riêng mình, có thể bạn có thể muốn kiểm tra lại các cấu hình của mình. Bạn có thể sử dụng lệnh `git config --list` để liệt kê tất cả các cấu hình mình đã thực hiện.

```
$ git config --list
user.name=Nga Nguyen Duy
user.email=kyo1508@gmail.com
color.status=auto
color.branch=auto
color.interactive=auto
color.diff=auto
...
```

Hoặc bạn có thể kiểm tra một trường hợp riêng biệt nào đấy như user name hay email chẳng hạn:

`$ git config user.name` hay `$ git config user.email`

Okay, sau bài này, chúng ta đã có được những thiết lập cơ bản để chuẩn bị cho việc thao tác cơ bản với Git trong bài sau.
