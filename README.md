# Dell 7710 usb ports

````
       Left               Right
USB 1/ 2 | usb3           usb3    |   usb 1/2 
    1-1    2-1            2-3     |    1-2
                          2-4     |    1-3
                          2-5     |    1-4


webcam =  1-11
??     = 1-6
````

```
 qm set $VM-ID -args "\
-device usb-ehci,id=ehci1 \
-device usb-host,bus=ehci1.0,hostbus=1,hostport=2,id=R-Port-1-usb2 \
-device usb-host,bus=ehci1.0,hostbus=1,hostport=2.1,id=R-Port-1-hub-1-usb2 \
-device usb-host,bus=ehci1.0,hostbus=1,hostport=2.2,id=R-Port-1-hub-2-usb2 \
-device usb-host,bus=ehci1.0,hostbus=1,hostport=2.3,id=R-Port-1-hub-3-usb2 \
-device usb-ehci,id=ehci2 \
-device usb-host,bus=ehci2.0,hostbus=1,hostport=3,id=R-Port-2 \
-device usb-host,bus=ehci2.0,hostbus=1,hostport=3.1,id=R-Port-2-hub-1-usb2 \
-device usb-host,bus=ehci2.0,hostbus=1,hostport=3.2,id=R-Port-2-hub-2-usb2 \
-device usb-host,bus=ehci2.0,hostbus=1,hostport=3.3,id=R-Port-2-hub-3-usb2 \
-device usb-ehci,id=ehci3 \
-device usb-host,bus=ehci3.0,hostbus=1,hostport=4,id=R-Port-3 \
-device usb-host,bus=ehci3.0,hostbus=1,hostport=4.1,id=R-Port-3-hub-1-usb2 \
-device usb-host,bus=ehci3.0,hostbus=1,hostport=4.2,id=R-Port-3-hub-2-usb2 \
-device usb-host,bus=ehci3.0,hostbus=1,hostport=4.3,id=R-Port-3-hub-3-usb2 \
-device usb-ehci,id=ehci4 \
-device usb-host,bus=ehci4.0,hostbus=1,hostport=1,id=L-Port\
-device usb-host,bus=ehci4.0,hostbus=1,hostport=1.1,id=L-Port-hub-1-usb2 \
-device usb-host,bus=ehci4.0,hostbus=1,hostport=1.2,id=L-Port-hub-2-usb2 \
-device usb-host,bus=ehci4.0,hostbus=1,hostport=1.3,id=L-Port-hub-3-usb2 \
-device qemu-xhci,id=xhci1 \
-device usb-host,bus=xhci1.0,hostbus=2,hostport=3,id=R-Port-1-usb3 \
-device usb-host,bus=xhci1.0,hostbus=2,hostport=3.1,id=R-Port-1-hub-1-usb3 \
-device usb-host,bus=xhci1.0,hostbus=2,hostport=3.2,id=R-Port-1-hub-2-usb3 \
-device usb-host,bus=xhci1.0,hostbus=2,hostport=3.3,id=R-Port-1-hub-3-usb3 \
-device qemu-xhci,id=xhci2 \
-device usb-host,bus=xhci2.0,hostbus=2,hostport=4,id=R-Port-2-usb3 \
-device usb-host,bus=xhci2.0,hostbus=2,hostport=4.1,id=R-Port-2-hub-1-usb3 \
-device usb-host,bus=xhci2.0,hostbus=2,hostport=4.2,id=R-Port-2-hub-2-usb3 \
-device usb-host,bus=xhci2.0,hostbus=2,hostport=4.3,id=R-Port-2-hub-3-usb3 \
-device qemu-xhci,id=xhci3 \
-device usb-host,bus=xhci3.0,hostbus=2,hostport=5,id=R-Port-3-usb3 \
-device usb-host,bus=xhci3.0,hostbus=2,hostport=5.1,id=R-Port-3-hub-1-usb3 \
-device usb-host,bus=xhci3.0,hostbus=2,hostport=5.2,id=R-Port-3-hub-2-usb3 \
-device usb-host,bus=xhci3.0,hostbus=2,hostport=5.3,id=R-Port-3-hub-3-usb3 \
-device qemu-xhci,id=xhci4 \
-device usb-host,bus=xhci4.0,hostbus=2,hostport=1,id=L-Port-usb3 \
-device usb-host,bus=xhci4.0,hostbus=2,hostport=1.1,id=L-Port-hub-1-usb3 \
-device usb-host,bus=xhci4.0,hostbus=2,hostport=1.2,id=L-Port-hub-2-usb3 \
-device usb-host,bus=xhci4.0,hostbus=2,hostport=1.3,id=L-Port-hub-3-usb3 \
"
```
