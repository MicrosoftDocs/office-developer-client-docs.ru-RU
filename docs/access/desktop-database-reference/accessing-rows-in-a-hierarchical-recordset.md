---
title: Доступ к строкам в иерархическом наборе записей
TOCTitle: Accessing rows in a hierarchical Recordset
ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15)
ms:contentKeyID: 48548104
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a80b089fa72ef01eb1b4b2f1dae494e002c6a6fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281958"
---
# <a name="accessing-rows-in-a-hierarchical-recordset"></a>Доступ к строкам в иерархическом наборе записей

**Область применения**: Access 2013, Office 2013

В следующем примере показаны действия, необходимые для доступа к строкам в иерархическом [наборе записей:](recordset-object-ado.md)

1. **Объекты Recordset** из таблиц авторов и titleauthor связаны с ИД автора.

2. Внешний цикл отображает имя и фамилию каждого автора, состояние и идентификацию.

3. Приложение **Recordset** для каждой строки извлекается из коллекции **Fields** и назначено *rstTitleAuthor.*

4. Внутренний цикл отображает четыре поля из каждой строки в приложении **Recordset.**

> [!NOTE] 
> Свойство [StayInSync](stayinsync-property-ado.md) настроено как FALSE для иллюстрации, поэтому в каждой итерации внешней петли можно увидеть явное изменение главы. Однако пример будет более эффективным, если назначение на шаге 3 перемещается перед первой строкой на шаге 2, так что назначение выполняется только один раз. Установите **свойство StayInSync** true, чтобы *rstTitleAuthor* неявно и автоматически менял соответствующую главу всякий раз, когда *rST* перемещается в новую строку.

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

