# ProPresenter

Display setup, midi setup.

## Useful Keyboard Shortcuts

| Shortcut | Action                         |
| -------- | ------------------------------ |
| `cmd+1`  | Toggle Output                  |
| `cmd+2`  | Toggle Stage Display           |
| `cmd+3`  | Toggle Stage Display Preview   |
| `F1`     | Clear Everything (Blackout)    |
| `F6`     | Clear Everything (Go to Logo)  |
| `F2`     | Clear Slide (Leave Background) |
| `F3`     | Clear Background               |
| `F4`     | Clear Props                    |
| `F5`     | Clear Audio                    |


## Display Setup

The output should be configured to go to the projector and the stage display should be configured to go to the TV.

![Display Settings](./images/propresenter/display-settings.png)

## Midi Setup

Leave all midi notes the way they are for portability. Dealing with the midi notes will be covered in [Recording Slide Automation](recording-slide-automation.md).

## Remote Control

As a portable church we hold service in venues where we do not control the network. As a result, we are not typically able to remote-control ProPresenter over WiFi. That said, given a Linux server hosted somewhere on the Internet, we can tunnel the ProPresenter port to a public IP address. For example:

```sh
ssh -i <public-key> -nNT -R *:<remote-port>:localhost:<local-port> <remote-user>@<remote-ip>
```

From there, you can connect using the ProPresenter iOS or Android app at `<remote-ip>` on `<remote-port>`.

## Weekly Setup Checklist

* [ ] Songs
* [ ] Announcements Video
* [ ] Bumper Video
* [ ] Message Slides
