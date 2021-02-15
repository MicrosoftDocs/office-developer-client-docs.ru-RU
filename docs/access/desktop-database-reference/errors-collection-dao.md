---
title: Errors collection (DAO)
TOCTitle: Errors Collection
ms:assetid: d42007b5-6410-14e9-baf9-9306fdef38f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834805(v=office.15)
ms:contentKeyID: 48547929
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf8e891936d4f8bd03535fa199026bc4ad8ff9ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293415"
---
# <a name="errors-collection-dao"></a>Errors collection (DAO)


**Область применения**: Access 2013, Office 2013

Коллекция **Errors** содержит все сохраненные объекты **Error,** каждый из которых относится к одной операции с DAO.

## <a name="remarks"></a>Заметки

Любая операция, включаемая объекты DAO, может создавать одну или несколько ошибок. При каждой ошибке один или несколько объектов **Error** помещаются в коллекцию **Errors** объекта **DBEngine.** Когда другая операция DAO создает ошибку, коллекция **Errors** очищается, а новый набор объектов **Error** помещается в коллекцию **Errors.** Объект с самым высоким номером в коллекции **Errors** (DBEngine.Errors.Count - 1) соответствует ошибке, сообщаемой объектом **Err** Microsoft Visual Basic для приложений (VBA).

Операции DAO, которые не вызывают ошибку, не влияют на коллекцию **ошибок.**

Элементы коллекции **Errors** не примеся, так как они обычно находятся в других коллекциях, поэтому коллекция **Errors** не поддерживает методы **Append** и **Delete.**

Набор объектов **Error** в коллекции **Errors** описывает одну ошибку. Первый объект **Error** — это ошибка самого низкого уровня, второй — следующий более высокий и так далее. Например, если при попытке открыть объект **[Recordset](recordset-object-dao.md)** возникает ошибка ODBC, первый объект ошибки содержит ошибку самого низкого уровня ODBC; последующие ошибки содержат ошибки ODBC, возвращенные различными уровнями ODBC. В этом случае диспетчер драйверов ODBC и, возможно, сам драйвер возвращают отдельные **объекты error.** Последний объект **Error** содержит ошибку DAO, указывающее на то, что не удалось открыть объект.

Enumerating the specific errors in the Errors collection enables your error-handling **routines** to more precisely determine the cause and origin of an error, and take appropriate steps to recover.


> [!NOTE]
> Если ключевое слово **New** используется для создания объекта, который вызывает ошибку до или во время его вложения в коллекцию **Errors,** коллекция не содержит сведений об ошибке этого объекта, так как новый объект не связан с объектом **DBEngine.** Однако сведения об ошибке доступны в объекте VBA **Err.**

## <a name="example"></a>Пример

В этом примере показана приодерживая ошибка, она застигает ее и отображает свойства **Description,** **Number,** **Source,** **HelpContext** и **HelpFile** итоговых объектов **Error.**

```vb 
Sub DescriptionX() 
 
 Dim dbsTest As Database 
 
 On Error GoTo ErrorHandler 
 
 ' Intentionally trigger an error. 
 Set dbsTest = OpenDatabase("NoDatabase") 
 
 Exit Sub 
 
ErrorHandler: 
 Dim strError As String 
 Dim errLoop As Error 
 
 ' Enumerate Errors collection and display properties of 
 ' each Error object. 
 For Each errLoop In Errors 
 With errLoop 
 strError = _ 
 "Error #" & .Number & vbCr 
 strError = strError & _ 
 " " & .Description & vbCr 
 strError = strError & _ 
 " (Source: " & .Source & ")" & vbCr 
 strError = strError & _ 
 "Press F1 to see topic " & .HelpContext & vbCr 
 strError = strError & _ 
 " in the file " & .HelpFile & "." 
 End With 
 MsgBox strError 
 Next 
 
 Resume Next 
 
End Sub 
 
```

