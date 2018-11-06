---
title: Метод Recordset2.Clone (DAO)
TOCTitle: Clone Method
ms:assetid: f0d32cb1-03f6-395d-2509-b2139a5fdc68
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836567(v=office.15)
ms:contentKeyID: 48548614
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 598944aadb344ab97d7561e7ef55a67041c4fbf1
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998752"
---
# <a name="recordset2clone-method-dao"></a>Метод Recordset2.Clone (DAO)

**Применимо к**: Access 2013, Office 2013

Создает объект повторяющихся **[записей](recordset-object-dao.md)** , на который ссылается на исходный объект **Recordset2** .

## <a name="syntax"></a>Синтаксис

*выражение* . Копия

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

## <a name="return-value"></a>Возвращаемое значение

Набор записей

## <a name="remarks"></a>Примечания

Используйте метод **клонированной** для создания нескольких дубликатов объектов **набора записей** . Каждый набор записей может иметь собственный текущей записи. С помощью **клонированной** сам по себе не изменяет данные в объектах или в их базовые структуры. При использовании метода **клонирования** могут совместно использовать закладки между двумя или более объектов **Recordset2** , так как их закладки являются взаимозаменяемыми.

Можно использовать метод **клонированной** , если необходимо использовать для выполнения операции наборов записей, требует нескольких записей текущей. Это быстрее и эффективнее, чем при открытии второго набора записей. При создании набора записей с помощью метода **клонированной** его изначально не имеет текущей записи. Чтобы сделать запись текущей, прежде чем использовать клонированной записей, необходимо задать свойство **[закладку](recordset2-bookmark-property-dao.md)** или используйте один из методов **[перемещения](recordset-movefirst-method-dao.md)** , один из методов **[поиска](recordset2-findfirst-method-dao.md)** , либо метод **[Seek](recordset2-seek-method-dao.md)** .

С помощью метода **[Close](connection-close-method-dao.md)** исходной или повторяющихся объекта не влияет на другой объект. К примеру на исходный набора записей с помощью **Закрыть** не закройте копия.

> [!NOTE]
> - Закрытие набора записей клонированной ожидающие транзакции будет отображено неявные операции **отката** .
> - При клонировании объекта **набора записей** в таблице типа в рабочей области Microsoft Access значение свойства **[Index](recordset2-index-property-dao.md)** не копируется в новую копию набора записей. Необходимо скопировать вручную значение свойства **Index** .

## <a name="example"></a>Пример

В этом примере используется метод **клонированной** для создания копии набора записей и затем позволяет пользователя положение указателя записи каждой копии независимо друг от друга.

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
