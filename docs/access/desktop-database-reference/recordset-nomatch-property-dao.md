---
title: Свойство Recordset.NoMatch (DAO)
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
ms.openlocfilehash: 605c18b5390d60f8a92a4380cb9a11a269e0a39d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929701"
---
# <a name="recordsetnomatch-property-dao"></a><span data-ttu-id="887c9-102">Свойство Recordset.NoMatch (DAO)</span><span class="sxs-lookup"><span data-stu-id="887c9-102">Recordset.NoMatch property (DAO)</span></span>

<span data-ttu-id="887c9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="887c9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="887c9-104">Указывает, будет ли определенный запись найдена с помощью метода **[Seek](recordset-seek-method-dao.md)** или один из методов **[поиска](recordset-findfirst-method-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="887c9-104">Indicates whether a particular record was found by using the **[Seek](recordset-seek-method-dao.md)** method or one of the **[Find](recordset-findfirst-method-dao.md)** methods (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="887c9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="887c9-105">Syntax</span></span>

<span data-ttu-id="887c9-106">*выражение* . NoMatch</span><span class="sxs-lookup"><span data-stu-id="887c9-106">*expression* .NoMatch</span></span>

<span data-ttu-id="887c9-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="887c9-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="887c9-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="887c9-108">Remarks</span></span>

<span data-ttu-id="887c9-109">При открытии или создание объекта **[набора записей](recordset-object-dao.md)** , его свойство **NoMatch** имеет значение **False**.</span><span class="sxs-lookup"><span data-stu-id="887c9-109">When you open or create a **[Recordset](recordset-object-dao.md)** object, its **NoMatch** property is set to **False**.</span></span>

<span data-ttu-id="887c9-110">Чтобы найти записи, используйте метод **Seek** на объект **набора записей** в таблице тип или один из методов **поиска** для объекта **набора записей** добавляющий или моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="887c9-110">To locate a record, use the **Seek** method on a table-type **Recordset** object or one of the **Find** methods on a dynaset- or snapshot-type **Recordset** object.</span></span> <span data-ttu-id="887c9-111">Проверьте значение свойства **NoMatch** , чтобы увидеть, является ли запись найдена.</span><span class="sxs-lookup"><span data-stu-id="887c9-111">Check the **NoMatch** property setting to see whether the record was found.</span></span>

<span data-ttu-id="887c9-112">Если **Seek** или **Найти** метод завершается неудачно, а свойство **NoMatch** имеет **значение True**, текущей записи будет становятся недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="887c9-112">If the **Seek** or **Find** method is unsuccessful and the **NoMatch** property is **True**, the current record will no longer be valid.</span></span> <span data-ttu-id="887c9-113">Убедитесь, что для получения текущей записи закладку перед использованием **Seek** метод или метод **поиска** , если вам потребуется вернуться к этой записи.</span><span class="sxs-lookup"><span data-stu-id="887c9-113">Be sure to obtain the current record's bookmark before using the **Seek** method or a **Find** method if you'll need to return to that record.</span></span>


> [!NOTE]
> <span data-ttu-id="887c9-114">Использовать любой из способов **[перемещать](recordset-movefirst-method-dao.md)** **целиком** не влияет на его значение свойства **NoMatch** .</span><span class="sxs-lookup"><span data-stu-id="887c9-114">Using any of the **[Move](recordset-movefirst-method-dao.md)** methods on a **Recordset** object won't affect its **NoMatch** property setting.</span></span>


## <a name="example"></a><span data-ttu-id="887c9-115">Пример</span><span class="sxs-lookup"><span data-stu-id="887c9-115">Example</span></span>

<span data-ttu-id="887c9-116">В этом примере используется свойство **NoMatch** для определения ли **Seek** и **FindFirst** было выполнено успешно и если это не так, чтобы предоставить соответствующий отзыв.</span><span class="sxs-lookup"><span data-stu-id="887c9-116">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback.</span></span> <span data-ttu-id="887c9-117">Процедуры SeekMatch и FindMatch необходимы для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="887c9-117">The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

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

<span data-ttu-id="887c9-118">Следующем примере показано, как использовать метод поиска для поиска записей в связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="887c9-118">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="887c9-119">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="887c9-119">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
