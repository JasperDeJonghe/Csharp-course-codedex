### 1
Output:
```
xoxoxoxoxo
xoxoxoxoxo
xoxoxoxoxo
xoxoxoxoxo
xoxoxoxoxo
xoxoxoxoxo
xoxoxoxoxo
xoxoxoxoxo
xoxoxoxoxo
xoxoxoxoxo
```
Solution:
```csharp
string content = "";

for (int i = 0; i < 10; i++) {
    for (int j = 0; j < 10; j++) {
        content += "X";
    }
    content += "\r\n";
}

Console.WriteLine(content);
```
### 2
Output:
```
XOOOOOOOOO
XXOOOOOOOO
XXXOOOOOOO
XXXXOOOOOO
XXXXXOOOOO
XXXXXXOOOO
XXXXXXXOOO
XXXXXXXXOO
XXXXXXXXXO
XXXXXXXXXX
```
Solution:
```csharp
string content = "";

for (int i = 0; i < 10; i++) {
    for (int j = 0; j < 10; j++) {
        if (i >= j) {
            content += "X";
        } else {
            content += "O";
        }
        
    }
    content += "\r\n";
}

Console.WriteLine(content);
```

### 3
Output:
```
XOOOOOOOOX
OXOOOOOOXO
OOXOOOOXOO
OOOXOOXOOO
OOOOXXOOOO
OOOOXXOOOO
OOOXOOXOOO
OOXOOOOXOO
OXOOOOOOXO
XOOOOOOOOX
```
Solution:
```csharp
string content = "";

for (int i = 0; i < 10; i++) {
    for (int j = 0; j < 10; j++) {
        if (i == j || i == 9-j) {
            content += "X";
        } else {
            content += "O";
        }
        
    }
    content += "\r\n";
}

Console.WriteLine(content);
```

### 4
Output:
```
XXXXXXXXXX
XOOOOOOOOX
XOOOOOOOOX
XOOOOOOOOX
XOOOOOOOOX
XOOOOOOOOX
XOOOOOOOOX
XOOOOOOOOX
XOOOOOOOOX
XXXXXXXXXX
```
Solution:
```csharp
string content = "";

for (int i = 0; i < 10; i++) {
    for (int j = 0; j < 10; j++) {
        if (i == 0 || i == 9 || j == 0 || j == 9) {
            content += "X";
        } else {
            content += "O";
        }
        
    }
    content += "\r\n";
}

Console.WriteLine(content);
wgi```