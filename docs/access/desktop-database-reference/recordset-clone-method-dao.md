---
title: Метод Recordset.Clone (DAO)
TOCTitle: Clone Method
ms:assetid: 50cbc011-7e72-4dee-488d-96e681618e8e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193824(v=office.15)
ms:contentKeyID: 48544802
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052909
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: ecc5592893c1caee16f0a00687ce50f68b05e9c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300660"
---
# <a name="recordsetclone-method-dao"></a>Метод Recordset.Clone (DAO)

**Область применения**: Access 2013, Office 2013

Создает дубликат объекта **[Recordset](recordset-object-dao.md)**, который ссылается на исходный объект **Recordset**.

## <a name="syntax"></a>Синтаксис

*expression* .Clone

*expression*: переменная, представляющая объект **Recordset**.

## <a name="return-value"></a>Возвращаемое значение

Recordset

## <a name="remarks"></a>Примечания

Метод **Clone** используется для создания нескольких дублированных объектов **Recordset**. У каждого объекта **Recordset** есть собственная текущая запись. Сам по себе метод **Clone** не меняет данные в объектах и их базовых структурах. Благодаря методу **Clone** вы можете использовать одни и те же закладки в нескольких объектах **Recordset**, так как их закладки взаимозаменяемы.

Вы можете использовать метод **Clone**, если с объектом **Recordset** нужно выполнить операцию, требующую нескольких текущих записей. Это быстрее и эффективнее, чем открытие второго объекта **Recordset**. При создании объекта **Recordset** с помощью метода **Clone** изначально отсутствует текущая запись. Чтобы сделать запись текущей перед использованием клона объекта **Recordset**, необходимо задать свойство **[Bookmark](recordset-bookmark-property-dao.md)** или использовать один из методов **[Move](recordset-movefirst-method-dao.md)**, один из методов **[Find](recordset-findfirst-method-dao.md)** или метод **[Seek](recordset-seek-method-dao.md)**.

Использование метода **[Close](connection-close-method-dao.md)** для исходного или дублированного объекта не влияет на другой объект. Например, при использовании метода **Close** для исходного объекта **Recordset** клон не закрывается.

> [!NOTE]
> - Закрытие клонированного набора записей в транзакции, ожидающей обработки, приведет к выполнению неявной операции **Rollback**.
> - При клонировании объекта **Recordset** табличного типа в рабочей области Microsoft Access значение свойства **[Index](recordset2-index-property-dao.md)** не клонируется в новую копию набора записей. Значение свойства **Index** следует копировать вручную.

## <a name="example"></a>Пример

В этом примере используется метод **Clone**, чтобы создать копии объекта **Recordset**, после чего пользователь может разместить указатели записей для каждой копии независимо друг от друга.

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset 
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
