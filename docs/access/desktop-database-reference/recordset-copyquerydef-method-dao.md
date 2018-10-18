---
title: Recordset.CopyQueryDef Method (DAO)
TOCTitle: CopyQueryDef Method
ms:assetid: fee8c2fe-500e-dfb3-21ce-211e54ff334b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837296(v=office.15)
ms:contentKeyID: 48548950
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f8c9342a58e70587e60236d8cb5410d9eb2709f0
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606173"
---
# <a name="recordsetcopyquerydef-method-dao"></a><span data-ttu-id="5ca1e-102">Recordset.CopyQueryDef Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="5ca1e-102">Recordset.CopyQueryDef Method (DAO)</span></span>


<span data-ttu-id="5ca1e-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ca1e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5ca1e-104">Возвращает объект **[QueryDef](querydef-object-dao.md)** , являющееся копией **QueryDef** , используемый для создания объекта **[набора записей](recordset-object-dao.md)** , представленного заполнитель набора записей (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5ca1e-104">Returns a **[QueryDef](querydef-object-dao.md)** object that is a copy of the **QueryDef** used to create the **[Recordset](recordset-object-dao.md)** object represented by the recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="5ca1e-105">.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="5ca1e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ca1e-106">Syntax</span></span>

<span data-ttu-id="5ca1e-107">*выражение* . CopyQueryDef</span><span class="sxs-lookup"><span data-stu-id="5ca1e-107">*expression* .CopyQueryDef</span></span>

<span data-ttu-id="5ca1e-108">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5ca1e-108">*expression* A variable that represents a **Recordset** object.</span></span>

<span data-ttu-id="5ca1e-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="5ca1e-109"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="5ca1e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ca1e-110">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="5ca1e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ca1e-111">Return value</span></span>
>>>>>>> <span data-ttu-id="5ca1e-112">master</span><span class="sxs-lookup"><span data-stu-id="5ca1e-112">master</span></span>

<span data-ttu-id="5ca1e-113">QueryDef</span><span class="sxs-lookup"><span data-stu-id="5ca1e-113">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="5ca1e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="5ca1e-114">Remarks</span></span>

<span data-ttu-id="5ca1e-115">Метод **CopyQueryDef** можно использовать для создания нового **QueryDef** , дублирующих **QueryDef** , используемые для создания **записей**.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-115">You can use the **CopyQueryDef** method to create a new **QueryDef** that is a duplicate of the **QueryDef** used to create the **Recordset**.</span></span>

<span data-ttu-id="5ca1e-116">Если **QueryDef** не был создан этот **набор записей**, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-116">If a **QueryDef** wasn't used to create this **Recordset**, an error occurs.</span></span> <span data-ttu-id="5ca1e-117">Сначала необходимо открыть **набора записей** с помощью метода **OpenRecordset** перед использованием метода **CopyQueryDef** .</span><span class="sxs-lookup"><span data-stu-id="5ca1e-117">You must first open a **Recordset** with the **OpenRecordset** method before using the **CopyQueryDef** method.</span></span>

<span data-ttu-id="5ca1e-118">Этот метод полезен, когда создание объекта **набора записей** из **QueryDef**и передать **набора записей** функции и функции необходимо повторно создать эквивалент SQL запроса, например, чтобы изменить каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-118">This method is useful when you create a **Recordset** object from a **QueryDef**, and pass the **Recordset** to a function, and the function must re-create the SQL equivalent of the query, for example, to modify it in some way.</span></span>

## <a name="example"></a><span data-ttu-id="5ca1e-119">Пример</span><span class="sxs-lookup"><span data-stu-id="5ca1e-119">Example</span></span>

<span data-ttu-id="5ca1e-120">В этом примере используется метод **CopyQueryDef** для создания копии **QueryDef** из существующих **записей** и изменяет эту копию, добавив предложение свойство SQL.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-120">This example uses the **CopyQueryDef** method to create a copy of a **QueryDef** from an existing **Recordset** and modifies the copy by adding a clause to the SQL property.</span></span> <span data-ttu-id="5ca1e-121">При создании постоянной **QueryDef**пробелы, точки с запятой или каретки могут быть добавлены к свойству SQL; необходимо очищено от вложения эти дополнительные символы, прежде чем любые новые предложения можно присоединить к инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="5ca1e-121">When you create a permanent **QueryDef**, spaces, semicolons, or linefeeds may be added to the SQL property; these extra characters must be stripped before any new clauses can be attached to the SQL statement.</span></span>

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

<span data-ttu-id="5ca1e-122">В этом примере показано возможное использование CopyQueryNew().</span><span class="sxs-lookup"><span data-stu-id="5ca1e-122">This example shows a possible use of CopyQueryNew().</span></span>

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

