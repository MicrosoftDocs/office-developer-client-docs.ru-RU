---
title: Field.ValidateOnSet Property (DAO)
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
ms.openlocfilehash: 9a7f89277b51ef0edb5603c4482d4547201673fb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884777"
---
# <a name="fieldvalidateonset-property-dao"></a>Field.ValidateOnSet Property (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает значение, указывает ли значение **[поля](field-object-dao.md)** объекта сразу же проверке, если свойство **[Value](field-value-property-dao.md)** объекта установлено (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . Проверка набора

*выражение* Переменная, которая представляет собой объект- **поля** .

## <a name="remarks"></a>Замечания

Только **поля** объектов в объекты **[набора записей](recordset-object-dao.md)** поддерживает **Проверка набора** свойств для чтения и записи.

**Проверка набора** для свойства значение **True,** можно использовать в ситуации, когда пользователь вводит записей, включая значительно сократить объем данных заметка. Ждать, пока **[обновление](recordset-update-method-dao.md)** звонок, чтобы проверить данные, может привести к ненужных времени, затраченного записи длительных данных Memo в базу данных при оказывается, данные недопустимо все равно так, как было нарушено правило проверки в другом поле.

## <a name="example"></a>Пример

В этом примере используется свойство **Проверка набора** для демонстрации как одно может блокирование ошибок во время ввода данных. Функция ValidateData является обязательным для выполнения этой процедуры.

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
