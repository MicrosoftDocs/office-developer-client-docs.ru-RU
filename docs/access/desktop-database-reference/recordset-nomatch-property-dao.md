---
title: Recordset.NoMatch Property (DAO)
TOCTitle: NoMatch Property
ms:assetid: 47d03575-f570-89b5-a20f-a3bd8b8b5c6d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193226(v=office.15)
ms:contentKeyID: 48544606
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052889
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ebb1178525d1efb663ce49f4e5493e828afbfc2e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874134"
---
# <a name="recordsetnomatch-property-dao"></a>Recordset.NoMatch Property (DAO)

**Применимо к**: Access 2013, Office 2013

Указывает, будет ли определенный запись найдена с помощью метода **[Seek](recordset-seek-method-dao.md)** или один из методов **[поиска](recordset-findfirst-method-dao.md)** (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . NoMatch

*выражение* Переменная, которая представляет собой объект **набора записей** .

## <a name="remarks"></a>Замечания

При открытии или создание объекта **[набора записей](recordset-object-dao.md)** , его свойство **NoMatch** имеет значение **False**.

Чтобы найти записи, используйте метод **Seek** на объект **набора записей** в таблице тип или один из методов **поиска** для объекта **набора записей** добавляющий или моментальный снимок. Проверьте значение свойства **NoMatch** , чтобы увидеть, является ли запись найдена.

Если **Seek** или **Найти** метод завершается неудачно, а свойство **NoMatch** имеет **значение True**, текущей записи будет становятся недопустимыми. Убедитесь, что для получения текущей записи закладку перед использованием **Seek** метод или метод **поиска** , если вам потребуется вернуться к этой записи.


> [!NOTE]
> Использовать любой из способов **[перемещать](recordset-movefirst-method-dao.md)** **целиком** не влияет на его значение свойства **NoMatch** .


## <a name="example"></a>Пример

В этом примере используется свойство **NoMatch** для определения ли **Seek** и **FindFirst** было выполнено успешно и если это не так, чтобы предоставить соответствующий отзыв. Процедуры SeekMatch и FindMatch необходимы для выполнения этой процедуры.

```vb
    Sub NoMatchX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim rstCustomers As Recordset 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim strCountry As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' Default is dbOpenTable; required if Index property will  
       ' be used. 
       Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
       With rstProducts 
          .Index = "PrimaryKey" 
     
          Do While True 
             ' Show current record information; ask user for  
             ' input. 
             strMessage = "NoMatch with Seek method" & vbCr & _ 
                "Product ID: " & !ProductID & vbCr & _ 
                "Product Name: " & !ProductName & vbCr & _ 
                "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
                "Enter a product ID." 
             strSeek = InputBox(strMessage) 
             If strSeek = "" Then Exit Do 
     
             ' Call procedure that seeks for a record based on  
             ' the ID number supplied by the user. 
             SeekMatch rstProducts, Val(strSeek) 
          Loop 
     
          .Close 
       End With 
     
       Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
          "SELECT CompanyName, Country FROM Customers " & _ 
          "ORDER BY CompanyName", dbOpenSnapshot) 
     
       With rstCustomers 
     
          Do While True 
             ' Show current record information; ask user for  
             ' input. 
             strMessage = "NoMatch with FindFirst method" & _ 
                vbCr & "Customer Name: " & !CompanyName & _ 
                vbCr & "Country: " & !Country & vbCr & _ 
                "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
                "Enter country on which to search." 
             strCountry = Trim(InputBox(strMessage)) 
             If strCountry = "" Then Exit Do 
     
             ' Call procedure that finds a record based on  
             ' the country name supplied by the user. 
             FindMatch rstCustomers, _ 
                "Country = '" & strCountry & "'" 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset, _ 
       intSeek As Integer) 
     
       Dim varBookmark As Variant 
       Dim strMessage As String 
     
       With rstTemp 
          ' Store current record location. 
          varBookmark = .Bookmark 
          .Seek "=", intSeek 
     
          ' If Seek method fails, notify user and return to the  
          ' last current record. 
          If .NoMatch Then 
             strMessage = _ 
                "Not found! Returning to current record." & _ 
                vbCr & vbCr & "NoMatch = " & .NoMatch 
             MsgBox strMessage 
             .Bookmark = varBookmark 
          End If 
     
       End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
       strFind As String) 
     
       Dim varBookmark As Variant 
       Dim strMessage As String 
     
       With rstTemp 
          ' Store current record location. 
          varBookmark = .Bookmark 
          .FindFirst strFind 
     
          ' If Find method fails, notify user and return to the  
          ' last current record. 
          If .NoMatch Then 
             strMessage = _ 
                "Not found! Returning to current record." & _ 
                vbCr & vbCr & "NoMatch = " & .NoMatch 
             MsgBox strMessage 
             .Bookmark = varBookmark 
          End If 
     
       End With 
     
    End Sub 
```

<br/>

Следующем примере показано, как использовать метод поиска для поиска записей в связанной таблице.

**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```
