---
title: Коллекция Errors (DAO)
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
# <a name="errors-collection-dao"></a>Коллекция Errors (DAO)


**Область применения**: Access 2013, Office 2013

Коллекция **Errors** содержит все хранимые объекты **Error** , каждая из которых относится к одной операции, включающей в себя DAO.

## <a name="remarks"></a>Примечания

Любая операция, включающая объекты DAO, может вызвать одну или несколько ошибок. При возникновении каждой ошибки в коллекцию **Errors** объекта **DBEngine** помещаются один или несколько объектов **Error** . Если при выполнении другой операции DAO возникает ошибка, удаляется коллекция **Errors** , и в коллекцию **Errors** помещается новый набор объектов **Error** . Объект с самыми высокими номерами в коллекции **Errors** (DBEngine. Errors. Count-1) соответствует ошибке, указанной в объекте **Err** языка Microsoft Visual Basic для приложений (VBA).

Операции DAO, не создающие ошибку, не влияют на коллекцию **Errors** .

Элементы коллекции **Errors** не добавляются, как правило, с другими коллекциями, поэтому коллекция **Errors** не поддерживает методы **append** и **Delete** .

В наборе объектов **Error** в семействе **Errors** описывается одна ошибка. Первый объект **Error** — это ошибка самого нижнего уровня, второй следующий более высокий уровень и т. д. Например, если при попытке открыть объект **[Recordset](recordset-object-dao.md)** возникла ошибка ODBC, первый объект Error содержит ошибку ODBC самого низкого уровня; Последующие ошибки содержат ошибки ODBC, возвращенные различными уровнями ODBC. В этом случае диспетчер драйверов ODBC и, возможно, сам драйвер возвращают отдельные объекты **Error** . Последний объект **Error** содержит ошибку DAO, указывающую на то, что не удалось открыть объект.

Перечисление определенных ошибок **в семействе Errors** позволяет подпрограммам обработки ошибок определять причину и происхождение ошибки и выполнять необходимые действия для восстановления.


> [!NOTE]
> Если вы используете ключевое слово **New** для создания объекта, который вызывает ошибку до или во время помещения в коллекцию **Errors** , коллекция не содержит сведения об ошибке для этого объекта, так как новый объект не связан с объектом **DBEngine** . Однако сведения об ошибке доступны в объекте VBA **Err** .

## <a name="example"></a>Пример

В этом примере вызывается ошибка, выполняется ее перехват и отображаются свойства **Description**, **Number**, **Source**, **HelpContext**и **HelpFile** полученного объекта **Error** .

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

