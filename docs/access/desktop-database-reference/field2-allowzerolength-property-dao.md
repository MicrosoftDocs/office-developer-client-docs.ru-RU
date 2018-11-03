---
title: Свойство Field2.AllowZeroLength (DAO)
TOCTitle: AllowZeroLength Property
ms:assetid: d3795634-527f-b4c5-b606-50f9945cac12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834791(v=office.15)
ms:contentKeyID: 48547908
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 853b2ca82703174ab1d62007dd92b8268ea13e54
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923051"
---
# <a name="field2allowzerolength-property-dao"></a><span data-ttu-id="787c3-102">Свойство Field2.AllowZeroLength (DAO)</span><span class="sxs-lookup"><span data-stu-id="787c3-102">Field2.AllowZeroLength property (DAO)</span></span>


<span data-ttu-id="787c3-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="787c3-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="787c3-104">Задает или возвращает значение, указывающее, является ли строка нулевой длины ("») — это недопустимое значение для свойства **[Value](field-value-property-dao.md)** объекта **поле2** с типом данных Text или Memo (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="787c3-104">Sets or returns a value that indicates whether a zero-length string ("") is a valid setting for the **[Value](field-value-property-dao.md)** property of the **Field2** object with a Text or Memo data type (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="787c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="787c3-105">Syntax</span></span>

<span data-ttu-id="787c3-106">*выражение* . Пустые строки</span><span class="sxs-lookup"><span data-stu-id="787c3-106">*expression* .AllowZeroLength</span></span>

<span data-ttu-id="787c3-107">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="787c3-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="787c3-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="787c3-108">Remarks</span></span>

<span data-ttu-id="787c3-109">Для объекта еще не добавляется в конец коллекции **полей** это свойство соответствует чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="787c3-109">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="787c3-110">Когда добавляется в конец коллекции **полей** , доступность свойства **пустые строки** зависит от объекта, который содержит коллекцию **полей** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="787c3-110">Once appended to a **Fields** collection, the availability of the **AllowZeroLength** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="787c3-111">Если принадлежит коллекции полей</span><span class="sxs-lookup"><span data-stu-id="787c3-111">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="787c3-112">Затем — пустые строки</span><span class="sxs-lookup"><span data-stu-id="787c3-112">Then AllowZeroLength is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="787c3-113">Объект <strong>индекса</strong></span><span class="sxs-lookup"><span data-stu-id="787c3-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="787c3-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="787c3-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="787c3-115">Объект <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="787c3-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="787c3-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="787c3-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="787c3-117">Объект <strong>набора записей</strong></span><span class="sxs-lookup"><span data-stu-id="787c3-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="787c3-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="787c3-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="787c3-119"><strong>Отношения</strong> объектов</span><span class="sxs-lookup"><span data-stu-id="787c3-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="787c3-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="787c3-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="787c3-121">Объект <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="787c3-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="787c3-122">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="787c3-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="787c3-123">Это свойство, а также **[требуется](field-required-property-dao.md)** **[Проверка набора](field-validateonset-property-dao.md)** и **[значение](field-validationrule-property-dao.md)** свойства можно использовать для проверки значения в поле.</span><span class="sxs-lookup"><span data-stu-id="787c3-123">You can use this property along with the **[Required](field-required-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)**, or **[ValidationRule](field-validationrule-property-dao.md)** property to validate a value in a field.</span></span>

## <a name="example"></a><span data-ttu-id="787c3-124">Пример</span><span class="sxs-lookup"><span data-stu-id="787c3-124">Example</span></span>

<span data-ttu-id="787c3-125">В следующем примере свойство **пустые строки** пользователь может задать значение **поле2** пустую строку.</span><span class="sxs-lookup"><span data-stu-id="787c3-125">In this example, the **AllowZeroLength** property allows the user to set the value of a **Field2** to an empty string.</span></span> <span data-ttu-id="787c3-126">В этом случае пользователь может различать записи, где неизвестно данных и запись, где данные не применяется.</span><span class="sxs-lookup"><span data-stu-id="787c3-126">In this situation, the user can distinguish between a record where data is not known and a record where the data does not apply.</span></span>

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
