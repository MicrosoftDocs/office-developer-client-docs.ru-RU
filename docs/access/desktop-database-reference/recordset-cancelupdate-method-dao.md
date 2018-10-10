---
title: Recordset.CancelUpdate Method (DAO)
TOCTitle: CancelUpdate Method
ms:assetid: efc4f60b-876f-5e11-37fd-0fbbf225b15b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836421(v=office.15)
ms:contentKeyID: 48548590
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053072
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ca7f21d4607e8934f80ab807cae36002b0cf5d2b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480502"
---
# <a name="recordsetcancelupdate-method-dao"></a><span data-ttu-id="323fe-102">Recordset.CancelUpdate Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="323fe-102">Recordset.CancelUpdate Method (DAO)</span></span>


<span data-ttu-id="323fe-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="323fe-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="323fe-104">Отменяет все ожидающие обновления для объекта **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="323fe-104">Cancels any pending updates for a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="323fe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="323fe-105">Syntax</span></span>

<span data-ttu-id="323fe-106">*выражение* . CancelUpdate (***UpdateType***)</span><span class="sxs-lookup"><span data-stu-id="323fe-106">*expression* .CancelUpdate(***UpdateType***)</span></span>

<span data-ttu-id="323fe-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="323fe-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="323fe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="323fe-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="323fe-109">Имя</span><span class="sxs-lookup"><span data-stu-id="323fe-109">Name</span></span></p></th>
<th><p><span data-ttu-id="323fe-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="323fe-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="323fe-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="323fe-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="323fe-112">Описание</span><span class="sxs-lookup"><span data-stu-id="323fe-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="323fe-113">UpdateType</span><span class="sxs-lookup"><span data-stu-id="323fe-113">UpdateType</span></span></p></td>
<td><p><span data-ttu-id="323fe-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="323fe-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="323fe-115"><strong>Длинный</strong></span><span class="sxs-lookup"><span data-stu-id="323fe-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="323fe-116">Установите одно из значений <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="323fe-116">Set to one of the <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> values.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="323fe-117">Значения <EM>dbUpdateRegular</EM> и <EM>dbUpdateBatch</EM> являются допустимыми только в том случае, если обновление пакета включен.</span><span class="sxs-lookup"><span data-stu-id="323fe-117">The <EM>dbUpdateRegular</EM> and <EM>dbUpdateBatch</EM> values are valid only if batch updating is enabled.</span></span></P>


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="323fe-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="323fe-118">Remarks</span></span>

<span data-ttu-id="323fe-119">Чтобы отменить все ожидающие обновления, полученный после **[изменения](recordset-edit-method-dao.md)** или **[AddNew](recordset-addnew-method-dao.md)** операции можно использовать метод **CancelUpdate** .</span><span class="sxs-lookup"><span data-stu-id="323fe-119">You can use the **CancelUpdate** method to cancel any pending updates resulting from an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** operation.</span></span> <span data-ttu-id="323fe-120">Например если пользователь вызывает метод **AddNew** или **Изменить** и еще не вызван метод **Update** , **CancelUpdate** показано, как отменить все изменения, внесенные после **изменения** или **AddNew** вызван.</span><span class="sxs-lookup"><span data-stu-id="323fe-120">For example, if a user invokes the **Edit** or **AddNew** method and hasn't yet invoked the **Update** method, **CancelUpdate** cancels any changes made after **Edit** or **AddNew** was invoked.</span></span>

<span data-ttu-id="323fe-121">Проверьте свойство **[EditMode](recordset-editmode-property-dao.md)** **набора записей** для определения ожидающие операции, которая может быть отменена.</span><span class="sxs-lookup"><span data-stu-id="323fe-121">Check the **[EditMode](recordset-editmode-property-dao.md)** property of the **Recordset** to determine if there is a pending operation that can be canceled.</span></span>


> [!NOTE]
> <P><span data-ttu-id="323fe-122">С помощью метода <STRONG>CancelUpdate</STRONG> имеет тот же эффект, как перейти к другой записи без с помощью метода <STRONG><A href="recordset-update-method-dao.md">Update</A></STRONG> , за исключением того, что текущей записи не изменяется и не обновляются различные свойства, такие как <STRONG><A href="recordset-bof-property-dao.md">BOF</A></STRONG> и <STRONG><A href="recordset-eof-property-dao.md">EOF</A></STRONG>.</span><span class="sxs-lookup"><span data-stu-id="323fe-122">Using the <STRONG>CancelUpdate</STRONG> method has the same effect as moving to another record without using the <STRONG><A href="recordset-update-method-dao.md">Update</A></STRONG> method, except that the current record doesn't change, and various properties, such as <STRONG><A href="recordset-bof-property-dao.md">BOF</A></STRONG> and <STRONG><A href="recordset-eof-property-dao.md">EOF</A></STRONG>, aren't updated.</span></span></P>



## <a name="example"></a><span data-ttu-id="323fe-123">Пример</span><span class="sxs-lookup"><span data-stu-id="323fe-123">Example</span></span>

<span data-ttu-id="323fe-124">В этом примере показано использование метода **CancelUpdate** с помощью метода **AddNew** .</span><span class="sxs-lookup"><span data-stu-id="323fe-124">This example shows how the **CancelUpdate** method is used with the **AddNew** method.</span></span>

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

<span data-ttu-id="323fe-125">В этом примере показано, как метод **CancelUpdate** используется с методом **изменения** .</span><span class="sxs-lookup"><span data-stu-id="323fe-125">This example shows how the **CancelUpdate** method is used with the **Edit** method.</span></span>

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

