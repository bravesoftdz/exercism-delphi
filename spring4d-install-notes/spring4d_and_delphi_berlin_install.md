Instructions for integrating Spring4d open source [here](https://bitbucket.org/sglienke/spring4d/src/7e029a4b36e42abfbe3bf34e7b03a50ac5fcca77/?at=release%2F1.2) with Starter Edition of Delphi.  These instructions are based on the July 7, 2017 `release v1.2`.  There have been many hotfix updates that you may decide to use if you like.

Note: Spring4D comes with a very nice build tool to automatically install spring4d into all occurrences of Delphi that it may find, however, it will not work with Starter Edition as no command line compiler is available.  The Spring4d Installer requires the use of the Delphi command line compiler.  If you are not using Starter Edition and are using a compatible version of Delphi, then please utilize the installer and not follow these instructions.

In Delphi Starter Edition, navigate to:  
1. `Tools` => `Environment Options` => `Environment Variables`  
1. Add a `New...` variable to represent where you have placed Spring4D locally:  
For example: SPRING4D=C:\Program Files\Embarcadero\Studio\18.0\source\spring4d\Source  
***Note: replace `18.0` with your version of Delphi if you placed Spring4d within the folder structure of Delphi.  Berlin is `18.0` and `Tokyo` is `19.0`.***
1. Still within options go to: `Environment Options` => `Delphi Options` => `Library`  
   1. For `Browsing Path` click the `...` button and `add` the following paths  
      1. $(SPRING4D)  
      1. $(SPRING4D)\Base  
      1. $(SPRING4D)\Base\Collections  
      1. $(SPRING4D)\Base\Logging  
      1. $(SPRING4D)\Base\Patches  
      1. $(SPRING4D)\Core\Services  
      1. $(SPRING4D)\Core\Container  
      1. $(SPRING4D)\Core\Interception  
      1. $(SPRING4D)\Core\Logging  
      1. $(SPRING4D)\Core\Mocking  
      1. $(SPRING4D)\Extensions\Utils  
      1. $(SPRING4D)\Extensions\Cryptography  
1. Finally in `Delphi options` repeat 3.i, but this time in `Library path:`

