---
title: Свойство Recordset2. не ПОИСКПОЗ (DAO)
TOCTitle: NoMatch Property
ms:assetid: 2d7a02ff-a2bf-5f0e-bd71-a6d42c25b13a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192114(v=office.15)
ms:contentKeyID: 48543972
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c3168dcce9fb13d057380e7a1a4ef89f8814e02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309396"
---
# <a name="recordset2nomatch-property-dao"></a><span data-ttu-id="9f72b-102">Свойство Recordset2. не ПОИСКПОЗ (DAO)</span><span class="sxs-lookup"><span data-stu-id="9f72b-102">Recordset2.NoMatch property (DAO)</span></span>

<span data-ttu-id="9f72b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f72b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9f72b-104">Указывает, была ли найдена конкретная запись с помощью метода **[Seek](recordset2-seek-method-dao.md)** или одного из методов **[Find](recordset2-findfirst-method-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9f72b-104">Indicates whether a particular record was found by using the **[Seek](recordset2-seek-method-dao.md)** method or one of the **[Find](recordset2-findfirst-method-dao.md)** methods (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f72b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f72b-105">Syntax</span></span>

<span data-ttu-id="9f72b-106">*expression* .NoMatch</span><span class="sxs-lookup"><span data-stu-id="9f72b-106">*expression* .NoMatch</span></span>

<span data-ttu-id="9f72b-107">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="9f72b-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f72b-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f72b-108">Remarks</span></span>

<span data-ttu-id="9f72b-109">При открытии или создании объекта **[Recordset](recordset-object-dao.md)**, его свойство **NoMatch** имеет значение **False**.</span><span class="sxs-lookup"><span data-stu-id="9f72b-109">When you open or create a **[Recordset](recordset-object-dao.md)** object, its **NoMatch** property is set to **False**.</span></span>

<span data-ttu-id="9f72b-110">Чтобы найти запись воспользуйтесь методом **Seek** для объекта **Recordset** табличного типа или одним из методов **Find** для объекта **Recordset** типа dynaset или мгновенный снимок.</span><span class="sxs-lookup"><span data-stu-id="9f72b-110">To locate a record, use the **Seek** method on a table-type **Recordset** object or one of the **Find** methods on a dynaset- or snapshot-type **Recordset** object.</span></span> <span data-ttu-id="9f72b-111">Проверьте настройки свойства **NoMatch**, чтобы узнать, была ли найдена запись.</span><span class="sxs-lookup"><span data-stu-id="9f72b-111">Check the **NoMatch** property setting to see whether the record was found.</span></span>

<span data-ttu-id="9f72b-112">Если использование метода **Seek** или **Find** не принесет результаты, а свойство **NoMatch** имеет значение **True**, текущая запись больше недействительна.</span><span class="sxs-lookup"><span data-stu-id="9f72b-112">If the **Seek** or **Find** method is unsuccessful and the **NoMatch** property is **True**, the current record will no longer be valid.</span></span> <span data-ttu-id="9f72b-113">Не забудьте получить закладки текущей записи, прежде чем использовать метод **Seek** или **Find**, если вам потребуется вернуться к этой записи.</span><span class="sxs-lookup"><span data-stu-id="9f72b-113">Be sure to obtain the current record's bookmark before using the **Seek** method or a **Find** method if you'll need to return to that record.</span></span>

> [!NOTE]
> <span data-ttu-id="9f72b-114">Использование методов **[Move](recordset-movefirst-method-dao.md)** для объекта **Recordset** не оказывает влияние на настройку свойства **NoMatch**.</span><span class="sxs-lookup"><span data-stu-id="9f72b-114">Using any of the **[Move](recordset-movefirst-method-dao.md)** methods on a **Recordset** object won't affect its **NoMatch** property setting.</span></span>

## <a name="example"></a><span data-ttu-id="9f72b-115">Пример</span><span class="sxs-lookup"><span data-stu-id="9f72b-115">Example</span></span>

<span data-ttu-id="9f72b-116">В этом примере используется свойство **NoMatch** для определения того, принесли ли результат методы **Seek** и **FindFirst**, и если нет, обеспечение соответствующей реакции.</span><span class="sxs-lookup"><span data-stu-id="9f72b-116">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback.</span></span> <span data-ttu-id="9f72b-117">Процедуры SeekMatch и FindMatch являются обязательными для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="9f72b-117">The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

```vb
    Sub NoMatchX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim rstCustomers As Recordset2 
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
     
    Sub SeekMatch(rstTemp As Recordset2, _ 
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
