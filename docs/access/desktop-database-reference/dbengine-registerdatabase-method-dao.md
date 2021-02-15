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

Введите сведения о под соединении для источника данных ODBC в реестре Windows. Драйверу ODBC необходимы сведения о под подключениех при открытом источнике данных ODBC во время сеанса.

## <a name="syntax"></a>Синтаксис

*выражение .* RegisterDatabase(***Dsn***, ***Driver***, ***Silent***, ***Attributes***)

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
<td><p>Обязательно</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>имя, используемого в <strong><a href="dbengine-opendatabase-method-dao.md">методе OpenDatabase.</a></strong> Он ссылается на блок описательных сведений об источнике данных. Например, если источником данных является удаленная база данных ODBC, это может быть имя сервера.</p></td>
</tr>
<tr class="even">
<td><p><em>Driver</em></p></td>
<td><p>Обязательно</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Имя драйвера ODBC. Это не имя DLL-файла драйвера ODBC.</p></td>
</tr>
<tr class="odd">
<td><p><em>Silent</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Логический</strong></p></td>
<td><p><strong>True,</strong> если вы не хотите отображать диалоговое окно драйвера ODBC с запросом сведений о драйверах; Или <strong>false,</strong> если вы хотите отобразить диалоговое окно драйвера ODBC. Если параметр silent имеет <strong>true,</strong>атрибуты должны содержать все необходимые сведения, необходимые для драйверов, иначе диалоговое окно все равно будет отображаться.</p></td>
</tr>
<tr class="even">
<td><p><em>Атрибуты</em></p></td>
<td><p>Обязательно</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Список ключевых слов, добавляемого в реестр Windows. Ключевые слова находятся в строке с делегировкой возврата каретки.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

Если база данных уже зарегистрирована (сведения о под подключениех уже введены) в реестре Windows при использовании метода **RegisterDatabase,** сведения о под подключением обновляются.

Если метод **RegisterDatabase** по какой-либо причине не удается, в реестр Windows не внося никаких изменений и возникает ошибка.

Дополнительные сведения о драйверах ODBC, таких как SQL Server, см. в файле справки, предоставленного драйвером.

## <a name="example"></a>Пример

В этом примере метод **RegisterDatabase** используется для регистрации Microsoft SQL Server данных Publishers в реестре Windows.

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

