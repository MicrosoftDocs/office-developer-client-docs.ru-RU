---
title: Recordset.Clone Method (DAO)
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
ms.openlocfilehash: 1c0b1ea2f0103d444a1429748b16c6a4314eb92c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876430"
---
# <a name="recordsetclone-method-dao"></a>Recordset.Clone Method (DAO)


**Применимо к**: Access 2013, Office 2013

Создает объект повторяющихся **[записей](recordset-object-dao.md)** , на который ссылается на исходный объект **набора записей** .

## <a name="syntax"></a>Синтаксис

*выражение* . Копия

*выражение* Переменная, которая представляет собой объект **набора записей** .

### <a name="return-value"></a>Возвращаемое значение

Набор записей

## <a name="remarks"></a>Замечания

Используйте метод **клонированной** для создания нескольких дубликатов объектов **набора записей** . Каждый **набор записей** может иметь собственный текущей записи. С помощью **клонированной** сам по себе не изменяет данные в объектах или в их базовые структуры. При использовании метода **клонирования** могут совместно использовать закладки между двумя или более объектов **наборов записей** , так как их закладки являются взаимозаменяемыми.

Можно использовать метод **клонированной** , если необходимо использовать для выполнения операции над требует нескольких записей текущего **набора записей** . Это быстрее и эффективнее, чем при открытии второго **набора записей**. При создании **набора записей** с помощью метода **клонированной** его изначально не имеет текущей записи. Чтобы сделать запись текущей, прежде чем использовать клонированной **записей** , необходимо задать свойство **[закладку](recordset-bookmark-property-dao.md)** или используйте один из методов **[перемещения](recordset-movefirst-method-dao.md)** , один из методов **[поиска](recordset-findfirst-method-dao.md)** , либо метод **[Seek](recordset-seek-method-dao.md)** .

С помощью метода **[Close](connection-close-method-dao.md)** исходной или повторяющихся объекта не влияет на другой объект. К примеру с помощью **Закрыть** на исходной **набора записей** не закройте копия.


> [!NOTE]
> <UL>
> <LI>
> <P>Закрытие набора записей клонированной ожидающие транзакции будет отображено неявные операции <STRONG>отката</STRONG> .</P>
> <LI>
> <P>При клонировании объекта <STRONG>набора записей</STRONG> в таблице типа в рабочей области Microsoft Access значение свойства <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG> не копируется в новую копию набора записей. Необходимо скопировать вручную значение свойства <STRONG>Index</STRONG> .</P></LI></UL>



## <a name="example"></a>Пример

В этом примере используется метод **клонированной** для создания копии **набора записей** и затем позволяет пользователя положение указателя записи каждой копии независимо друг от друга.

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
