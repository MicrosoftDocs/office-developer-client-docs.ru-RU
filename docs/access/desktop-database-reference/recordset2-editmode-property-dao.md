---
title: Свойство Recordset2.EditMode (DAO)
TOCTitle: EditMode Property
ms:assetid: fd61ea2b-e7d7-195f-4114-87e54eba2451
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837240(v=office.15)
ms:contentKeyID: 48548914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053080
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d4043a442bec8c5ce421d85de6256eb9c5cb353f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307352"
---
# <a name="recordset2editmode-property-dao"></a>Свойство Recordset2.EditMode (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает состояние редактирования для текущей записи.

## <a name="syntax"></a>Синтаксис

*выражения* . EditMode

*выражение* Переменная, представляюная объект **Recordset2.**

## <a name="remarks"></a>Примечания

Возвращается значение **Long,** которое указывает состояние редактирования. Это значение может быть одним из **[констант EditModeEnum.](editmodeenum-enumeration-dao.md)**

Свойство **EditMode полезно,** если процесс редактирования прерывается, например, ошибкой во время проверки. Значение свойства **EditMode** можно использовать для определения того, следует ли использовать метод **[Update](recordset2-update-method-dao.md)** или **[CancelUpdate.](recordset2-cancelupdate-method-dao.md)**

Вы также можете проверить, является ли параметр  **[Свойства LockEdits](recordset2-lockedits-property-dao.md)** true, а параметр **свойства EditMode** **— dbEditInProgress,** чтобы определить, заблокирована ли текущая страница.

## <a name="example"></a>Пример

В этом примере показано значение **свойства EditMode** в различных условиях. Для запуска этой процедуры требуется функция EditModeOutput.

```vb
    Sub EditModeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     
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
