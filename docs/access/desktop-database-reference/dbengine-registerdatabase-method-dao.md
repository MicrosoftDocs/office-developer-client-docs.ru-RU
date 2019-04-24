---
title: Метод DBEngine. RegisterDatabase (DAO)
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
# <a name="dbengineregisterdatabase-method-dao"></a>Метод DBEngine. RegisterDatabase (DAO)

**Область применения**: Access 2013, Office 2013

Вводит сведения о подключении для источника данных ODBC в реестре Windows. Драйверу ODBC необходимы сведения о подключении при открытии источника данных ODBC во время сеанса.

## <a name="syntax"></a>Синтаксис

*Expression* . RegisterDatabase (***DSN***, ***Driver***, ***Silent***, ***Attributes***)

*Expression (выражение* ) Переменная, представляющая объект **DBEngine** .

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
<th><p>Обязательно/необязательно</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Имя</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>имя, используемое в методе <strong><a href="dbengine-opendatabase-method-dao.md">openDatabase</a></strong> . Он ссылается на блок описательных сведений о источнике данных. Например, если источником данных является удаленная база данных ODBC, это может быть имя сервера.</p></td>
</tr>
<tr class="even">
<td><p><em>Driver</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Имя драйвера ODBC. Это имя не является файлом DLL драйвера ODBC.</p></td>
</tr>
<tr class="odd">
<td><p><em>Удаля</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Логический</strong></p></td>
<td><p><strong>Значение true</strong> , если вы не хотите отображать диалоговые окна драйвера ODBC, в которых запрашиваются сведения об определенном драйвере; или <strong>false</strong> , если вы хотите отобразить диалоговые окна драйвера ODBC. Если свойство Silent имеет <strong>значение true</strong>, атрибуты должны содержать все необходимые сведения о конкретном драйвере, а диалоговые окна отображаются в любом случае.</p></td>
</tr>
<tr class="even">
<td><p><em>Attributes</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Список ключевых слов, которые необходимо добавить в реестр Windows. Ключевые слова находятся в строке со строками, разделенными символами возврата каретки.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Если база данных уже зарегистрирована (сведения о подключении уже введены) в реестре Windows при использовании метода **RegisterDatabase** , сведения о подключении обновляются.

Если метод **RegisterDatabase** по какой либо причине завершается с ошибкой, в реестр Windows не вносятся никакие изменения, и возникает ошибка.

Для получения дополнительных сведений о драйверах ODBC, таких как SQL Server, обратитесь к справочному файлу, указанному в драйвере.

## <a name="example"></a>Пример

В этом примере используется метод **RegisterDatabase** для регистрации источника данных Microsoft SQL Server с именем "Publishers" в реестре Windows.

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

