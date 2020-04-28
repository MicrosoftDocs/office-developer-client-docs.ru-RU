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
# <a name="requery-macro-action"></a><span data-ttu-id="89041-102">Макрокоманда Requery</span><span class="sxs-lookup"><span data-stu-id="89041-102">Requery macro action</span></span>

<span data-ttu-id="89041-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89041-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="89041-104">Вы можете использовать действие **Requery** для обновления данных в указанном элементе управления в активном объекте, заменив запрос к источнику этого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="89041-104">You can use the **Requery** action to update the data in a specified control on the active object by requerying the source of the control.</span></span> <span data-ttu-id="89041-105">Если элемент управления не указан, это действие повторно запрашивает источник самого объекта.</span><span class="sxs-lookup"><span data-stu-id="89041-105">If no control is specified, this action requeries the source of the object itself.</span></span> <span data-ttu-id="89041-106">Используйте это действие, чтобы убедиться, что активный объект или один из его элементов управления отображает актуальные данные.</span><span class="sxs-lookup"><span data-stu-id="89041-106">Use this action to ensure that the active object or one of its controls displays the most current data.</span></span>

## <a name="setting"></a><span data-ttu-id="89041-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="89041-107">Setting</span></span>

<span data-ttu-id="89041-108">Действие **Requery** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="89041-108">The **Requery** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89041-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="89041-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="89041-110">Описание</span><span class="sxs-lookup"><span data-stu-id="89041-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89041-111"><strong>Имя элемента управления</strong></span><span class="sxs-lookup"><span data-stu-id="89041-111"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="89041-112">Имя элемента управления, который необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="89041-112">The name of the control you want to update.</span></span> <span data-ttu-id="89041-113">Введите имя элемента управления в поле <strong>имя элемента управления</strong> в разделе <strong>аргументы макрокоманды</strong> в области построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="89041-113">Enter the control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="89041-114">Следует использовать только имя элемента управления, а не полный идентификатор (например, <strong>Forms</strong>!<em> FormName</em>! <em>контролнаме</em>).</span><span class="sxs-lookup"><span data-stu-id="89041-114">You should use only the name of the control, not the fully qualified identifier (such as <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>).</span></span> <span data-ttu-id="89041-115">Оставьте этот аргумент пустым, чтобы запросить источник активного объекта.</span><span class="sxs-lookup"><span data-stu-id="89041-115">Leave this argument blank to requery the source of the active object.</span></span> <span data-ttu-id="89041-116">Если активный объект является таблицей данных или набором результатов запроса, необходимо оставить этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="89041-116">If the active object is a datasheet or a query result set, you must leave this argument blank.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="89041-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="89041-117">Remarks</span></span>

<span data-ttu-id="89041-118">Действие **Requery** выполняет одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="89041-118">The **Requery** action does one of the following:</span></span>

- <span data-ttu-id="89041-119">Повторно выполняет запрос, на котором основан элемент управления или объект.</span><span class="sxs-lookup"><span data-stu-id="89041-119">Reruns the query on which the control or object is based.</span></span>

- <span data-ttu-id="89041-120">Отображает все новые или измененные записи, а также удаляет все удаленные записи из таблицы, на которой основан элемент управления или объект.</span><span class="sxs-lookup"><span data-stu-id="89041-120">Displays any new or changed records, and removes any deleted records from the table on which the control or object is based.</span></span>

> [!NOTE]
> <span data-ttu-id="89041-121">Действие **Requery** не влияет на положение указателя записи.</span><span class="sxs-lookup"><span data-stu-id="89041-121">The **Requery** action does not affect the position of the record pointer.</span></span>

<span data-ttu-id="89041-122">Элементы управления, основанные на запросе или таблице, включают:</span><span class="sxs-lookup"><span data-stu-id="89041-122">Controls based on a query or table include:</span></span>

- <span data-ttu-id="89041-123">Списки и поля со списками.</span><span class="sxs-lookup"><span data-stu-id="89041-123">List boxes and combo boxes.</span></span>

- <span data-ttu-id="89041-124">Элементы управления подчиненной формы.</span><span class="sxs-lookup"><span data-stu-id="89041-124">Subform controls.</span></span>

- <span data-ttu-id="89041-125">Объекты OLE, например диаграммы.</span><span class="sxs-lookup"><span data-stu-id="89041-125">OLE objects, such as charts.</span></span>

- <span data-ttu-id="89041-126">Элементы управления, содержащие статистические функции домена, такие как **DSum**.</span><span class="sxs-lookup"><span data-stu-id="89041-126">Controls containing domain aggregate functions, such as **DSum**.</span></span>

<span data-ttu-id="89041-127">Если указанный элемент управления не основан на запросе или таблице, это действие приводит к пересчету элемента управления.</span><span class="sxs-lookup"><span data-stu-id="89041-127">If the specified control isn't based on a query or table, this action forces a recalculation of the control.</span></span>

<span data-ttu-id="89041-128">Если оставить аргумент " **имя элемента управления** " пустым, действие **Requery** будет иметь такое же действие, как нажатие клавиш SHIFT + F9, когда объект находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="89041-128">If you leave the **Control Name** argument blank, the **Requery** action has the same effect as pressing SHIFT+F9 when the object has the focus.</span></span> <span data-ttu-id="89041-129">Если фокус находится на элементе управления подчиненной формы, это действие повторно запрашивает только источник подчиненной формы (аналогично нажатию клавиши SHIFT + F9).</span><span class="sxs-lookup"><span data-stu-id="89041-129">If a subform control has the focus, this action requeries only the source of the subform (just as pressing SHIFT+F9 does).</span></span>

> [!NOTE]
> <span data-ttu-id="89041-130">Действие **Requeries** повторно запрашивает источник элемента управления или объекта.</span><span class="sxs-lookup"><span data-stu-id="89041-130">The **Requery** action requeries the source of the control or object.</span></span> <span data-ttu-id="89041-131">В отличие от этого, действие **репаинтобжект** перерисовывает элементы управления в указанном объекте, но не записывает базу данных или не отображает новые записи.</span><span class="sxs-lookup"><span data-stu-id="89041-131">In contrast, the **RepaintObject** action repaints controls in the specified object but doesn't requery the database or display new records.</span></span> <span data-ttu-id="89041-132">Действие **шоваллрекордс** не только повторно запрашивает активный объект, но и удаляет все примененные фильтры, не выполняемые действием **requeries** .</span><span class="sxs-lookup"><span data-stu-id="89041-132">The **ShowAllRecords** action not only requeries the active object, but it also removes any applied filters, which the **Requery** action doesn't do.</span></span>

<span data-ttu-id="89041-133">Если необходимо запросить элемент управления, не включенный в активный объект, необходимо использовать метод **Requery** в модуле Visual Basic для приложений (VBA), а не действие **Requery** или соответствующий метод **Requery** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="89041-133">If you want to requery a control that isn't on the active object, you must use the **Requery** method in a Visual Basic for Applications (VBA) module, not the **Requery** action or its corresponding **Requery** method of the **DoCmd** object.</span></span> <span data-ttu-id="89041-134">Метод **Requery** в языке VBA работает быстрее, чем действие **Requery** . Requery. Requery. **Requery** . Requery.</span><span class="sxs-lookup"><span data-stu-id="89041-134">The **Requery** method in VBA is faster than the **Requery** action or the **DoCmd.Requery** method.</span></span> <span data-ttu-id="89041-135">Кроме того, при использовании макрокоманды **Reload** или **DoCmd. Reload** Microsoft Access закрывает запрос и перезагружает его из базы данных, но при использовании метода **Reload** запрос повторно выполнит запрос без закрытия и перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="89041-135">In addition, when you use the **Requery** action or the **DoCmd.Requery** method, Microsoft Access closes the query and reloads it from the database, but when you use the **Requery** method, Access reruns the query without closing and reloading it.</span></span> <span data-ttu-id="89041-136">Обратите внимание, что метод **Requery** объекта данных ACTIVEX (ADO) работает так же, как метод **Requery** Access.</span><span class="sxs-lookup"><span data-stu-id="89041-136">Note that the ActiveX Data object (ADO) **Requery** method works the same way as the Access **Requery** method.</span></span>

