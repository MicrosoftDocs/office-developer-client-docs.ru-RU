---
title: Свойство Field.AllowZeroLength (DAO)
TOCTitle: AllowZeroLength Property
ms:assetid: 5103a905-9258-e088-0210-857372f41c3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193832(v=office.15)
ms:contentKeyID: 48544807
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052962
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f1eb08c6079257a350a5bb92392871869e720f1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293163"
---
# <a name="fieldallowzerolength-property-dao"></a><span data-ttu-id="0a3db-102">Свойство Field.AllowZeroLength (DAO)</span><span class="sxs-lookup"><span data-stu-id="0a3db-102">Field.AllowZeroLength property (DAO)</span></span>

<span data-ttu-id="0a3db-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a3db-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0a3db-104">Задает или возвращает значение, которое указывает, является ли строка нулевой длины ("") допустимым параметром свойства **[Value](field-value-property-dao.md)** объекта **[Field](field-object-dao.md)** с типом данных Text или Memo (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0a3db-104">Sets or returns a value that indicates whether a zero-length string ("") is a valid setting for the **[Value](field-value-property-dao.md)** property of the **[Field](field-object-dao.md)** object with a Text or Memo data type (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="0a3db-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a3db-105">Syntax</span></span>

<span data-ttu-id="0a3db-106">*выражение .* AllowZeroLength</span><span class="sxs-lookup"><span data-stu-id="0a3db-106">*expression* .AllowZeroLength</span></span>

<span data-ttu-id="0a3db-107">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="0a3db-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a3db-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="0a3db-108">Remarks</span></span>

<span data-ttu-id="0a3db-109">Для объекта, еще не примежаемого к коллекции **Fields,** это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0a3db-109">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="0a3db-110">После этого доступность свойства **AllowZeroLength** зависит от объекта, который содержит коллекцию **Fields,** как показано в следующей таблице. </span><span class="sxs-lookup"><span data-stu-id="0a3db-110">Once appended to a **Fields** collection, the availability of the **AllowZeroLength** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0a3db-111">Если коллекция Fields принадлежит к</span><span class="sxs-lookup"><span data-stu-id="0a3db-111">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="0a3db-112">Then AllowZeroLength is</span><span class="sxs-lookup"><span data-stu-id="0a3db-112">Then AllowZeroLength is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a3db-113">Объект <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="0a3db-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0a3db-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0a3db-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3db-115">Объект <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="0a3db-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0a3db-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a3db-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3db-117">Объект <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="0a3db-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0a3db-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a3db-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a3db-119">Объект <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="0a3db-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0a3db-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0a3db-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a3db-121">Объект <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="0a3db-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0a3db-122">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0a3db-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0a3db-123">Это свойство можно использовать вместе со свойством **[Required,](field-required-property-dao.md)** **[ValidateOnSet](field-validateonset-property-dao.md)** или **[ValidationRule](field-validationrule-property-dao.md)** для проверки значения в поле.</span><span class="sxs-lookup"><span data-stu-id="0a3db-123">You can use this property along with the **[Required](field-required-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)**, or **[ValidationRule](field-validationrule-property-dao.md)** property to validate a value in a field.</span></span>

## <a name="example"></a><span data-ttu-id="0a3db-124">Пример</span><span class="sxs-lookup"><span data-stu-id="0a3db-124">Example</span></span>

<span data-ttu-id="0a3db-125">В этом примере свойство **AllowZeroLength** позволяет пользователю установить  для поля пустую строку.</span><span class="sxs-lookup"><span data-stu-id="0a3db-125">In this example, the **AllowZeroLength** property allows the user to set the value of a **Field** to an empty string.</span></span> <span data-ttu-id="0a3db-126">В этой ситуации пользователь может различать запись, данные которой неизвестны, и запись, в которой эти данные не применяются.</span><span class="sxs-lookup"><span data-stu-id="0a3db-126">In this situation, the user can distinguish between a record where data is not known and a record where the data does not apply.</span></span>

```vb
    Sub AllowZeroLengthX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldTemp As Field 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim strInput As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     ' Create a new Field object and append it to the Fields 
     ' collection of the Employees table. 
     Set fldTemp = tdfEmployees.CreateField("FaxPhone", _ 
     dbText, 24) 
     fldTemp.AllowZeroLength = True 
     tdfEmployees.Fields.Append fldTemp 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Get user input. 
     .Edit 
     strMessage = "Enter fax number for " & _ 
     !FirstName & " " & !LastName & "." & vbCr & _ 
     "[? - unknown, X - has no fax]" 
     strInput = UCase(InputBox(strMessage)) 
     If strInput <> "" Then 
     Select Case strInput 
     Case "?" 
     !FaxPhone = Null 
     Case "X" 
     !FaxPhone = "" 
     Case Else 
     !FaxPhone = strInput 
     End Select 
     
     .Update 
     
     ' Print report. 
     Debug.Print "Name - Fax number" 
     Debug.Print !FirstName & " " & !LastName & " - "; 
     
     If IsNull(!FaxPhone) Then 
     Debug.Print "[Unknown]" 
     Else 
     If !FaxPhone = "" Then 
     Debug.Print "[Has no fax]" 
     Else 
     Debug.Print !FaxPhone 
     End If 
     End If 
     
     Else 
     .CancelUpdate 
     End If 
     
     .Close 
     End With 
     
     ' Delete new field because this is a demonstration. 
     tdfEmployees.Fields.Delete fldTemp.Name 
     dbsNorthwind.Close 
     
    End Sub
```
