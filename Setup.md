# Setup 

## Windows 

1. Öffne eine Powershell im **Administratormodus** 

2. ```powershell
   dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
   ```

3. ```powershell
   dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
   ```

4. Starte den PC neu 

5. Lade das WSL Update [hier](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) herunter und installiere es 

6. Default veresion setzen: 

   1. Für PC's ohne VPN's 

      ```powershell
      wsl --set-default-version 2
      ```

   2. Für PC's mit VPN 

      ```powershell
      wsl --set-default-version 1
      ```

7. Lade dir Ubuntu aus dem [Microsoft store](https://www.microsoft.com/de-de/p/ubuntu/9nblggh4msv6?activetab=pivot:overviewtab) herunter 

8. Starte Ubunut und richte deinen user ein

9. Führe folgende Kommandos in Ubuntu aus, damit dein System aktuallisiert wird: 

   ```shell
   sudo apt update && sudo apt upgrade -y
   ```

10. Überprüfe deine Ubuntu Version: 

    ```shell
    lsb_release -a
    ```

    Ist die Version 20.10 oder größer gehe zu Schritt

11. Führe folgende Schritte aus, um die version von Ubuntu zu uppen: 

    ```shell
    sudo apt dist-upgrade
    sudo apt autoremove
    sudo nano /etc/update-manager/release-upgrades
    ```

    In dem Fenster mit den Pfeiltasten zu =lts navigieren und lts durch normal ersetzen. Mit strg+x beenden und speichern. 

    ```shell
    sudo do-release-upgrade
    ```

    Der obige Befehl wird einige Zeit laufen (1-2h) 

12. Latex installieren: 

    ```shell
    sudo apt install texlive texlive-latex-extra texlive-lang-german texlive-fonts-extra latexmk texlive-science texlive-bibtex-extra biber texlive-extra-utils -y
    ```

    Auch dieses Kommando wird einige Zeit Brauchen 

