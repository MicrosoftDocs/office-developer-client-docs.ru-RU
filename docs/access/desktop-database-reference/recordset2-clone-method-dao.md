---
title: Метод Recordset2. Clone (DAO)
TOCTitle: Clone Method
ms:assetid: f0d32cb1-03f6-395d-2509-b2139a5fdc68
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836567(v=office.15)
ms:contentKeyID: 48548614
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6780a27d573f5ff7ff41060074fb8abb9f8e2b80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307394"
---
# <a name="recordset2clone-method-dao"></a>Метод Recordset2. Clone (DAO)

**Область применения**: Access 2013, Office 2013

Создает дубликат объекта **[Recordset](recordset-object-dao.md)** , ссылающегося на исходный объект **Recordset2** .

## <a name="syntax"></a>Синтаксис

*expression* .Clone

*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .

## <a name="return-value"></a>Возвращаемое значение

Recordset

## <a name="remarks"></a>Примечания

Метод **Clone** используется для создания нескольких дублированных объектов **Recordset**. Каждый набор записей может иметь собственную текущую запись. Сам по себе метод **Clone** не меняет данные в объектах и их базовых структурах. При использовании метода **clone** можно предоставить общий доступ к закладкам между двумя или более объектами **Recordset2** , так как их закладки являются взаимозаменяемыми.

Метод **clone** можно использовать, если требуется выполнить операцию с набором записей, для которого требуется несколько текущих записей. Это быстрее и эффективнее, чем открыть второй набор записей. Когда вы создаете объект Recordset с помощью метода **clone** , он изначально не имеет текущей записи. Чтобы сделать запись текущей, прежде чем использовать клон набора записей, необходимо задать свойство **[Bookmark](recordset2-bookmark-property-dao.md)** или использовать один **[из методов](recordset-movefirst-method-dao.md)** Find, один из методов **[Find](recordset2-findfirst-method-dao.md)** или метод **[Seek](recordset2-seek-method-dao.md)** .

Использование метода **[Close](connection-close-method-dao.md)** для исходного или дублированного объекта не влияет на другой объект. Например, использование **Close** для исходного объекта Recordset не приводит к закрытию клона.

> [!NOTE]
> - Закрытие клонированного набора записей в транзакции, ожидающей обработки, приведет к выполнению неявной операции **Rollback**.
> - При клонировании объекта **Recordset** табличного типа в рабочей области Microsoft Access значение свойства **[Index](recordset2-index-property-dao.md)** не клонируется в новую копию набора записей. Значение свойства **Index** следует копировать вручную.

## <a name="example"></a>Пример

В этом примере используется метод **clone** для создания копий объекта Recordset, а затем пользователю разрешается располагать указатель записи каждой копии независимо друг от друга.

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset2 
       Dim intLoop As Integer 
       Dim strMessage As String 
       Dim strFind As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' If the following SQL statement will be used often,  
       ' creating a permanent QueryDef will result in better 
       ' performance. 
       Set arstProducts(1) = dbsNorthwind.OpenRecordset( _ 
          "SELECT ProductName FROM Products " & _ 
          "ORDER BY ProductName", dbOpenSnapshot) 
     
       ' Create two clones of the original Recordset. 
       Set arstProducts(2) = arstProducts(1).Clone 
       Set arstProducts(3) = arstProducts(1).Clone 
     
       Do While True 
     
          ' Loop through the array so that on each pass, the  
          ' user is searching a different copy of the same  
          ' Recordset. 
          For intLoop = 1 To 3 
     
             ' Ask for search string while showing where the 
             ' current record pointer is for each Recordset. 
             strMessage = _ 
                "Recordsets from Products table:" & vbCr & _ 
                "  1 - Original - Record pointer at " & _ 
                arstProducts(1)!ProductName & vbCr & _ 
                "  2 - Clone - Record pointer at " & _ 
                arstProducts(2)!ProductName & vbCr & _ 
                "  3 - Clone - Record pointer at " & _ 
                arstProducts(3)!ProductName & vbCr & _ 
                "Enter search string for #" & intLoop & ":" 
             strFind = Trim(InputBox(strMessage)) 
             If strFind = "" Then Exit Do 
     
             ' Find the search string; if there's no match, jump 
             ' to the last record. 
             With arstProducts(intLoop) 
                .FindFirst "ProductName >= '" & strFind & "'" 
                If .NoMatch Then .MoveLast 
             End With 
     
          Next intLoop 
     
       Loop 
     
       arstProducts(1).Close 
       arstProducts(2).Close 
       arstProducts(3).Close 
       dbsNorthwind.Close 
     
    End Sub
```
