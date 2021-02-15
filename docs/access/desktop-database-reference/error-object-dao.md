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

**Объект** error содержит сведения об ошибках доступа к данным, каждая из которых относится к одной операции с DAO.

## <a name="remarks"></a>Заметки

Любая операция, включаемая DAO, может вызвать одну или несколько ошибок. Например, вызов сервера ODBC может привести к ошибке сервера базы данных, ошибке ODBC и ошибке DAO. При каждой такой ошибке объект **Error** помещается в коллекцию **Errors** объекта **DBEngine.** Таким образом, одно событие может привести к от появления нескольких объектов **Error** в коллекции **Errors.**

Когда последующая операция DAO создает ошибку, коллекция **Errors** очищается, и один или несколько новых объектов **Error** помещаются в коллекцию **Errors.** Операции DAO, которые не вызывают ошибку, не влияют на коллекцию **ошибок.**

Набор объектов **Error** в коллекции **Errors** описывает одну ошибку. Первый объект **Error** — это ошибка самого низкого уровня (исходная ошибка), вторая — следующая ошибка более высокого уровня и так далее. Например, если при попытке открыть объект **[Recordset](recordset-object-dao.md)** возникает ошибка ODBC, первый объект **Error** ( **Errors**(0) содержит ошибку самого низкого уровня ODBC; последующие ошибки содержат ошибки ODBC, возвращенные различными уровнями ODBC. В этом случае диспетчер драйверов ODBC и, возможно, сам драйвер возвращают отдельные **объекты error.** Последний **объект Error** ( **Errors.Count-** 1) содержит ошибку DAO, указывающее на то, что не удалось открыть объект.

Enumerating the specific errors in the Errors collection enables your error-handling **routines** to more precisely determine the cause and origin of an error, and take appropriate steps to recover. Вы можете прочитать свойства объекта **Error,** чтобы получить подробные сведения о каждой ошибке, в том числе:

  - Свойство **[Description,](error-description-property-dao.md)** которое содержит текст оповещения об ошибке, которое будет отображаться на экране, если ошибка не будет перехранна.

  - Свойство **[Number,](error-number-property-dao.md)** которое содержит длинное integer значение константы ошибки.

  - Свойство **[Source,](error-source-property-dao.md)** которое идентифицирует объект, который вызывает ошибку. Это особенно полезно, если в коллекции **errors** есть несколько объектов **Errors** после запроса к источнику данных ODBC.

  - Свойства **HelpFile** и **HelpContext,** которые указывают соответствующий файл справки Microsoft Windows и раздел справки соответственно (если они существуют) для ошибки.
    

    > [!NOTE]
    > При программировании в Microsoft Visual Basic для приложений (VBA) при использовании ключевого слова **New** для создания объекта, который впоследствии вызывает ошибку перед его  приложением к коллекции, коллекция ошибок объекта **DBEngine** не будет содержать запись об ошибке этого объекта, так как новый объект не связан с объектом **DBEngine.** Однако сведения об ошибке доступны в объекте VBA **Err.** Код обработки ошибок VBA должен проверять коллекцию **ошибок** всякий раз, когда ожидается ошибка доступа к данным. 
    > 
    > Если вы пишете централизованный обработитель ошибок, протестировать объект VBA **Err,** чтобы определить, допустимы ли сведения об ошибке в коллекции **Errors.** Если свойство **Number** последнего элемента коллекции **Errors** (DBEngine.Errors.Count - 1) и значение объекта **Err** совпадают, можно использовать серию заявлений **Select Case** для определения конкретной ошибки ИЛИ ошибок DAO. Если они не совпадают, используйте метод [Refresh](errors-refresh-method-dao.md) в коллекции **Errors.**



## <a name="example"></a>Пример

В этом примере показана привратная ошибка, ее ловка и отображение свойств **Description,** **Number,** **Source,** **HelpContext** и **HelpFile** итоговых объектов **Error.**

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

