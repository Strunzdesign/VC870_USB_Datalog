~he2325u~

compile:
  - cd in this directory
  - get hidapi: git clone git://github.com/signal11/hidapi.git
  - make (hidapi has some depencies, make will output whats missing)



usage:
    unfortunately hw access is required -> sudo

  - only 1 interface cable connected, autodetect:
        sudo ./he2325u

  - multiple interface cables connected, use first cable:
        sudo ./he2325u

  - multiple cables, find out the available adresses:
        sudo ./he2325u 

    will output the available devices:

        [!] found 2 devices:
        0002:001f:00
        0002:0020:00

    -OR-
        lsusb | grep HE2325U

    will output the available devices:
        Bus 002 Device 032: ID 1a86:e008 QinHeng Electronics HID-based USB-serial converter, full-speed, similar to HE2325U
        Bus 002 Device 031: ID 1a86:e008 QinHeng Electronics HID-based USB-serial converter, full-speed, similar to HE2325U

    Bus X Device Y converts to XXXX:YYYY:00, with X and Y in hex


  - now a specific device can be used by:
        sudo ./he2325u 0002:0020:00


    


