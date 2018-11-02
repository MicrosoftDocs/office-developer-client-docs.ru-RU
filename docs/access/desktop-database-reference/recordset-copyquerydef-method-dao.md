---
title: Метод Recordset.CopyQueryDef (DAO)
TOCTitle: CopyQueryDef Method
ms:assetid: fee8c2fe-500e-dfb3-21ce-211e54ff334b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837296(v=office.15)
ms:contentKeyID: 48548950
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 45856ba6563924d0a918cf89dd95a86287d68acf
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921777"
---
# <a name="recordsetcopyquerydef-method-dao"></a><span data-ttu-id="f1c2c-102">Метод Recordset.CopyQueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="f1c2c-102">Recordset.CopyQueryDef method (DAO)</span></span>


<span data-ttu-id="f1c2c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f1c2c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f1c2c-104">Возвращает объект **[QueryDef](querydef-object-dao.md)** , являющееся копией **QueryDef** , используемый для создания объекта **[набора записей](recordset-object-dao.md)** , представленного заполнитель набора записей (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f1c2c-104">Returns a **[QueryDef](querydef-object-dao.md)** object that is a copy of the **QueryDef** used to create the **[Recordset](recordset-object-dao.md)** object represented by the recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="f1c2c-105">.</span><span class="sxs-lookup"><span data-stu-id="f1c2c-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="f1c2c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1c2c-106">Syntax</span></span>

<span data-ttu-id="f1c2c-107">*выражение* . CopyQueryDef</span><span class="sxs-lookup"><span data-stu-id="f1c2c-107">*expression* .CopyQueryDef</span></span>

<span data-ttu-id="f1c2c-108">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="f1c2c-108">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="return-value"></a><span data-ttu-id="f1c2c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1c2c-109">Return value</span></span>

<span data-ttu-id="f1c2c-110">QueryDef</span><span class="sxs-lookup"><span data-stu-id="f1c2c-110">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="f1c2c-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="f1c2c-111">Remarks</span></span>

<span data-ttu-id="f1c2c-112">Метод **CopyQueryDef** можно использовать для создания нового **QueryDef** , дублирующих **QueryDef** , используемые для создания **записей**.</span><span class="sxs-lookup"><span data-stu-id="f1c2c-112">You can use the **CopyQueryDef** method to create a new **QueryDef** that is a duplicate of the **QueryDef** used to create the **Recordset**.</span></span>

<span data-ttu-id="f1c2c-113">Если **QueryDef** не был создан этот **набор записей**, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="f1c2c-113">If a **QueryDef** wasn't used to create this **Recordset**, an error occurs.</span></span> <span data-ttu-id="f1c2c-114">Сначала необходимо открыть **набора записей** с помощью метода **OpenRecordset** перед использованием метода **CopyQueryDef** .</span><span class="sxs-lookup"><span data-stu-id="f1c2c-114">You must first open a **Recordset** with the **OpenRecordset** method before using the **CopyQueryDef** method.</span></span>

<span data-ttu-id="f1c2c-115">Этот метод полезен, когда создание объекта **набора записей** из **QueryDef**и передать **набора записей** функции и функции необходимо повторно создать эквивалент SQL запроса, например, чтобы изменить каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="f1c2c-115">This method is useful when you create a **Recordset** object from a **QueryDef**, and pass the **Recordset** to a function, and the function must re-create the SQL equivalent of the query, for example, to modify it in some way.</span></span>

## <a name="example"></a><span data-ttu-id="f1c2c-116">Пример</span><span class="sxs-lookup"><span data-stu-id="f1c2c-116">Example</span></span>

<span data-ttu-id="f1c2c-117">В этом примере используется метод **CopyQueryDef** для создания копии **QueryDef** из существующих **записей** и изменяет эту копию, добавив предложение свойство SQL.</span><span class="sxs-lookup"><span data-stu-id="f1c2c-117">This example uses the **CopyQueryDef** method to create a copy of a **QueryDef** from an existing **Recordset** and modifies the copy by adding a clause to the SQL property.</span></span> <span data-ttu-id="f1c2c-118">При создании постоянной **QueryDef**пробелы, точки с запятой или каретки могут быть добавлены к свойству SQL; необходимо очищено от вложения эти дополнительные символы, прежде чем любые новые предложения можно присоединить к инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="f1c2c-118">When you create a permanent **QueryDef**, spaces, semicolons, or linefeeds may be added to the SQL property; these extra characters must be stripped before any new clauses can be attached to the SQL statement.</span></span>

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

<span data-ttu-id="f1c2c-119">В этом примере показано возможное использование CopyQueryNew().</span><span class="sxs-lookup"><span data-stu-id="f1c2c-119">This example shows a possible use of CopyQueryNew().</span></span>

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

