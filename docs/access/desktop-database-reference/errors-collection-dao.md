---
title: Коллекция ошибок (DAO)
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
# <a name="errors-collection-dao"></a>Коллекция ошибок (DAO)


**Область применения**: Access 2013, Office 2013

Коллекция **ошибок** содержит все сохраненные объекты **ошибки,** каждый из которых относится к одной операции с участием DAO.

## <a name="remarks"></a>Примечания

Любая операция с объектами DAO может создавать одну или несколько ошибок. По мере возникновения каждой ошибки один или несколько объектов **ошибки** помещаются в коллекцию **Ошибок** объекта **DBEngine.** Когда другая операция DAO создает  ошибку, коллекция ошибок очищается  и новый набор объектов ошибки помещается в коллекцию **Ошибок.** Объект с самым высоким номером в коллекции Ошибок (DBEngine.Errors.Count - 1) соответствует ошибке, сообщаемой объектом **Err** microsoft Visual Basic для приложений (VBA). 

Операции DAO, которые не создают ошибку, не влияют на коллекцию **ошибок.**

Элементы коллекции **Ошибок** не примыкают к ним, как правило,  с другими коллекциями,  поэтому коллекция Ошибок не поддерживает методы приложения и **удаления.**

Набор объектов **ошибки** в коллекции **Errors** описывает одну ошибку. Первый объект **Error** — это ошибка самого низкого уровня, вторая — более высокого уровня и так далее. Например, если при попытке открыть объект **[Recordset](recordset-object-dao.md)** возникает ошибка ODBC, первый объект ошибки содержит ошибку самого низкого уровня; последующие ошибки содержат ошибки ODBC, возвращаемые различными слоями ODBC. В этом случае диспетчер драйвера ODBC и, возможно, сам драйвер возвращают отдельные **объекты ошибки.** Последний объект **Error** содержит ошибку DAO, указывающее, что объект не может быть открыт.

Переопределение определенных ошибок  в коллекции Ошибок позволяет вашим процедурам обработки ошибок точнее определить причину и происхождение ошибки и принять соответствующие меры для восстановления.


> [!NOTE]
> Если вы используете ключевое слово **New** для создания объекта, который  вызывает ошибку до или во время их вложения в коллекцию Ошибок, коллекция не содержит сведений об ошибках этого объекта, так как новый объект не связан с объектом **DBEngine.** Однако сведения об ошибках доступны в объекте VBA **Err.**

## <a name="example"></a>Пример

В этом примере приводится ошибка, она ловушек, и отображает описание **,** номер **,** **источник**, **HelpContext** и **HelpFile** свойства в результате **объекта Ошибки.**

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

