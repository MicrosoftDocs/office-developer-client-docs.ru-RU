---
title: Метод Recordset.CopyQueryDef (DAO)
TOCTitle: CopyQueryDef Method
ms:assetid: fee8c2fe-500e-dfb3-21ce-211e54ff334b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837296(v=office.15)
ms:contentKeyID: 48548950
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa6c5aab5f357eef8c62c63c6fca873e64031411
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300562"
---
# <a name="recordsetcopyquerydef-method-dao"></a><span data-ttu-id="6f422-102">Метод Recordset.CopyQueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="6f422-102">Recordset.CopyQueryDef method (DAO)</span></span>


<span data-ttu-id="6f422-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f422-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6f422-104">Возвращает объект **[QueryDef](querydef-object-dao.md)**, который является копией **QueryDef** и используется для создания объекта **[Recordset](recordset-object-dao.md)**, представленного заполнителем recordset (только для рабочие области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6f422-104">Returns a **[QueryDef](querydef-object-dao.md)** object that is a copy of the **QueryDef** used to create the **[Recordset](recordset-object-dao.md)** object represented by the recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="6f422-105">.</span><span class="sxs-lookup"><span data-stu-id="6f422-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="6f422-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f422-106">Syntax</span></span>

<span data-ttu-id="6f422-107">*Expression* . CopyQueryDef</span><span class="sxs-lookup"><span data-stu-id="6f422-107">*expression* .CopyQueryDef</span></span>

<span data-ttu-id="6f422-108">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6f422-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f422-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f422-109">Return value</span></span>

<span data-ttu-id="6f422-110">QueryDef</span><span class="sxs-lookup"><span data-stu-id="6f422-110">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="6f422-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="6f422-111">Remarks</span></span>

<span data-ttu-id="6f422-112">С помощью метода **CopyQueryDef** можно создать новый объект **QueryDef** , который является дубликатом объекта **QueryDef** , использованного для создания объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6f422-112">You can use the **CopyQueryDef** method to create a new **QueryDef** that is a duplicate of the **QueryDef** used to create the **Recordset**.</span></span>

<span data-ttu-id="6f422-113">Если объект **QueryDef** не использовался для создания этого объекта **Recordset**, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="6f422-113">If a **QueryDef** wasn't used to create this **Recordset**, an error occurs.</span></span> <span data-ttu-id="6f422-114">Прежде чем использовать метод **CopyQueryDef** , необходимо сначала открыть объект **Recordset** с помощью метода **OpenRecordset** .</span><span class="sxs-lookup"><span data-stu-id="6f422-114">You must first open a **Recordset** with the **OpenRecordset** method before using the **CopyQueryDef** method.</span></span>

<span data-ttu-id="6f422-115">Этот метод полезен при создании объекта **Recordset** из объекта **QueryDef**и передаче объекта **Recordset** в функцию, а функция должна повторно создать эквивалент SQL запроса, например, чтобы изменить его каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="6f422-115">This method is useful when you create a **Recordset** object from a **QueryDef**, and pass the **Recordset** to a function, and the function must re-create the SQL equivalent of the query, for example, to modify it in some way.</span></span>

## <a name="example"></a><span data-ttu-id="6f422-116">Пример</span><span class="sxs-lookup"><span data-stu-id="6f422-116">Example</span></span>

<span data-ttu-id="6f422-117">В этом примере используется метод **CopyQueryDef** для создания копии объекта **QueryDef** из существующего **набора записей** и изменения копии путем добавления предложения в свойство SQL.</span><span class="sxs-lookup"><span data-stu-id="6f422-117">This example uses the **CopyQueryDef** method to create a copy of a **QueryDef** from an existing **Recordset** and modifies the copy by adding a clause to the SQL property.</span></span> <span data-ttu-id="6f422-118">При создании постоянного объекта **QueryDef**в свойство SQL можно добавить пробелы, пробелы, точки с запятой или символы переноса строки; Эти дополнительные символы необходимо отключать до того, как все новые предложения можно присоединить к оператору SQL.</span><span class="sxs-lookup"><span data-stu-id="6f422-118">When you create a permanent **QueryDef**, spaces, semicolons, or linefeeds may be added to the SQL property; these extra characters must be stripped before any new clauses can be attached to the SQL statement.</span></span>

```vb
    Function CopyQueryNew(rstTemp As Recordset, _ 
     strAdd As String) As QueryDef 
     
     Dim strSQL As String 
     Dim strRightSQL As String 
     
     Set CopyQueryNew = rstTemp.CopyQueryDef 
     With CopyQueryNew 
     ' Strip extra characters. 
     strSQL = .SQL 
     strRightSQL = Right(strSQL, 1) 
     Do While strRightSQL = " " Or strRightSQL = ";" Or _ 
     strRightSQL = Chr(10) Or strRightSQL = vbCr 
     strSQL = Left(strSQL, Len(strSQL) - 1) 
     strRightSQL = Right(strSQL, 1) 
     Loop 
     .SQL = strSQL & strAdd 
     End With 
     
    End Function 
```

<br/>

<span data-ttu-id="6f422-119">В этом примере показано возможное использование Копикуеринев ().</span><span class="sxs-lookup"><span data-stu-id="6f422-119">This example shows a possible use of CopyQueryNew().</span></span>

```vb 
Sub CopyQueryDefX() 
 
 Dim dbsNorthwind As Database 
 Dim qdfEmployees As QueryDef 
 Dim rstEmployees As Recordset 
 Dim intCommand As Integer 
 Dim strOrderBy As String 
 Dim qdfCopy As QueryDef 
 Dim rstCopy As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfEmployees = dbsNorthwind.CreateQueryDef( _ 
 "NewQueryDef", "SELECT FirstName, LastName, " & _ 
 "BirthDate FROM Employees") 
 Set rstEmployees = qdfEmployees.OpenRecordset( _ 
 dbOpenForwardOnly) 
 
 Do While True 
 intCommand = Val(InputBox( _ 
 "Choose field on which to order a new " & _ 
 "Recordset:" & vbCr & "1 - FirstName" & vbCr & _ 
 "2 - LastName" & vbCr & "3 - BirthDate" & vbCr & _ 
 "[Cancel - exit]")) 
 Select Case intCommand 
 Case 1 
 strOrderBy = " ORDER BY FirstName" 
 Case 2 
 strOrderBy = " ORDER BY LastName" 
 Case 3 
 strOrderBy = " ORDER BY BirthDate" 
 Case Else 
 Exit Do 
 End Select 
 Set qdfCopy = CopyQueryNew(rstEmployees, strOrderBy) 
 Set rstCopy = qdfCopy.OpenRecordset(dbOpenSnapshot, _ 
 dbForwardOnly) 
 With rstCopy 
 Do While Not .EOF 
 Debug.Print !LastName & ", " & !FirstName & _ 
 " - " & !BirthDate 
 .MoveNext 
 Loop 
 .Close 
 End With 
 Exit Do 
 Loop 
 
 rstEmployees.Close 
 ' Delete new QueryDef because this is a demonstration. 
 dbsNorthwind.QueryDefs.Delete qdfEmployees.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

