---
title: Свойство field2. Валидатеонсет (DAO)
TOCTitle: ValidateOnSet Property
ms:assetid: 07612730-8dad-4ef0-b19b-f76845973fc3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844969(v=office.15)
ms:contentKeyID: 48543075
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 427903186cce0f2ce3adf7690682a793fb417873
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292645"
---
# <a name="field2validateonset-property-dao"></a><span data-ttu-id="5d64a-102">Свойство field2. Валидатеонсет (DAO)</span><span class="sxs-lookup"><span data-stu-id="5d64a-102">Field2.ValidateOnSet property (DAO)</span></span>


<span data-ttu-id="5d64a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d64a-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="5d64a-104">Задает или возвращает значение, указывающее, является ли значение объекта **field2** немедленно проверенным, когда задано свойство **value** объекта (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5d64a-104">Sets or returns a value that specifies whether or not the value of a **Field2** object is immediately validated when the object's **Value** property is set (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d64a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d64a-105">Syntax</span></span>

<span data-ttu-id="5d64a-106">*Expression* . валидатеонсет</span><span class="sxs-lookup"><span data-stu-id="5d64a-106">*expression* .ValidateOnSet</span></span>

<span data-ttu-id="5d64a-107">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="5d64a-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d64a-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="5d64a-108">Remarks</span></span>

<span data-ttu-id="5d64a-109">Только объекты **field2** в объектах **Recordset** поддерживают свойство **валидатеонсет** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5d64a-109">Only **Field2** objects in **Recordset** objects support the **ValidateOnSet** property as read/write.</span></span>

<span data-ttu-id="5d64a-110">Установка свойства **валидатеонсет** в **значение true** может быть полезна в ситуации, когда пользователь вводит записи, содержащие существенные данные о заметках.</span><span class="sxs-lookup"><span data-stu-id="5d64a-110">Setting the **ValidateOnSet** property to **True** can be useful in a situation when a user is entering records that include substantial Memo data.</span></span> <span data-ttu-id="5d64a-111">Ожидание, пока вызов **Update** для проверки данных может повлечь за собой ненужное время на запись длинных данных MEMO в базу данных, если оказалось, что данные недопустимы, так как правило проверки было разорвано в другом поле.</span><span class="sxs-lookup"><span data-stu-id="5d64a-111">Waiting until the **Update** call to validate the data can result in unnecessary time spent writing the lengthy Memo data to the database if it turns out that the data was invalid anyway because a validation rule was broken in another field.</span></span>

## <a name="example"></a><span data-ttu-id="5d64a-112">Пример</span><span class="sxs-lookup"><span data-stu-id="5d64a-112">Example</span></span>

<span data-ttu-id="5d64a-113">В этом примере используется свойство **валидатеонсет** , чтобы продемонстрировать, как может осуществляться треппинг для ошибок при вводе данных.</span><span class="sxs-lookup"><span data-stu-id="5d64a-113">This example uses the **ValidateOnSet** property to demonstrate how one might trap for errors during data entry.</span></span> <span data-ttu-id="5d64a-114">Для выполнения этой процедуры требуется функция Валидатедата.</span><span class="sxs-lookup"><span data-stu-id="5d64a-114">The ValidateData function is required for this procedure to run.</span></span>

```vb
    Sub ValidateOnSetX() 
     
     Dim dbsNorthwind As Database 
     Dim fldDays As Field2 
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
     
    Function ValidateData(fldTemp As Field2, _ 
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
