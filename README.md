# XmodMap - Caplock to Control
## A script to change Caplock to Control
### Why do I create this repo?
My daily work required runing two computers, a Fedora(Gnome) and a Window 10. Idealy, I use only a pair of keyboard and mouse. In middle, there is a ugreen switch .
I always prefer binding `Caplock` to `Ctr`. My main problem is after I switch from `Window` to `Fedora`, I cannot use my `Caplock` as a `Ctr`. Due to limited time available, I create
this repo to help me work around the problem quickly. Everytime I switch my working OS, I will run the script name `main.sh` using keyboard shortcut. I prefer binding `pause break` key to run `main.sh`.

The main method of this application is about to execute the following command
```
/usr/bin/xmodmap XmodMap
```

XmodMap's content is quite simple. [reference](https://wiki.archlinux.org/index.php/Xmodmap#Turn_CapsLock_into_Control)
```
clear lock
clear control
keycode 66 = Control_L
add control = Control_L Control_R

```

### How to use?
1. Clone the repository
2. Modify file named `main.sh`, modify file path to correct location that you clone the repository.
3. Assign a shortcut to launch the file `main.sh`.


### [VN] Tản Mạn
Công việc hàng ngày cùa tôi yêu cầu phải sử dụng Fedora(Gnome) và Window 10. Để làm việc dễ dàng hơn, tôi mong muốn chỉ sử dụng một bộ bàn phím + chuột.
Ở giữa trung gian sẽ có switch [KVM Switch USB Ugreen 30357](https://tiki.vn/bo-chuyen-tin-hieu-2-cpu-dung-1-man-hinh-kvm-switch-usb-ugreen-30357-hang-chinh-hang-p4594727.html?spid=14532209) để chuyển, tôi sử dụng `Emacs` và tôi đã bind phím `Caplock` thành `Ctrl`, tuy nhiên sau khi tôi sử dụng switch chuyển từ `Window` về `Linux`,
thiết lập này không còn tác dụng nữa. Repository này là giải pháp tạm thời trước khi tôi có thời gian nghiên cứu sâu hơn. Với giải pháp này, mỗi khi tôi chuyển
từ window về linux, tôi sẽ chạy cái script `main.sh` để nó bind phím lại. Bạn có thể chạy chương trình này bằng nhiều cách, cá nhân tôi bind phím `pause break`
trên bàn phím để kích hoạt script `main.sh` (Settings > Keyboard Shortcuts).
