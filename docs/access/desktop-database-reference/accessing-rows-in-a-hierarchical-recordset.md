---
title: Accessing Rows in a Hierarchical Recordset
TOCTitle: Accessing Rows in a Hierarchical Recordset
ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15)
ms:contentKeyID: 48548104
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a7596341f96c7df1d51e67721aacd15f8b075f25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482955"
---
# <a name="accessing-rows-in-a-hierarchical-recordset"></a>Accessing Rows in a Hierarchical Recordset


**Применимо к**: Access 2013 | Office 2013

В следующем примере показано действия, необходимые для доступа к строк в иерархической [набора записей](recordset-object-ado.md):

1.  Объекты **набора записей** из авторов и titleauthor таблицы связаны с идентификатором автора.

2.  Внешний цикл отображается имя и фамилию, состояние и идентификации каждого автора.

3.  Добавленный **набора записей** для каждой строки извлекается из коллекции **полей** и назначается *rstTitleAuthor*.

4.  Внутренний цикл отображаются четыре поля из каждой строки в присоединенной **набора записей**.

(Свойство [StayInSync](stayinsync-property-ado.md) задано значение FALSE для наглядности, чтобы увидеть, главы явным образом изменить в каждой итерации внешнего цикла. Тем не менее пример будет более эффективным, если назначение на шаге 3 перемещается перед первой строки на шаге 2, поэтому назначения выполняется только один раз. Задайте свойство **StayInSync** имеет значение TRUE, таким образом, чтобы *rstTitleAuthor* неявно и автоматически изменится на соответствующий главы каждый раз, когда *rst* перемещает на новую строку.)

**Пример**

```vb 
 
Sub datashape() 
 Dim cnn As New ADODB.Connection 
 Dim rst As New ADODB.Recordset 
 Dim rstTitleAuthor As New ADODB.Recordset 
 
 cnn.Provider = "MSDataShape" 
 cnn.Open "Data Provider=MSDASQL;" & _ 
 "Data Source=SRV;" & _ 
 "User Id=MyUserName;Password=MyPassword;Database=Pubs" 
' STEP 1 
 rst.StayInSync = FALSE 
 rst.Open "SHAPE {select * from authors} " & _ 
 "APPEND ({select * from titleauthor} " & _ 
 "RELATE au_id TO au_id) AS chapTitleAuthor", _ 
 cnn 
' STEP 2 
 While Not rst.EOF 
 Debug.Print rst("au_fname"), rst("au_lname"), _ 
 rst("state"), rst("au_id") 
' STEP 3 
 Set rstTitleAuthor = rst("chapTitleAuthor").Value 
' STEP 4 
 While Not rstTitleAuthor.EOF 
 Debug.Print rstTitleAuthor(0), rstTitleAuthor(1), _ 
 rstTitleAuthor(2), rstTitleAuthor(3) 
 rstTitleAuthor.MoveNext 
 Wend 
 rst.MoveNext 
 Wend 
End Sub 
```

