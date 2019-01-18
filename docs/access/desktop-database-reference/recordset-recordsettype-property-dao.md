---
title: Свойство Recordset.RecordsetType (DAO)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709659"
---
# <a name="recordsetrecordsettype-property-dao"></a><span data-ttu-id="0dc90-102">Свойство Recordset.RecordsetType (DAO)</span><span class="sxs-lookup"><span data-stu-id="0dc90-102">Recordset.RecordsetType property (DAO)</span></span>

<span data-ttu-id="0dc90-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0dc90-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0dc90-104">Свойство **Тип набора записей** можно использовать для указания типа набора записей можно сделать доступной для формы.</span><span class="sxs-lookup"><span data-stu-id="0dc90-104">You can use the **RecordsetType** property to specify what kind of recordset is made available to a form.</span></span> <span data-ttu-id="0dc90-105">Чтение и запись **байтов**.</span><span class="sxs-lookup"><span data-stu-id="0dc90-105">Read/write **Byte**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dc90-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0dc90-106">Syntax</span></span>

<span data-ttu-id="0dc90-107">*выражение* . Тип набора записей</span><span class="sxs-lookup"><span data-stu-id="0dc90-107">*expression* .RecordsetType</span></span>

<span data-ttu-id="0dc90-108">*выражение* Переменная, которая представляет собой объект- **форму** .</span><span class="sxs-lookup"><span data-stu-id="0dc90-108">*expression* A variable that represents a **Form** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dc90-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="0dc90-109">Remarks</span></span>

<span data-ttu-id="0dc90-110">Свойство **Тип набора записей** используются следующие параметры в базе данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0dc90-110">The **RecordsetType** property uses the following settings in a Microsoft Access database.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0dc90-111">Setting</span><span class="sxs-lookup"><span data-stu-id="0dc90-111">Setting</span></span></p></th>
<th><p><span data-ttu-id="0dc90-112">Тип набора записей</span><span class="sxs-lookup"><span data-stu-id="0dc90-112">Type of Recordset</span></span></p></th>
<th><p><span data-ttu-id="0dc90-113">Описание</span><span class="sxs-lookup"><span data-stu-id="0dc90-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0dc90-114">0</span><span class="sxs-lookup"><span data-stu-id="0dc90-114">0</span></span></p></td>
<td><p><span data-ttu-id="0dc90-115">Динамический набор</span><span class="sxs-lookup"><span data-stu-id="0dc90-115">Dynaset</span></span></p></td>
<td><p><span data-ttu-id="0dc90-116">(По умолчанию) Вы можете изменить привязки элементов управления на основе одной таблицы или таблиц с отношением «один к одному».</span><span class="sxs-lookup"><span data-stu-id="0dc90-116">(Default) You can edit bound controls based on a single table or tables with a one-to-one relationship.</span></span> <span data-ttu-id="0dc90-117">Для элементов управления, привязанных к полям таблиц в отношении один ко многим, не могут изменять данные из поля присоединиться к на &quot;один&quot; сторона отношения cascade обновление не подключена между таблицами.</span><span class="sxs-lookup"><span data-stu-id="0dc90-117">For controls bound to fields based on tables with a one-to-many relationship, you can't edit data from the join field on the &quot;one&quot; side of the relationship unless cascade update is enabled between the tables.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc90-118">1</span><span class="sxs-lookup"><span data-stu-id="0dc90-118">1</span></span></p></td>
<td><p><span data-ttu-id="0dc90-119">Динамический набор (неправильное обновления)</span><span class="sxs-lookup"><span data-stu-id="0dc90-119">Dynaset (Inconsistent Updates)</span></span></p></td>
<td><p><span data-ttu-id="0dc90-120">Можно редактировать все таблицы и элементов управления, присоединенных к их полям.</span><span class="sxs-lookup"><span data-stu-id="0dc90-120">All tables and controls bound to their fields can be edited.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dc90-121">2</span><span class="sxs-lookup"><span data-stu-id="0dc90-121">2</span></span></p></td>
<td><p><span data-ttu-id="0dc90-122">Моментальный снимок</span><span class="sxs-lookup"><span data-stu-id="0dc90-122">Snapshot</span></span></p></td>
<td><p><span data-ttu-id="0dc90-123">Нет таблиц или элементов управления, привязанных к их поля могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="0dc90-123">No tables or the controls bound to their fields can be edited.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="0dc90-124">Если вы не хотите данные в связанных элементов управления для редактирования при открытии формы в режиме формы или таблицы, свойства **Тип набора записей** значение 2.</span><span class="sxs-lookup"><span data-stu-id="0dc90-124">If you don't want data in bound controls to be edited when a form is in Form view or Datasheet view, you can set the **RecordsetType** property to 2.</span></span>

<span data-ttu-id="0dc90-125">Свойство **Тип набора записей** используются следующие параметры в проекте Microsoft Access (файлы с расширением ADP).</span><span class="sxs-lookup"><span data-stu-id="0dc90-125">The **RecordsetType** property uses the following settings in a Microsoft Access project (.adp).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0dc90-126">Setting</span><span class="sxs-lookup"><span data-stu-id="0dc90-126">Setting</span></span></p></th>
<th><p><span data-ttu-id="0dc90-127">Тип набора записей</span><span class="sxs-lookup"><span data-stu-id="0dc90-127">Type of Recordset</span></span></p></th>
<th><p><span data-ttu-id="0dc90-128">Описание</span><span class="sxs-lookup"><span data-stu-id="0dc90-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0dc90-129">3</span><span class="sxs-lookup"><span data-stu-id="0dc90-129">3</span></span></p></td>
<td><p><span data-ttu-id="0dc90-130">Моментальный снимок</span><span class="sxs-lookup"><span data-stu-id="0dc90-130">Snapshot</span></span></p></td>
<td><p><span data-ttu-id="0dc90-131">Нет таблиц или элементов управления, привязанных к их поля могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="0dc90-131">No tables or the controls bound to their fields can be edited.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dc90-132">4</span><span class="sxs-lookup"><span data-stu-id="0dc90-132">4</span></span></p></td>
<td><p><span data-ttu-id="0dc90-133">Обновляемые моментальных снимков</span><span class="sxs-lookup"><span data-stu-id="0dc90-133">Updatable Snapshot</span></span></p></td>
<td><p><span data-ttu-id="0dc90-134">(По умолчанию) Можно редактировать все таблицы и элементов управления, присоединенных к их полям.</span><span class="sxs-lookup"><span data-stu-id="0dc90-134">(Default) All tables and controls bound to their fields can be edited.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="0dc90-135">Изменение свойства **Тип набора записей** открытая форма или отчет вызывает автоматическое воссоздание набора записей.</span><span class="sxs-lookup"><span data-stu-id="0dc90-135">Changing the **RecordsetType** property of an open form or report causes an automatic recreation of the recordset.</span></span>

<span data-ttu-id="0dc90-136">Можно создавать формы, основанные на нескольких таблицах с помощью полей, привязанных к элементам управления в формах.</span><span class="sxs-lookup"><span data-stu-id="0dc90-136">You can create forms based on multiple underlying tables with fields bound to controls on the forms.</span></span> <span data-ttu-id="0dc90-137">В зависимости от настройки свойства **Тип набора записей** , можно ограничить, какой из этих связанных элементов управления можно изменить их невозможно.</span><span class="sxs-lookup"><span data-stu-id="0dc90-137">Depending on the **RecordsetType** property setting, you can limit which of these bound controls can be edited.</span></span>

<span data-ttu-id="0dc90-138">Помимо управления редактирования предоставлено **Тип набора записей**каждого элемента управления в форме имеет свойство **Locked** , можно задать для определения, является ли элемент управления и базовые данные можно изменить.</span><span class="sxs-lookup"><span data-stu-id="0dc90-138">In addition to the editing control provided by **RecordsetType**, each control on a form has a **Locked** property that you can set to specify whether the control and its underlying data can be edited.</span></span> <span data-ttu-id="0dc90-139">Если свойство **Locked** задано значение Да, не могут изменять данные.</span><span class="sxs-lookup"><span data-stu-id="0dc90-139">If the **Locked** property is set to Yes, you can't edit the data.</span></span>

## <a name="example"></a><span data-ttu-id="0dc90-140">Пример</span><span class="sxs-lookup"><span data-stu-id="0dc90-140">Example</span></span>

<span data-ttu-id="0dc90-141">В следующем примере только в том случае, если пользователю присваивается идентификатор АДМИНИСТРАТОР может записи обновляться.</span><span class="sxs-lookup"><span data-stu-id="0dc90-141">In the following example, only if the user ID is ADMIN can records be updated.</span></span> <span data-ttu-id="0dc90-142">Этот пример кода задает свойство **Тип набора записей** к снимку Если значение общей переменной gstrUserID не администратор.</span><span class="sxs-lookup"><span data-stu-id="0dc90-142">This code sample sets the **RecordsetType** property to Snapshot if the public variable gstrUserID value is not ADMIN.</span></span>

```vb
    Sub Form_Open(Cancel As Integer) 
     Const conSnapshot = 2 
     If gstrUserID <> "ADMIN" Then 
     Forms!Employees.RecordsetType = conSnapshot 
     End If 
    End Sub
```

## <a name="see-also"></a><span data-ttu-id="0dc90-143">См. также</span><span class="sxs-lookup"><span data-stu-id="0dc90-143">See also</span></span>

- [<span data-ttu-id="0dc90-144">Объект Form</span><span class="sxs-lookup"><span data-stu-id="0dc90-144">Form Object</span></span>](https://docs.microsoft.com/office/vba/api/Access.Form)


