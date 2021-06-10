---
title: Свойство Recordset.EditMode (DAO)
TOCTitle: EditMode Property
ms:assetid: 3cf67f64-c8c3-ad0a-ce00-6f37a3c264ee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192697(v=office.15)
ms:contentKeyID: 48544329
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 326f23f95f9ccf8763f76b21df8955c39198a88c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307653"
---
# <a name="recordseteditmode-property-dao"></a>Свойство Recordset.EditMode (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает состояние редактирования для текущей записи.

## <a name="syntax"></a>Синтаксис

*выражения* . EditMode

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

Возвращается значение **Long,** которое указывает состояние редактирования. Это значение может быть одним из **[констант EditModeEnum.](editmodeenum-enumeration-dao.md)**

Свойство **EditMode полезно,** если процесс редактирования прерывается, например, ошибкой во время проверки. Значение свойства **EditMode** можно использовать для определения того, следует ли использовать метод **[Update](recordset-update-method-dao.md)** или **[CancelUpdate.](recordset-cancelupdate-method-dao.md)**

Вы также можете проверить, является ли параметр  **[Свойства LockEdits](recordset-lockedits-property-dao.md)** true, а параметр **свойства EditMode** **— dbEditInProgress,** чтобы определить, заблокирована ли текущая страница.

## <a name="example"></a>Пример

В этом примере показано значение **свойства EditMode** в различных условиях. Для запуска этой процедуры требуется функция EditModeOutput.

```vb
    Sub EditModeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     ' Show the EditMode property under different editing 
     ' states. 
     With rstEmployees 
     EditModeOutput "Before any Edit or AddNew:", .EditMode 
     .Edit 
     EditModeOutput "After Edit:", .EditMode 
     .Update 
     EditModeOutput "After Update:", .EditMode 
     .AddNew 
     EditModeOutput "After AddNew:", .EditMode 
     .CancelUpdate 
     EditModeOutput "After CancelUpdate:", .EditMode 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function EditModeOutput(strTemp As String, _ 
     intEditMode As Integer) 
     
     ' Print report based on the value of the EditMode 
     ' property. 
     Debug.Print strTemp 
     Debug.Print " EditMode = "; 
     
     Select Case intEditMode 
     Case dbEditNone 
     Debug.Print "dbEditNone" 
     Case dbEditInProgress 
     Debug.Print "dbEditInProgress" 
     Case dbEditAdd 
     Debug.Print "dbEditAdd" 
     End Select 
     
    End Function
```
