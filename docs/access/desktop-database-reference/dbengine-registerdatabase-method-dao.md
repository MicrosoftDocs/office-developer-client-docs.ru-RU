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
ms.openlocfilehash: 767bd146de7a5568d7441024adb9ad6816cb806e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923513"
---
# <a name="dbengineregisterdatabase-method-dao"></a>Метод DBEngine.RegisterDatabase (DAO)


**Применимо к**: Access 2013, Office 2013


Вводит сведения о подключении к источнику данных ODBC в реестре Windows. Драйвер ODBC требуются данные подключения при открытии источника данных во время сеанса.

## <a name="syntax"></a>Синтаксис

*выражение* . RegisterDatabase (***уведомления о доставке***, ***драйвер***, ***Автоматическая***, ***атрибуты***)

*выражение* Переменная, которая представляет собой объект- **DBEngine** .

### <a name="parameters"></a>Параметры

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Уведомления о доставке</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>имя, используемое в методе <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> . Он ссылается на блок описательные сведения об источнике данных. Например если источник данных ODBC удаленной базы данных, может быть имя сервера.</p></td>
</tr>
<tr class="even">
<td><p>Драйвер</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Имя драйвера ODBC. Это не имя DLL-файла драйвера ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Автоматическая</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Boolean</strong></p></td>
<td><p><strong>Значение true,</strong> Если вы не хотите отображение диалоговых окон драйвера ODBC, запрашивающие сведения; или <strong>значение False,</strong> Если необходимо отобразить диалоговые окна драйвера ODBC. Если автоматическая имеет <strong>значение True</strong>, атрибуты должно содержать все необходимые сведения или диалоговые окна отображаются все равно.</p></td>
</tr>
<tr class="even">
<td><p>Атрибуты</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Список ключевых слов для добавления к реестра Windows. Ключевые слова находятся в возврат каретки return – запятой строку.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Если база данных уже зарегистрирована (сведения о подключении к уже введены) в реестре Windows при использовании метода **RegisterDatabase** обновляется сведения о подключении.

В случае сбоя метода **RegisterDatabase** по любой причине никаких изменений не производится реестра Windows, и возникает ошибка.

Дополнительные сведения о драйверы ODBC, такие как SQL Server файл справки, входящие в состав драйвера см.

## <a name="example"></a>Пример

В этом примере используется метод **RegisterDatabase** для регистрации источника данных Microsoft SQL Server с именем издателей в реестре Windows.

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

