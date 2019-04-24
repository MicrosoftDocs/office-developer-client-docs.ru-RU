---
title: Свойство Recordset. RecordsetType (DAO)
TOCTitle: RecordsetType Property
ms:assetid: a66d4043-08cc-ead1-f9ff-efc7d7ea21bf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821178(v=office.15)
ms:contentKeyID: 48546853
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13361
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 64f7dda8bec7806ef510d265deab350dc3cdad6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307632"
---
# <a name="recordsetrecordsettype-property-dao"></a><span data-ttu-id="6bc47-102">Свойство Recordset. RecordsetType (DAO)</span><span class="sxs-lookup"><span data-stu-id="6bc47-102">Recordset.RecordsetType property (DAO)</span></span>

<span data-ttu-id="6bc47-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6bc47-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6bc47-104">Свойство **RecordsetType** можно использовать, чтобы указать тип набора записей, доступный для формы.</span><span class="sxs-lookup"><span data-stu-id="6bc47-104">You can use the **RecordsetType** property to specify what kind of recordset is made available to a form.</span></span> <span data-ttu-id="6bc47-105">**Байт**для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6bc47-105">Read/write **Byte**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bc47-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6bc47-106">Syntax</span></span>

<span data-ttu-id="6bc47-107">*Expression* . RecordsetType</span><span class="sxs-lookup"><span data-stu-id="6bc47-107">*expression* .RecordsetType</span></span>

<span data-ttu-id="6bc47-108">*выражение*: переменная, представляющая объект **Form**.</span><span class="sxs-lookup"><span data-stu-id="6bc47-108">*expression* A variable that represents a **Form** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bc47-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="6bc47-109">Remarks</span></span>

<span data-ttu-id="6bc47-110">Свойство **RecordsetType** использует следующие параметры в базе данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="6bc47-110">The **RecordsetType** property uses the following settings in a Microsoft Access database.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6bc47-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="6bc47-111">Setting</span></span></p></th>
<th><p><span data-ttu-id="6bc47-112">Тип объекта Recordset</span><span class="sxs-lookup"><span data-stu-id="6bc47-112">Type of Recordset</span></span></p></th>
<th><p><span data-ttu-id="6bc47-113">Описание</span><span class="sxs-lookup"><span data-stu-id="6bc47-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6bc47-114">нуль</span><span class="sxs-lookup"><span data-stu-id="6bc47-114">0</span></span></p></td>
<td><p><span data-ttu-id="6bc47-115">Типа dynaset</span><span class="sxs-lookup"><span data-stu-id="6bc47-115">Dynaset</span></span></p></td>
<td><p><span data-ttu-id="6bc47-116">Умолчани Можно редактировать присвязанные элементы управления на основе одной таблицы или таблиц с отношением "один к одному".</span><span class="sxs-lookup"><span data-stu-id="6bc47-116">(Default) You can edit bound controls based on a single table or tables with a one-to-one relationship.</span></span> <span data-ttu-id="6bc47-117">Для элементов управления, привязанных к полям, основанным на таблицах с отношением "один ко многим" &quot;, нельзя изменить данные из поля&quot; присоединения на одной стороне отношения, если между таблицами не включено каскадное обновление.</span><span class="sxs-lookup"><span data-stu-id="6bc47-117">For controls bound to fields based on tables with a one-to-many relationship, you can't edit data from the join field on the &quot;one&quot; side of the relationship unless cascade update is enabled between the tables.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bc47-118">1,1</span><span class="sxs-lookup"><span data-stu-id="6bc47-118">1</span></span></p></td>
<td><p><span data-ttu-id="6bc47-119">Динамическое подМножество (несогласованные обновления)</span><span class="sxs-lookup"><span data-stu-id="6bc47-119">Dynaset (Inconsistent Updates)</span></span></p></td>
<td><p><span data-ttu-id="6bc47-120">Можно редактировать все таблицы и элементы управления, привязанные к их полям.</span><span class="sxs-lookup"><span data-stu-id="6bc47-120">All tables and controls bound to their fields can be edited.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bc47-121">2</span><span class="sxs-lookup"><span data-stu-id="6bc47-121">2</span></span></p></td>
<td><p><span data-ttu-id="6bc47-122">Статически</span><span class="sxs-lookup"><span data-stu-id="6bc47-122">Snapshot</span></span></p></td>
<td><p><span data-ttu-id="6bc47-123">Не допускается редактирование таблиц и элементов управления, привязанных к их полям.</span><span class="sxs-lookup"><span data-stu-id="6bc47-123">No tables or the controls bound to their fields can be edited.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6bc47-124">Если вы не хотите, чтобы данные в привязанных элементах управления были изменены, если форма находится в режиме формы или в режиме таблицы, можно задать для свойства **RecordsetType** значение 2.</span><span class="sxs-lookup"><span data-stu-id="6bc47-124">If you don't want data in bound controls to be edited when a form is in Form view or Datasheet view, you can set the **RecordsetType** property to 2.</span></span>

<span data-ttu-id="6bc47-125">Свойство **RecordsetType** использует следующие параметры в проекте Microsoft Access (ADP).</span><span class="sxs-lookup"><span data-stu-id="6bc47-125">The **RecordsetType** property uses the following settings in a Microsoft Access project (.adp).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6bc47-126">Параметр</span><span class="sxs-lookup"><span data-stu-id="6bc47-126">Setting</span></span></p></th>
<th><p><span data-ttu-id="6bc47-127">Тип объекта Recordset</span><span class="sxs-lookup"><span data-stu-id="6bc47-127">Type of Recordset</span></span></p></th>
<th><p><span data-ttu-id="6bc47-128">Описание</span><span class="sxs-lookup"><span data-stu-id="6bc47-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6bc47-129">4</span><span class="sxs-lookup"><span data-stu-id="6bc47-129">3</span></span></p></td>
<td><p><span data-ttu-id="6bc47-130">Статически</span><span class="sxs-lookup"><span data-stu-id="6bc47-130">Snapshot</span></span></p></td>
<td><p><span data-ttu-id="6bc47-131">Не допускается редактирование таблиц и элементов управления, привязанных к их полям.</span><span class="sxs-lookup"><span data-stu-id="6bc47-131">No tables or the controls bound to their fields can be edited.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bc47-132">SP4</span><span class="sxs-lookup"><span data-stu-id="6bc47-132">4</span></span></p></td>
<td><p><span data-ttu-id="6bc47-133">Обновляемый моментальный снимок</span><span class="sxs-lookup"><span data-stu-id="6bc47-133">Updatable Snapshot</span></span></p></td>
<td><p><span data-ttu-id="6bc47-134">Умолчани Можно редактировать все таблицы и элементы управления, привязанные к их полям.</span><span class="sxs-lookup"><span data-stu-id="6bc47-134">(Default) All tables and controls bound to their fields can be edited.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6bc47-135">Изменение свойства **RecordsetType** для открытой формы или отчета приводит к автоматическому воссозданию объекта Recordset.</span><span class="sxs-lookup"><span data-stu-id="6bc47-135">Changing the **RecordsetType** property of an open form or report causes an automatic recreation of the recordset.</span></span>

<span data-ttu-id="6bc47-136">Вы можете создавать формы на основе нескольких базовых таблиц с полями, связанными с элементами управления в формах.</span><span class="sxs-lookup"><span data-stu-id="6bc47-136">You can create forms based on multiple underlying tables with fields bound to controls on the forms.</span></span> <span data-ttu-id="6bc47-137">В зависимости от значения свойства **RecordsetType** можно ограничить возможности редактирования этих связанных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="6bc47-137">Depending on the **RecordsetType** property setting, you can limit which of these bound controls can be edited.</span></span>

<span data-ttu-id="6bc47-138">Помимо элемента управления редактирования, предоставленного **RecordsetType**, у каждого элемента управления в форме есть свойство **locked** , которое можно задать, чтобы указать, можно ли редактировать элемент управления и его базовые данные.</span><span class="sxs-lookup"><span data-stu-id="6bc47-138">In addition to the editing control provided by **RecordsetType**, each control on a form has a **Locked** property that you can set to specify whether the control and its underlying data can be edited.</span></span> <span data-ttu-id="6bc47-139">Если свойству **locked** присвоено значение "Да", данные изменить нельзя.</span><span class="sxs-lookup"><span data-stu-id="6bc47-139">If the **Locked** property is set to Yes, you can't edit the data.</span></span>

## <a name="example"></a><span data-ttu-id="6bc47-140">Пример</span><span class="sxs-lookup"><span data-stu-id="6bc47-140">Example</span></span>

<span data-ttu-id="6bc47-141">В следующем примере только в том случае, если идентификатор пользователя является АДМИНИСТРАТОРом, могут быть обновлены записи.</span><span class="sxs-lookup"><span data-stu-id="6bc47-141">In the following example, only if the user ID is ADMIN can records be updated.</span></span> <span data-ttu-id="6bc47-142">В этом примере кода для свойства **RecordsetType** задается значение snapshot, если общедоступная переменная гструсерид имеет значение Not admin.</span><span class="sxs-lookup"><span data-stu-id="6bc47-142">This code sample sets the **RecordsetType** property to Snapshot if the public variable gstrUserID value is not ADMIN.</span></span>

```vb
    Sub Form_Open(Cancel As Integer) 
     Const conSnapshot = 2 
     If gstrUserID <> "ADMIN" Then 
     Forms!Employees.RecordsetType = conSnapshot 
     End If 
    End Sub
```

## <a name="see-also"></a><span data-ttu-id="6bc47-143">См. также</span><span class="sxs-lookup"><span data-stu-id="6bc47-143">See also</span></span>

- [<span data-ttu-id="6bc47-144">Объект Form</span><span class="sxs-lookup"><span data-stu-id="6bc47-144">Form Object</span></span>](https://docs.microsoft.com/office/vba/api/Access.Form)


