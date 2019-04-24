---
title: Объект Error — объекты доступа к данным (DAO)
TOCTitle: Error Object
ms:assetid: e2608bc9-bece-9b47-4562-7a2689601f75
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835711(v=office.15)
ms:contentKeyID: 48548289
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3fdfe2091dc2be562f60e5e9cc1935291a74a11d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293478"
---
# <a name="error-object-dao"></a>Объект Error (DAO)


**Область применения**: Access 2013, Office 2013

Объект **Error** содержит сведения об ошибках доступа к данным, каждая из которых относится к одной операции, включающей в себя DAO.

## <a name="remarks"></a>Замечания

Любая операция, включающая DAO, может создать одну или несколько ошибок. Например, вызов сервера ODBC может привести к ошибке на сервере базы данных, ошибке ODBC и ошибка DAO. При возникновении такой ошибки объект **Error** помещается в коллекцию **Errors** объекта **DBEngine** . При наличии одного события может появиться несколько появляющихся объектов **Error** в **** коллекции Errors.

Когда последующая операция DAO создает ошибку, коллекция **Errors** очищается, а в коллекцию Errors помещаются один или несколько новых объектов **** **Error** . Операции DAO, не создающие ошибку, не влияют на коллекцию **Errors** .

В наборе объектов **Error** в семействе **Errors** описывается одна ошибка. Первый объект **Error** — это ошибка самого низкого уровня (исходная ошибка), вторая — следующая ошибка более высокого уровня и так далее. Например, при возникновении ошибки ODBC при попытке открыть объект **[Recordset](recordset-object-dao.md)** первый объект **Error** — **ошибки**(0) — содержит ошибку ODBC самого низкого уровня; Последующие ошибки содержат ошибки ODBC, возвращенные различными уровнями ODBC. В этом случае диспетчер драйверов ODBC и, возможно, сам драйвер возвращают отдельные объекты **Error** . Последний объект **Error** — **Errors. Count-** 1 — содержит ошибку DAO, указывающую на то, что не удалось открыть объект.

ПереЧисление определенных ошибок в семействе Errors позволяет подпрограммам обработки ошибок определять причину и происхождение ошибки и выполнять необходимые действия для восстановления. **** Вы можете прочитать свойства объекта **Error** , чтобы получить конкретные сведения об ошибке, в том числе:

  - Свойство **[Description](error-description-property-dao.md)** , которое содержит текст оповещения об ошибке, который будет отображаться на экране, если ошибка не перехвачена.

  - Свойство **[Number](error-number-property-dao.md)** , которое содержит длинное целое значение константы ошибки.

  - Свойство **[Source](error-source-property-dao.md)** , которое определяет объект, вызвавший ошибку. Это особенно полезно при наличии нескольких объектов **Error** в коллекции Errors **** после запроса к источнику данных ODBC.

  - Свойства **HelpFile** и **HelpContext** , указывающие соответствующий справочный файл Microsoft Windows и раздел справки (если они существуют) для ошибки.
    

    > [!NOTE]
    > При программировании в Microsoft Visual Basic для приложений (VBA), если вы используете ключевое слово **New** для создания объекта, который затем вызывает ошибку перед добавлением этого объекта в коллекцию, **ошибки** объекта **DBEngine** Коллекция не будет содержать запись об ошибке этого объекта, так как новый объект не связан с объектом **DBEngine** . Однако сведения об ошибке доступны в объекте VBA **Err** . Код обработки ошибок в VBA должен проверять коллекцию **ошибок** всякий раз, когда предполагается наличие ошибки доступа к данным. 
    > 
    > Если вы пишете централизованный обработчик ошибок, проверьте объект VBA **Err** , чтобы определить, действительны ли сведения об **** ошибке в семействе Errors. Если свойство **Number** последнего элемента коллекции Errors (DBEngine **** . Errors. Count-1) и значение объекта **Err** совпадают, можно использовать ряд операторов **Select Case** для определения конкретной ошибки DAO или произошедшие ошибки. Если они не совпадают, используйте метод [Refresh](errors-refresh-method-dao.md) в коллекции Errors **** .



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
            "  " & .Description & vbCr 
         strError = strError & _ 
            "  (Source: " & .Source & ")" & vbCr 
         strError = strError & _ 
            "Press F1 to see topic " & .HelpContext & vbCr 
         strError = strError & _ 
            "  in the file " & .HelpFile & "." 
      End With 
      MsgBox strError 
   Next 
 
   Resume Next 
 
End Sub 
 
```

