---
title: Объекты объект Error - доступ к данным (DAO)
TOCTitle: Error Object
ms:assetid: e2608bc9-bece-9b47-4562-7a2689601f75
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835711(v=office.15)
ms:contentKeyID: 48548289
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62b195907d5acc05832c1feac45165aadd9e14d1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481082"
---
# <a name="error-object-dao"></a>Error Object (DAO)


**Применимо к**: Access 2013 | Office 2013

Объект **Error** содержит сведения об ошибках доступа к данным, каждая из которых относятся к одной операции, включающие использование DAO.

## <a name="remarks"></a>Замечания

Любые операции, включающие использование DAO можно создать одну или несколько ошибок. Например вызов на сервер ODBC может привести ошибка с сервера баз данных, ошибку из ODBC и DAO ошибки. Как происходит каждой такой ошибки, объект **Error** помещается в семействе **Errors** объекта **DBEngine** . Одно событие может привести несколько объектов **ошибок** , изображения которых появляются в семейство **Errors** .

При последующих операций DAO создает сообщение об ошибке, семейство **Errors** снимается и один или несколько новых объектов **Ошибка** помещаются в семействе **Errors** . DAO операций, которые не возникнет ошибка не оказывают влияния на семейство **Errors** .

Набор объектов **об ошибке** в семействе **Errors** описаны одной ошибки. Первый объект **Error** является низшего уровня ошибка (ошибка исходную), второй — следующей ошибке более высокого уровня и т. д. Например, если при попытке открыть объект **[набора записей](recordset-object-dao.md)** первый объект **Error** , возникает ошибка ODBC — **ошибки**(0) — содержит низшего уровня ошибка ODBC; последующие сообщения об ошибках содержат ODBC ошибок, возвращаемых различные уровни ODBC. В этом случае драйвера ODBC и драйвера себе возвращают отдельные объекты **ошибки** . Последний объект **Error** — **Errors.Count -** 1 — содержит ошибки DAO, указывающее на то, что не удалось открыть объект.

Перечисление отдельных ошибок в семействе **Errors** позволяет вашей процедуры обработки ошибок более точно определить причину и источник ошибки и выполните соответствующие действия для восстановления. Можно считать свойства объект **Error** получить подробные сведения о каждой ошибки, включая:

  - Свойство **[Описание](error-description-property-dao.md)** , которое содержит текст, который будет отображаться на экране ошибки, не представленные сообщение об ошибке.

  - Свойство **[номер](error-number-property-dao.md)** , которое содержит значение "длинное целое" Ошибка константа.

  - Свойство **[Source](error-source-property-dao.md)** определяет объект, который вызвал ошибку. Это особенно удобно в тех случаях, когда у вас имеется несколько объектов **об ошибке** в семействе **Errors** следующий запрос к источнику данных ODBC.

  - **Файл справки** и **HelpContext** свойства, которые указывают соответствующего файла справки Microsoft Windows и раздел справки, соответственно, (если они существуют) для ошибки.
    

    > [!NOTE]
    > <P>При программировании в Microsoft Visual Basic для приложений (VBA), при использовании ключевого слова <STRONG>New</STRONG> для создания объекта, который затем вызывает ошибку перед этот объект был добавлен коллекцию объектов <STRONG>DBEngine</STRONG> <STRONG>ошибки</STRONG> семейства сайтов не будет содержать запись для этого объекта ошибки, так как новый объект не связан с объектом <STRONG>DBEngine</STRONG> . Тем не менее сведения об ошибке доступна в объекте VBA <STRONG>Err</STRONG> . Код обработки ошибок VBA следует изучить семейство <STRONG>Errors</STRONG> каждый раз, когда поступает ошибка доступа к данным. При создании обработчик централизованного ошибок проверки объекта VBA <STRONG>Err</STRONG> , чтобы определить допустимость сведения об ошибке в семействе <STRONG>Errors</STRONG> . Если свойство <STRONG>номер</STRONG> последнего элемента семейство <STRONG>Errors</STRONG> (DBEngine.Errors.Count - 1) и значение объекта <STRONG>Err</STRONG> , соответствуют, воспользуйтесь последовательность операторов <STRONG>Select Case</STRONG> для определения конкретной ошибки DAO или ошибки, возникшие. Если они не совпадают, используйте метод <STRONG><A href="errors-refresh-method-dao.md">Refresh</A></STRONG> на семейство <STRONG>Errors</STRONG> .</P>



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

