# C3D_PSet_file
PSets parameters file (property sets) for Autodesk AutoCAD Civil 3D and code on C# and dynamo for read it and apply to Civil3D application. Base of file structure was getting by Autodesk Revit shared parameters file, [read more about it](https://knowledge.autodesk.com/support/revit/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/Revit-Model/files/GUID-E7D12B71-C50D-46D8-886B-8E0C2B285988-htm.html#:~:text=Shared%20parameter%20definitions%20are%20stored,in%20multiple%20families%20or%20projects.).

# File description
This is classic TXT file with Unicode (UTF8) characters set with tab ```\t``` separators. 

Symbol | About
--|--
🟢 | Const field (using as wrote);
🟤 | Tab char - ```\t```;
🟡 | User's variables;
🟠 | Value from static collection (fix type);

Structure of file represent at table below (without any user's data, only symbols above, const fiels names and *recommended data type* for each field):

🟢 \#C3D PSet file|🟤|🟤|🟤|🟤|🟤|🟤|🟤
:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:
🟢 \*META|🟢 VERSION |🟢 MINVERSION|🟤|🟤|🟤|🟤|🟤
🟢 META|🟡 *integer*|🟡 *integer*|🟤|🟤|🟤|🟤|🟤
🟢 \*GROUP|🟢 ID|🟢 NAME|🟢 APPLYTO|🟢 DESCRIPTION|🟤|🟤|🟤
🟢 GROUP|🟡 *integer*|🟡 *string without symbols*|🟠 *string without tabs*|🟡 *any strings*|🟤|🟤|🟤
...|...|...|...|...|...|...|...|
🟢 \*PARAM|🟢 GUID|🟢 NAME|🟢 DATATYPE|🟢 GROUP|🟢 VISIABLE|🟢 DESCRIPTION|🟢 ORDER
🟢 PARAM|🟡 *guid*|🟡 *string without tabs*|🟠 *string without tabs*|🟡 *integer*|🟡 *boolean*|🟡 *any strings*|🟡 *integer*
...|...|...|...|...|...|...|...|
...|...|...|...|...|...|...|...|
