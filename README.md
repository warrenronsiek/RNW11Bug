1. `yarn install` the dependencies 
2. Build release, store upload app via visual studio, generating temp keys as needed
3. Install the app via the generated `windows\RNW11Bug\AppPackages\RNW11Bug_1.0.2.0_x64_Test` install script
4. Observe that the app runs
5. Uninstall via Add/Remove programs
6. Install via the .misxupload file:
   1. `Rename-Item -Path "RNW11Bug_1.0.2.0_x64.msixupload" -NewName "Bug.zip"`
   2. `Expand-Archive -Path Bug.zip -DestinationPath Bug`
   3. Double click install the Bug\RNW11Bug_1.0.2.0_x64.msix file
   4. Observe crash
   5. Check KERNELBASE.dll error crash logs in Event Viewer
