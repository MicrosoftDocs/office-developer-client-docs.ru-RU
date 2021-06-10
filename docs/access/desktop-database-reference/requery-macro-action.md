---
title: Макрокоманда Requery
TOCTitle: Requery macro action
ms:assetid: 6dbdcae5-81b6-9925-4cad-64b178c23060
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195544(v=office.15)
ms:contentKeyID: 48545499
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm30402
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 8b90af8d1cda073ffa37022bb5db5e8cf8e3b978
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306708"
---
# <a name="requery-macro-action"></a><span data-ttu-id="3e4a9-102">Макрокоманда Requery</span><span class="sxs-lookup"><span data-stu-id="3e4a9-102">Requery macro action</span></span>

<span data-ttu-id="3e4a9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e4a9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3e4a9-104">Вы можете использовать действие **Requery** для обновления данных в указанном контроле на активном объекте, переокупив источник управления.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-104">You can use the **Requery** action to update the data in a specified control on the active object by requerying the source of the control.</span></span> <span data-ttu-id="3e4a9-105">Если не задано управление, это действие повторно завоюет источник самого объекта.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-105">If no control is specified, this action requeries the source of the object itself.</span></span> <span data-ttu-id="3e4a9-106">Используйте это действие, чтобы убедиться, что активный объект или один из его элементов управления отображает самые актуальные данные.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-106">Use this action to ensure that the active object or one of its controls displays the most current data.</span></span>

## <a name="setting"></a><span data-ttu-id="3e4a9-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="3e4a9-107">Setting</span></span>

<span data-ttu-id="3e4a9-108">Действие **Requery** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-108">The **Requery** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3e4a9-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="3e4a9-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3e4a9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="3e4a9-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e4a9-111"><strong>Имя элемента управления</strong></span><span class="sxs-lookup"><span data-stu-id="3e4a9-111"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="3e4a9-112">Имя необходимого для обновления управления.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-112">The name of the control you want to update.</span></span> <span data-ttu-id="3e4a9-113">Введите имя управления в поле <strong>Имя управления</strong> в разделе <strong>Аргументы</strong> действий в области Macro Builder.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-113">Enter the control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="3e4a9-114">Необходимо использовать только имя управления, а не полностью квалифицированный идентификатор <strong>(например, Forms!</strong><em> formname!</em> <em>controlname</em>).</span><span class="sxs-lookup"><span data-stu-id="3e4a9-114">You should use only the name of the control, not the fully qualified identifier (such as <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>).</span></span> <span data-ttu-id="3e4a9-115">Оставьте этот аргумент пустым, чтобы переоставьте источник активного объекта.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-115">Leave this argument blank to requery the source of the active object.</span></span> <span data-ttu-id="3e4a9-116">Если активным объектом является таблица данных или набор результатов запроса, необходимо оставить этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-116">If the active object is a datasheet or a query result set, you must leave this argument blank.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3e4a9-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="3e4a9-117">Remarks</span></span>

<span data-ttu-id="3e4a9-118">Действие **Requery** делает одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="3e4a9-118">The **Requery** action does one of the following:</span></span>

- <span data-ttu-id="3e4a9-119">Повторное повторяющий запрос, на котором основан контроль или объект.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-119">Reruns the query on which the control or object is based.</span></span>

- <span data-ttu-id="3e4a9-120">Отображает новые или измененные записи и удаляет удаленные записи из таблицы, на которой основан контроль или объект.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-120">Displays any new or changed records, and removes any deleted records from the table on which the control or object is based.</span></span>

> [!NOTE]
> <span data-ttu-id="3e4a9-121">Действие **Requery** не влияет на положение указателя записи.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-121">The **Requery** action does not affect the position of the record pointer.</span></span>

<span data-ttu-id="3e4a9-122">Элементы управления на основе запроса или таблицы включают:</span><span class="sxs-lookup"><span data-stu-id="3e4a9-122">Controls based on a query or table include:</span></span>

- <span data-ttu-id="3e4a9-123">Списки и комбо-поля.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-123">List boxes and combo boxes.</span></span>

- <span data-ttu-id="3e4a9-124">Элементы управления subform.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-124">Subform controls.</span></span>

- <span data-ttu-id="3e4a9-125">Объекты OLE, например диаграммы.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-125">OLE objects, such as charts.</span></span>

- <span data-ttu-id="3e4a9-126">Элементы управления, содержащие агрегированные функции домена, такие как **DSum.**</span><span class="sxs-lookup"><span data-stu-id="3e4a9-126">Controls containing domain aggregate functions, such as **DSum**.</span></span>

<span data-ttu-id="3e4a9-127">Если указанный контроль не основан на запросе или таблице, это действие заставляет пересчет управления.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-127">If the specified control isn't based on a query or table, this action forces a recalculation of the control.</span></span>

<span data-ttu-id="3e4a9-128">Если оставить аргумент **"Имя** управления" пустым, действие **Requery** имеет тот же эффект, что и нажатие SHIFT+F9, когда объект имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-128">If you leave the **Control Name** argument blank, the **Requery** action has the same effect as pressing SHIFT+F9 when the object has the focus.</span></span> <span data-ttu-id="3e4a9-129">Если в центре внимания имеется управление подформами, это действие переоформит только источник подформы (точно так же, как и нажатие SHIFT+F9).</span><span class="sxs-lookup"><span data-stu-id="3e4a9-129">If a subform control has the focus, this action requeries only the source of the subform (just as pressing SHIFT+F9 does).</span></span>

> [!NOTE]
> <span data-ttu-id="3e4a9-130">Действие **Requery requery** повторно завоюет источник управления или объекта.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-130">The **Requery** action requeries the source of the control or object.</span></span> <span data-ttu-id="3e4a9-131">В отличие от этого, действие **RepaintObject** переквартирует элементы управления в указанном объекте, но не переопректирует базу данных и не отображает новые записи.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-131">In contrast, the **RepaintObject** action repaints controls in the specified object but doesn't requery the database or display new records.</span></span> <span data-ttu-id="3e4a9-132">Действие **ShowAllRecords** не только requeries активного объекта, но и удаляет все примененные фильтры, которые действие **Requery** не делают.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-132">The **ShowAllRecords** action not only requeries the active object, but it also removes any applied filters, which the **Requery** action doesn't do.</span></span>

<span data-ttu-id="3e4a9-133">Если требуется отыскать контроль, который не находится на активном объекте, необходимо использовать метод **Requery** в модуле Visual Basic для приложений (VBA), а не действие **Requery** или соответствующий метод **requery** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="3e4a9-133">If you want to requery a control that isn't on the active object, you must use the **Requery** method in a Visual Basic for Applications (VBA) module, not the **Requery** action or its corresponding **Requery** method of the **DoCmd** object.</span></span> <span data-ttu-id="3e4a9-134">Метод **Requery** в VBA быстрее, чем действие **Requery** или **метод DoCmd.Requery.**</span><span class="sxs-lookup"><span data-stu-id="3e4a9-134">The **Requery** method in VBA is faster than the **Requery** action or the **DoCmd.Requery** method.</span></span> <span data-ttu-id="3e4a9-135">Кроме того, при использовании действия **Requery** или метода **DoCmd.Requery** Microsoft Access закрывает запрос и перезагружает его из базы данных, но при использовании метода **Requery** Access повторно передает запрос, не закрывая и не перезагружая его.</span><span class="sxs-lookup"><span data-stu-id="3e4a9-135">In addition, when you use the **Requery** action or the **DoCmd.Requery** method, Microsoft Access closes the query and reloads it from the database, but when you use the **Requery** method, Access reruns the query without closing and reloading it.</span></span> <span data-ttu-id="3e4a9-136">Обратите внимание, что метод ActiveX (ADO) **Requery** работает так же, как метод Access **Requery.**</span><span class="sxs-lookup"><span data-stu-id="3e4a9-136">Note that the ActiveX Data object (ADO) **Requery** method works the same way as the Access **Requery** method.</span></span>

