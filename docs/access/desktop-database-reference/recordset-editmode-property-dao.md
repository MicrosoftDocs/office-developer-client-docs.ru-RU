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
# <a name="recordseteditmode-property-dao"></a><span data-ttu-id="c0291-102">Свойство Recordset.EditMode (DAO)</span><span class="sxs-lookup"><span data-stu-id="c0291-102">Recordset.EditMode property (DAO)</span></span>


<span data-ttu-id="c0291-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0291-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c0291-104">Возвращает значение, которое указывает состояние редактирования для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="c0291-104">Returns a value that indicates the state of editing for the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0291-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0291-105">Syntax</span></span>

<span data-ttu-id="c0291-106">*выражения* . EditMode</span><span class="sxs-lookup"><span data-stu-id="c0291-106">*expression* .EditMode</span></span>

<span data-ttu-id="c0291-107">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c0291-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0291-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="c0291-108">Remarks</span></span>

<span data-ttu-id="c0291-109">Возвращается значение **Long,** которое указывает состояние редактирования.</span><span class="sxs-lookup"><span data-stu-id="c0291-109">The return value is a **Long** that indicates the state of editing.</span></span> <span data-ttu-id="c0291-110">Это значение может быть одним из **[констант EditModeEnum.](editmodeenum-enumeration-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="c0291-110">The value can be one of the **[EditModeEnum](editmodeenum-enumeration-dao.md)** constants.</span></span>

<span data-ttu-id="c0291-111">Свойство **EditMode полезно,** если процесс редактирования прерывается, например, ошибкой во время проверки.</span><span class="sxs-lookup"><span data-stu-id="c0291-111">The **EditMode** property is useful when an editing process is interrupted, for example, by an error during validation.</span></span> <span data-ttu-id="c0291-112">Значение свойства **EditMode** можно использовать для определения того, следует ли использовать метод **[Update](recordset-update-method-dao.md)** или **[CancelUpdate.](recordset-cancelupdate-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="c0291-112">You can use the value of the **EditMode** property to determine whether you should use the **[Update](recordset-update-method-dao.md)** or **[CancelUpdate](recordset-cancelupdate-method-dao.md)** method.</span></span>

<span data-ttu-id="c0291-113">Вы также можете проверить, является ли параметр  **[Свойства LockEdits](recordset-lockedits-property-dao.md)** true, а параметр **свойства EditMode** **— dbEditInProgress,** чтобы определить, заблокирована ли текущая страница.</span><span class="sxs-lookup"><span data-stu-id="c0291-113">You can also check to see if the **[LockEdits](recordset-lockedits-property-dao.md)** property setting is **True** and the **EditMode** property setting is **dbEditInProgress** to determine whether the current page is locked.</span></span>

## <a name="example"></a><span data-ttu-id="c0291-114">Пример</span><span class="sxs-lookup"><span data-stu-id="c0291-114">Example</span></span>

<span data-ttu-id="c0291-115">В этом примере показано значение **свойства EditMode** в различных условиях.</span><span class="sxs-lookup"><span data-stu-id="c0291-115">This example shows the value of the **EditMode** property under various conditions.</span></span> <span data-ttu-id="c0291-116">Для запуска этой процедуры требуется функция EditModeOutput.</span><span class="sxs-lookup"><span data-stu-id="c0291-116">The EditModeOutput function is required for this procedure to run.</span></span>

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
