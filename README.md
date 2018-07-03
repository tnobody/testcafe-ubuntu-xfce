# An Ubuntu-XFCE based Container for "real"™ UI-Tests

This image provides an environment to run real browser tests with **[Testscafe](http://devexpress.github.io/testcafe/)**

It's based on `consol/ubuntu-xfce-vnc` so you have all advantages of this container like:

- VNC Access (incl. NoVNC Webview)
- Ubuntu environemnt
- Real and configurable Browsers

See it's repo to find more information: https://github.com/ConSol/docker-headless-vnc-container

## Run container

```
docker run -p 5901:5901 -p 6901:6901 -v $PWDexample-tests:/testcafe tnobody/testcafe-ubuntu-xfce testcafe chrome example.ts
```

The exposed Ports of this container are: 

- 5901: For VNC clients
- 6901: For browserbased VNC-Webview

To access this views the password: `vncpassword` is required.

`/testcafe` is the Workingdirectory where you should mount your testfiles.
