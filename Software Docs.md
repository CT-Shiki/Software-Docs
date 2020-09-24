# Software Docs

## Tools

### CMDer

![cmder](./imgs/cmder.png)

`cmder` is created out of pure frustraction over the absence of nice console emulators on Windows. 

#### Installation

1. [Download](https://github.com/cmderdev/cmder) and Unzip

2. (optional) Place your own executable files into the folder to be injected into your PATH.`bin`

3. Find following files in folders and right click to unlock file in attribute if warning when run `cmder.exe`

   | Files                                                        | Folder                                  |
   | ------------------------------------------------------------ | --------------------------------------- |
   | `ConEmu.exe`<br />`ConEmu64.exe`                             | `.\cmder\vendor\conemu-maximus5`        |
   | `ConEmuC.exe`<br />`ConEmuC64.exe`<br />`ConEmuCD.dll`<br />`ConEmuCD64.dll`<br />`ConEmuC.exe`<br />`ConEmuC64.exe`<br />`ConEmuHK.dll`<br />`ConEmuHK64.dll` | `.\cmder\vendor\conemu-maximus5\ConEmu` |

4. Run CMD or Powershell as an adminstrator and execute follow cmd to add cmder to right-click meau

   ```powershell
   Cmder.exe /REGISTER ALL
   ```

5. Run **Cmder** *(Cmder.exe)*

#### Settings

We can setting `Keys & Macro` to satisfy personal usage habits. (`Path:Settings-Keys & Macro`)

##### Pane Split

- `Ctrl+B` Split: Duplicate active ‘shell’ split to bottom: Split(0,0,50)
- `Ctrl+R` Split: Duplicate active ‘shell’ split to right: Split(0,50,0)
- `Ctrl+Enter` Split: Maximize/restore active pane: Split(3)
- `Ctrl+Shift+Up` Split: Move splitter upward: Split(1,0,-1)
- `Ctrl+Shift+Down` Split: Move splitter downward: Split(1,0,1)
- `Ctrl+Shift+Left` Split: Move splitter leftward: Split(1,-1,0)
- `Ctrl+Shift+Right` Split: Move splitter rightward: Split(1,1,0)
- `Ctrl+Right`  Split: Put focus to next visible pane: Tab(10,1)
- `Ctrl+Left`  Split: Put focus to previous visible pane: Tab(10,-1)
- `Win+Up` Split: Put focus to nearest pane upward: Split(2,0,-1)
- `Win+Down` Split: Put focus to nearest pane downward: Split(2,0,1)
- `Win+Left` Split: Put focus to nearest pane leftward: Split(2,-1,0)
- `Win+Right` Split: Put focus to nearest pane rightward: Split(2,1,0)
- `Ctrl+Alt+S` Split: Exchange (swap) with nearest pane: Split(4)
- `Ctrl+Alt+Up` Split: Exchange (swap) with nearest pane upward: Split(4,0,-1)
- `Ctrl+Alt+Down` Split: Exchange (swap) with nearest pane downward: Split(4,0,1)
- `Ctrl+Alt+Left` Split: Exchange (swap) with nearest pane leftward: Split(4,-1,0)
- `Ctrl+Alt+Right` Split: Exchange (swap) with nearest pane rightward: Split(4,1,0)
- `Ctrl+G` Group keyboard input for visible splits: GroupInput(0)

##### VScode Split

If Vscode is your main IDE, it's simple to integrate cmder and vscode by adding follow alias command in `user_aliases.cmd`

```bash
vscode = "E:\VSCode\Microsoft VS Code\Code.exe" $1 -new_console:s70H
```

![cmder+vscode](.\imgs\cmder+vscode.png)

##### Transparency

we can set cmder background transparency when window active and inactive. (`Path:Features-Transparency`)