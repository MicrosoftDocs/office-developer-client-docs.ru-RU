---
title: Метод DBEngine.RegisterDatabase (DAO)
TOCTitle: RegisterDatabase Method
ms:assetid: ed87a694-2c89-0a78-5d8b-0cc7e09fadff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836347(v=office.15)
ms:contentKeyID: 48548541
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052938
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 632f6e10d79d74dfef295b34a52ce62f1690101b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294227"
---
# <a name="dbengineregisterdatabase-method-dao"></a>Метод DBEngine.RegisterDatabase (DAO)

**Область применения**: Access 2013, Office 2013

Вводит сведения о подключении для источника данных ODBC в Windows реестре. Драйверу ODBC необходимы сведения о подключении, когда источник данных ODBC открыт во время сеанса.

## <a name="syntax"></a>Синтаксис

*выражения* . RegisterDatabase ***(Dsn,*** ***driver***, ***Silent***, ***Attributes***)

*expression*: переменная, представляющая объект **DBEngine**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Dsn</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>имя, используемого в <strong><a href="dbengine-opendatabase-method-dao.md">методе OpenDatabase.</a></strong> Он относится к блоку описательных сведений об источнике данных. Например, если источником данных является удаленная база данных ODBC, это может быть имя сервера.</p></td>
</tr>
<tr class="even">
<td><p><em>Driver</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Имя драйвера ODBC. Это не имя DLL-файла драйвера ODBC.</p></td>
</tr>
<tr class="odd">
<td><p><em>Silent</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Логический</strong></p></td>
<td><p><strong>True,</strong> если вы не хотите отображать диалоги драйверов ODBC, которые подсказывут сведения о конкретном драйвере; или <strong>False,</strong> если вы хотите отобразить диалоговое окно драйвера ODBC. Если silent is <strong>True,</strong>атрибуты должны содержать всю необходимую информацию для конкретного драйвера или диалоговое окно отображается в любом случае.</p></td>
</tr>
<tr class="even">
<td><p><em>Attributes</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Список ключевых слов, которые необходимо добавить в Windows реестра. Ключевые слова находятся в строке с делимитированной строкой с возвратом перевозки.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Если база данных уже зарегистрирована (сведения о подключении уже введены) в реестре Windows при использовании метода **RegisterDatabase,** сведения о подключении обновляются.

Если метод **RegisterDatabase** по какой-либо причине не удается, изменения в Windows реестра не происходят, и возникает ошибка.

Дополнительные сведения о драйверах ODBC, таких как SQL Server, см. в файле справки, предоставленной драйверу.

## <a name="example"></a>Пример

В этом примере метод **RegisterDatabase** используется для Microsoft SQL Server источника данных с именем Publishers в Windows реестре.

```vb 
Sub RegisterDatabaseX() 
 
 Dim dbsRegister As Database 
 Dim strDescription As String 
 Dim strAttributes As String 
 Dim errLoop As Error 
 
 ' Build keywords string. 
 strDescription = InputBox( "Enter a description " & _ 
 "for the database to be registered.") 
 strAttributes = "Database=pubs" & _ 
 vbCr & "Description=" & strDescription & _ 
 vbCr & "OemToAnsi=No" & _ 
 vbCr & "Server=Server1" 
 
 ' Update Windows Registry. 
 On Error GoTo Err_Register 
 DBEngine.RegisterDatabase "Publishers", "SQL Server", _ 
 True, strAttributes 
 On Error GoTo 0 
 
 MsgBox "Use regedit.exe to view changes: " & _ 
 "HKEY_CURRENT_USER\" & _ 
 "Software\ODBC\ODBC.INI" 
 
 Exit Sub 
 
Err_Register: 
 
 ' Notify user of any errors that result from 
 ' the invalid data. 
 If DBEngine.Errors.Count > 0 Then 
 For Each errLoop In DBEngine.Errors 
 MsgBox "Error number: " & errLoop.Number & _ 
 vbCr & errLoop.Description 
 Next errLoop 
 End If 
 
 Resume Next 
 
End Sub 
 
```

