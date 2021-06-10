---
title: Метод Recordset.CancelUpdate (DAO)
TOCTitle: CancelUpdate method
ms:assetid: efc4f60b-876f-5e11-37fd-0fbbf225b15b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836421(v=office.15)
ms:contentKeyID: 48548590
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053072
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5950154d8896678889af01254104a2ac0dfef4cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300681"
---
# <a name="recordsetcancelupdate-method-dao"></a><span data-ttu-id="4b2ef-102">Метод Recordset.CancelUpdate (DAO)</span><span class="sxs-lookup"><span data-stu-id="4b2ef-102">Recordset.CancelUpdate method (DAO)</span></span>

<span data-ttu-id="4b2ef-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b2ef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b2ef-104">Отменяет любые незавершенные обновления для объекта **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="4b2ef-104">Cancels any pending updates for a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b2ef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b2ef-105">Syntax</span></span>

<span data-ttu-id="4b2ef-106">*выражения* . CancelUpdate ***(UpdateType)***</span><span class="sxs-lookup"><span data-stu-id="4b2ef-106">*expression* .CancelUpdate(***UpdateType***)</span></span>

<span data-ttu-id="4b2ef-107">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="4b2ef-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="4b2ef-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b2ef-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b2ef-109">Имя</span><span class="sxs-lookup"><span data-stu-id="4b2ef-109">Name</span></span></p></th>
<th><p><span data-ttu-id="4b2ef-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="4b2ef-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="4b2ef-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4b2ef-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="4b2ef-112">Описание</span><span class="sxs-lookup"><span data-stu-id="4b2ef-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b2ef-113"><em>UpdateType</em></span><span class="sxs-lookup"><span data-stu-id="4b2ef-113"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="4b2ef-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="4b2ef-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="4b2ef-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="4b2ef-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="4b2ef-116">Установите одно из <strong><a href="updatetypeenum-enumeration-dao.md">значений UpdateTypeEnum.</a></strong></span><span class="sxs-lookup"><span data-stu-id="4b2ef-116">Set to one of the <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> values.</span></span></p><p><span data-ttu-id="4b2ef-117"><strong>ПРИМЕЧАНИЕ.</strong>Значения <EM>dbUpdateRegular</EM> и <EM>dbUpdateBatch</EM> действительны только при включенной пакетной обновлении.</span><span class="sxs-lookup"><span data-stu-id="4b2ef-117"><strong>NOTE</strong>: The <EM>dbUpdateRegular</EM> and <EM>dbUpdateBatch</EM> values are valid only if batch updating is enabled.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4b2ef-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="4b2ef-118">Remarks</span></span>

<span data-ttu-id="4b2ef-119">С помощью метода **CancelUpdate** можно отменить все ожидающие обновления в результате операции **[Edit](recordset-edit-method-dao.md)** или **[AddNew.](recordset-addnew-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="4b2ef-119">You can use the **CancelUpdate** method to cancel any pending updates resulting from an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** operation.</span></span> <span data-ttu-id="4b2ef-120">Например, если пользователь вызывает метод **Edit** или **AddNew** и еще  не вызывает метод **Update, CancelUpdate** отменяет любые изменения, внесенные после вызова **Edit** или **AddNew.**</span><span class="sxs-lookup"><span data-stu-id="4b2ef-120">For example, if a user invokes the **Edit** or **AddNew** method and hasn't yet invoked the **Update** method, **CancelUpdate** cancels any changes made after **Edit** or **AddNew** was invoked.</span></span>

<span data-ttu-id="4b2ef-121">Проверьте свойство **[EditMode](recordset-editmode-property-dao.md)** в **Наборе записей,** чтобы определить, существует ли ожидаемая операция, которую можно отменить.</span><span class="sxs-lookup"><span data-stu-id="4b2ef-121">Check the **[EditMode](recordset-editmode-property-dao.md)** property of the **Recordset** to determine if there is a pending operation that can be canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="4b2ef-122">Использование метода **CancelUpdate** имеет тот же эффект, что **[](recordset-update-method-dao.md)** и переход на другую запись без использования метода Update, за исключением того, что текущая запись не меняется, а различные свойства, такие как **[BOF](recordset-bof-property-dao.md)** и **[EOF,](recordset-eof-property-dao.md)** не обновляются.</span><span class="sxs-lookup"><span data-stu-id="4b2ef-122">Using the **CancelUpdate** method has the same effect as moving to another record without using the **[Update](recordset-update-method-dao.md)** method, except that the current record doesn't change, and various properties, such as **[BOF](recordset-bof-property-dao.md)** and **[EOF](recordset-eof-property-dao.md)**, aren't updated.</span></span>


## <a name="example"></a><span data-ttu-id="4b2ef-123">Пример</span><span class="sxs-lookup"><span data-stu-id="4b2ef-123">Example</span></span>

<span data-ttu-id="4b2ef-124">В этом примере показано, как метод **CancelUpdate** используется с **методом AddNew.**</span><span class="sxs-lookup"><span data-stu-id="4b2ef-124">This example shows how the **CancelUpdate** method is used with the **AddNew** method.</span></span>

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim intCommand As Integer 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
          "Employees", dbOpenDynaset) 
     
       With rstEmployees 
          .AddNew 
          !FirstName = "Kimberly" 
          !LastName = "Bowen" 
          intCommand = MsgBox("Add new record for " & _ 
             !FirstName & " " & !LastName & "?", vbYesNo) 
          If intCommand = vbYes Then 
             .Update 
             MsgBox "Record added." 
             ' Delete new record because this is a  
             ' demonstration. 
             .Bookmark = .LastModified 
             .Delete 
          Else 
             .CancelUpdate 
             MsgBox "Record not added." 
          End If 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="4b2ef-125">В этом примере показано, как метод **CancelUpdate** используется с методом **Редактирование.**</span><span class="sxs-lookup"><span data-stu-id="4b2ef-125">This example shows how the **CancelUpdate** method is used with the **Edit** method.</span></span>

```vb
Sub CancelUpdateX2() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim strFirst As String 
   Dim strLast As String 
   Dim intCommand As Integer 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
      "Employees", dbOpenDynaset) 
 
   With rstEmployees 
      strFirst = !FirstName 
      strLast = !LastName 
      .Edit 
      !FirstName = "Cora" 
      !LastName = "Edmonds" 
      intCommand = MsgBox("Replace current name with " & _ 
         !FirstName & " " & !LastName & "?", vbYesNo) 
      If intCommand = vbYes Then 
         .Update 
         MsgBox "Record modified." 
         ' Restore data because this is a demonstration. 
         .Bookmark = .LastModified 
         .Edit 
         !FirstName = strFirst 
         !LastName = strLast 
         .Update 
      Else 
         .CancelUpdate 
         MsgBox "Record not modified." 
      End If 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
 
```

