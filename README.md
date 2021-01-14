## Microsoft Teams Mac OS virtual camera fix

Microsoft Teams Mac OS client doesn't recognize virtual cameras by default (EOS Webcam utility, EpocCam, NDI client)

Use the below terminal commands until the problem is [resolved](https://docs.microsoft.com/en-gb/microsoftteams/troubleshoot/teams-on-mac/virtual-camera-doesnt-work-macos)

Be aware this fix will affect product security

```
xcode-select --install
```

```bash
sudo codesign --remove-signature "/Applications/Microsoft Teams.app"

sudo codesign --remove-signature "/Applications/Microsoft Teams.app/Contents/Frameworks/Microsoft Teams Helper.app"

sudo codesign --remove-signature "/Applications/Microsoft Teams.app/Contents/Frameworks/Microsoft Teams Helper (GPU).app"

sudo codesign --remove-signature "/Applications/Microsoft Teams.app/Contents/Frameworks/Microsoft Teams Helper (Plugin).app"

sudo codesign --remove-signature "/Applications/Microsoft Teams.app/Contents/Frameworks/Microsoft Teams Helper (Renderer).app"
```

[Bug report](https://microsoftteams.uservoice.com/forums/908686-bug-reports/suggestions/40961347-latest-teams-update-breaks-virtual-cameras-micro)

[Source](https://answers.microsoft.com/en-us/msteams/forum/msteams_tfb-msteams_tfmac/microsoft-teams-mac-os-client-is-not-recognizing/d9e863be-d9a4-4d03-a4b8-1b5c7df58828?page=1)
