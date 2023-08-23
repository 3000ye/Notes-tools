# Winedt快捷键配置

首先点击`Option -> Options Interface -> Menus and Toolbar -> Main Menu`，修改或添加配置：

**加粗：**

```ini
ITEM="Bold"
CAPTION="&Bold"
IMAGE="Bold"
MACRO="Exe('%b\Menus\Insert\Bold.edt');"
SHORTCUT="16450::Ctrl+B"
REQ_DOCUMENT=1
```

**斜体：**

```ini
ITEM="Emphasize_(Italic)"
CAPTION="&Emphasize (Italic)"
IMAGE="Italic"
MACRO="Exe('%b\Menus\Insert\Emph.edt');"
SHORTCUT="16457::Ctrl+I"
REQ_DOCUMENT=1
```

**数学环境：**

```ini
ITEM="Equation"
CAPTION="&Equation"
IMAGE="Equation"
MACRO="LetReg(9,'equation');LetReg(8,'\label{}');"+
"Exe('%b\Menus\Insert\Env.edt');"
SHORTCUT="16461::Ctrl+M"
REQ_DOCUMENT=1         
```

**无序列表与有序列表：**

```ini
ITEM="Itemize"
  CAPTION="&Itemize"
  IMAGE="ListItem"
  MACRO="LetReg(9,'List Items');LetReg(8,'itemize');"+
        "Exe('%b\Menus\Insert\List.edt');"
  SHORTCUT="49225::Ctrl+Alt+I"
  REQ_DOCUMENT=1
ITEM="Enumerate"
  CAPTION="&Enumerate"
  IMAGE="ListEnum"
  MACRO="LetReg(9,'Enumerate Items');LetReg(8,'enumerate');"+
        "Exe('%b\Menus\Insert\List.edt');"
  SHORTCUT="49221::Ctrl+Alt+E"   
```

**图片：**

```ini
ITEM="Figure"
  CAPTION="&Figure"
  IMAGE="Figure"
  MACRO="Exe('%b\Menus\Insert\Image.edt');"
  SHORTCUT="49222::Ctrl+Alt+F"
  REQ_DOCUMENT=1  
```

**编译：**

```ini
ITEM="XeLaTeX"
  CAPTION="XeLaTeX"
  IMAGE="TeXXeLaTeX"
  SAVE_INPUT=1
  MACRO="Exe('%b\Exec\TeX\XeLaTeX.edt');"
  REQ_FILTER=:"%!M=TeX"|"%!M=TeX:STY"|"%!M=TeX:AUX"
  SHORTCUT="24650::Shift+Ctrl+J"  
```