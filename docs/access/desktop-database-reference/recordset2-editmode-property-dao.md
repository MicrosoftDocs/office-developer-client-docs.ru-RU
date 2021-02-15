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
# <a name="recordset2editmode-property-dao"></a><span data-ttu-id="8e2f0-102">Свойство Recordset2.EditMode (DAO)</span><span class="sxs-lookup"><span data-stu-id="8e2f0-102">Recordset2.EditMode property (DAO)</span></span>


<span data-ttu-id="8e2f0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e2f0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8e2f0-104">Возвращает значение, которое указывает состояние редактирования для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-104">Returns a value that indicates the state of editing for the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e2f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e2f0-105">Syntax</span></span>

<span data-ttu-id="8e2f0-106">*выражение .* EditMode</span><span class="sxs-lookup"><span data-stu-id="8e2f0-106">*expression* .EditMode</span></span>

<span data-ttu-id="8e2f0-107">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="8e2f0-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e2f0-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="8e2f0-108">Remarks</span></span>

<span data-ttu-id="8e2f0-109">Возвращаемая величина — **long,** которая указывает состояние редактирования.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-109">The return value is a **Long** that indicates the state of editing.</span></span> <span data-ttu-id="8e2f0-110">Значение может быть одной из **[констант EditModeEnum.](editmodeenum-enumeration-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="8e2f0-110">The value can be one of the **[EditModeEnum](editmodeenum-enumeration-dao.md)** constants.</span></span>

<span data-ttu-id="8e2f0-111">Свойство **EditMode полезно** использовать, если процесс редактирования прерывается, например, из-за ошибки во время проверки.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-111">The **EditMode** property is useful when an editing process is interrupted, for example, by an error during validation.</span></span> <span data-ttu-id="8e2f0-112">Значение свойства **EditMode** можно использовать, чтобы определить, следует ли использовать метод **[Update](recordset2-update-method-dao.md)** или **[CancelUpdate.](recordset2-cancelupdate-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="8e2f0-112">You can use the value of the **EditMode** property to determine whether you should use the **[Update](recordset2-update-method-dao.md)** or **[CancelUpdate](recordset2-cancelupdate-method-dao.md)** method.</span></span>

<span data-ttu-id="8e2f0-113">Вы также можете проверить, имеет ли свойство **[LockEdits](recordset2-lockedits-property-dao.md)** состояние **True,** а для свойства **EditMode** — **dbEditInProgress,** чтобы определить, заблокирована ли текущая страница.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-113">You can also check to see if the **[LockEdits](recordset2-lockedits-property-dao.md)** property setting is **True** and the **EditMode** property setting is **dbEditInProgress** to determine whether the current page is locked.</span></span>

## <a name="example"></a><span data-ttu-id="8e2f0-114">Пример</span><span class="sxs-lookup"><span data-stu-id="8e2f0-114">Example</span></span>

<span data-ttu-id="8e2f0-115">В этом примере показано значение свойства **EditMode** в различных условиях.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-115">This example shows the value of the **EditMode** property under various conditions.</span></span> <span data-ttu-id="8e2f0-116">Для запуска этой процедуры требуется функция EditModeOutput.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-116">The EditModeOutput function is required for this procedure to run.</span></span>

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
