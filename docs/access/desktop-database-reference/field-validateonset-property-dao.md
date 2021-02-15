---
title: Свойство Field.ValidateOnSet (DAO)
TOCTitle: ValidateOnSet Property
ms:assetid: 00245a8a-a78f-b0a8-3eb3-11dd27873984
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844720(v=office.15)
ms:contentKeyID: 48542898
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052929
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2d8fb358ab757d826bcfcd335aada8825e3ba980
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292960"
---
# <a name="fieldvalidateonset-property-dao"></a><span data-ttu-id="320a9-102">Свойство Field.ValidateOnSet (DAO)</span><span class="sxs-lookup"><span data-stu-id="320a9-102">Field.ValidateOnSet property (DAO)</span></span>


<span data-ttu-id="320a9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="320a9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="320a9-104">Задает или возвращает значение, которое указывает, проверяется ли значение объекта **[Field](field-object-dao.md)** немедленно, если задано свойство **[Value](field-value-property-dao.md)** объекта (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="320a9-104">Sets or returns a value that specifies whether or not the value of a **[Field](field-object-dao.md)** object is immediately validated when the object's **[Value](field-value-property-dao.md)** property is set (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="320a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="320a9-105">Syntax</span></span>

<span data-ttu-id="320a9-106">*выражение .* ValidateOnSet</span><span class="sxs-lookup"><span data-stu-id="320a9-106">*expression* .ValidateOnSet</span></span>

<span data-ttu-id="320a9-107">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="320a9-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="320a9-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="320a9-108">Remarks</span></span>

<span data-ttu-id="320a9-109">Только **объекты Field** в **[объектах Recordset](recordset-object-dao.md)** поддерживают свойство **ValidateOnSet** как чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="320a9-109">Only **Field** objects in **[Recordset](recordset-object-dao.md)** objects support the **ValidateOnSet** property as read/write.</span></span>

<span data-ttu-id="320a9-110">Установка для **свойства ValidateOnSet** свойства **True** может оказаться полезной в ситуации, когда пользователь вводит записи, включающие существенные memo-данные.</span><span class="sxs-lookup"><span data-stu-id="320a9-110">Setting the **ValidateOnSet** property to **True** can be useful in a situation when a user is entering records that include substantial Memo data.</span></span> <span data-ttu-id="320a9-111">Ожидание вызова **[Update](recordset-update-method-dao.md)** для проверки данных может привести к ненужному времени, затраченного на запись длительных данных memo в базу данных, если окажется, что данные все равно недействительны, так как правило проверки было нарушено в другом поле.</span><span class="sxs-lookup"><span data-stu-id="320a9-111">Waiting until the **[Update](recordset-update-method-dao.md)** call to validate the data can result in unnecessary time spent writing the lengthy Memo data to the database if it turns out that the data was invalid anyway because a validation rule was broken in another field.</span></span>

## <a name="example"></a><span data-ttu-id="320a9-112">Пример</span><span class="sxs-lookup"><span data-stu-id="320a9-112">Example</span></span>

<span data-ttu-id="320a9-113">В этом примере свойство **ValidateOnSet** используется для демонстрации того, как можно ловить ошибки во время ввода данных.</span><span class="sxs-lookup"><span data-stu-id="320a9-113">This example uses the **ValidateOnSet** property to demonstrate how one might trap for errors during data entry.</span></span> <span data-ttu-id="320a9-114">Для запуска этой процедуры требуется функция ValidateData.</span><span class="sxs-lookup"><span data-stu-id="320a9-114">The ValidateData function is required for this procedure to run.</span></span>

```vb
    Sub ValidateOnSetX() 
     
     Dim dbsNorthwind As Database 
     Dim fldDays As Field 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create and append a new Field object to the Fields 
     ' collection of the Employees table. 
     Set fldDays = _ 
     dbsNorthwind.TableDefs!Employees.CreateField( _ 
     "DaysOfVacation", dbInteger, 2) 
     fldDays.ValidationRule = "BETWEEN 1 AND 20" 
     fldDays.ValidationText = _ 
     "Number must be between 1 and 20!" 
     dbsNorthwind.TableDefs!Employees.Fields.Append fldDays 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     
     Do While True 
     ' Add new record. 
     .AddNew 
     
     ' Get user input for three fields. Verify that the 
     ' data do not violate the validation rules for any 
     ' of the fields. 
     If ValidateData(!FirstName, _ 
     "Enter first name.") = False Then Exit Do 
     If ValidateData(!LastName, _ 
     "Enter last name.") = False Then Exit Do 
     If ValidateData(!DaysOfVacation, _ 
     "Enter days of vacation.") = False Then Exit Do 
     
     .Update 
     .Bookmark = .LastModified 
     Debug.Print !FirstName & " " & !LastName & _ 
     " - " & "DaysOfVacation = " & !DaysOfVacation 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     Exit Do 
     Loop 
     
     ' Cancel AddNew method if any of the validation rules 
     ' were broken. 
     If .EditMode <> dbEditNone Then .CancelUpdate 
     .Close 
     End With 
     
     ' Delete new field because this is a demonstration. 
     dbsNorthwind.TableDefs!Employees.Fields.Delete _ 
     fldDays.Name 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function ValidateData(fldTemp As Field, _ 
     strMessage As String) As Boolean 
     
     Dim strInput As String 
     Dim errLoop As Error 
     
     ValidateData = True 
     ' ValidateOnSet is only read/write for Field objects in 
     ' Recordset objects. 
     fldTemp.ValidateOnSet = True 
     
     Do While True 
     strInput = InputBox(strMessage) 
     If strInput = "" Then Exit Do 
     ' Trap for errors when setting the Field value. 
     On Error GoTo Err_Data 
     If fldTemp.Type = dbInteger Then 
     fldTemp = Val(strInput) 
     Else 
     fldTemp = strInput 
     End If 
     On Error GoTo 0 
     If Not IsNull(fldTemp) Then Exit Do 
     Loop 
     
     If strInput = "" Then ValidateData = False 
     
     Exit Function 
     
    Err_Data: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. The description 
     ' property of the last Error object will be set to 
     ' the ValidationText property of the relevant 
     ' field. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Function
```
