---
title: Семейство errors (DAO)
TOCTitle: Errors Collection
ms:assetid: d42007b5-6410-14e9-baf9-9306fdef38f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834805(v=office.15)
ms:contentKeyID: 48547929
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf8e891936d4f8bd03535fa199026bc4ad8ff9ba
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704569"
---
# <a name="errors-collection-dao"></a>Семейство errors (DAO)


**Применимо к**: Access 2013, Office 2013

Семейство **Errors** содержит все хранимые объекты **ошибки** , каждая из которых относятся к одной операции, включающие использование DAO.

## <a name="remarks"></a>Замечания

Любые операции, включающие использование объектов DAO можно создать одну или несколько ошибок. Как возникают ошибки, один или несколько объектов **Ошибка** помещаются в семействе **Errors** объекта **DBEngine** . Когда другой операции DAO создает сообщение об ошибке, семейство **Errors** снят и новый набор объектов **ошибок** переводится в семейство **Errors** . Объект наибольший номер в семействе **Errors** (DBEngine.Errors.Count - 1) соответствует с Microsoft Visual Basic для приложений (VBA) **Err** объекта сообщение об ошибке.

DAO операций, которые не возникнет ошибка не оказывают влияния на семейство **Errors** .

Элементы семейства **Errors** не добавлено как обычно в других семействах сайтов, семейство **Errors** не поддерживает методы **добавления** и **удаления** .

Набор объектов **об ошибке** в семействе **Errors** описаны одной ошибки. Первый объект **Error** является низшего уровня ошибки, второй — верхнего уровня и т. д. Например если возникает ошибка ODBC при попытке открыть объект **[набора записей](recordset-object-dao.md)** , первый объект error содержит низшего уровня ошибка ODBC; последующие сообщения об ошибках содержат ODBC ошибок, возвращаемых различные уровни ODBC. В этом случае драйвера ODBC и драйвера себе возвращают отдельные объекты **ошибки** . Последний объект **Error** содержит ошибки DAO, указывающее на то, что не удалось открыть объект.

Перечисление отдельных ошибок в семействе **Errors** позволяет вашей процедуры обработки ошибок более точно определить причину и источник ошибки и выполните соответствующие действия для восстановления.


> [!NOTE]
> При использовании ключевого слова **New** для создания объекта, который вызывает ошибку перед или во время ставится в коллекцию **ошибок** , эта коллекция не содержит сведения об объекте, так как новый объект не связан с Объект **DBEngine** . Тем не менее сведения об ошибке доступна в объекте VBA **Err** .

## <a name="example"></a>Пример

В этом примере принудительно ошибку, его перехватывает и отображает свойства **Description**, **номер**, **источник**, **HelpContext**и **HelpFile** итоговый объект **Error** .

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

