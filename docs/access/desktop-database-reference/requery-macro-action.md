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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705990"
---
# <a name="requery-macro-action"></a><span data-ttu-id="a3bca-102">Макрокоманда Requery</span><span class="sxs-lookup"><span data-stu-id="a3bca-102">Requery macro action</span></span>

<span data-ttu-id="a3bca-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3bca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3bca-104">Действие **запроса** можно использовать для обновления данных в указанный элемент управления для текущего объекта повторным запросом источника элемента управления.</span><span class="sxs-lookup"><span data-stu-id="a3bca-104">You can use the **Requery** action to update the data in a specified control on the active object by requerying the source of the control.</span></span> <span data-ttu-id="a3bca-105">Если элемент не указан, это действие вызывает повторный запрос источника самого объекта.</span><span class="sxs-lookup"><span data-stu-id="a3bca-105">If no control is specified, this action requeries the source of the object itself.</span></span> <span data-ttu-id="a3bca-106">Используйте это действие для убедитесь, что объекте или в элементе управления отображает текущих данных.</span><span class="sxs-lookup"><span data-stu-id="a3bca-106">Use this action to ensure that the active object or one of its controls displays the most current data.</span></span>

## <a name="setting"></a><span data-ttu-id="a3bca-107">Setting</span><span class="sxs-lookup"><span data-stu-id="a3bca-107">Setting</span></span>

<span data-ttu-id="a3bca-108">Действие **повторный запрос** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="a3bca-108">The **Requery** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3bca-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="a3bca-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a3bca-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a3bca-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3bca-111"><strong>Имя элемента управления</strong></span><span class="sxs-lookup"><span data-stu-id="a3bca-111"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="a3bca-112">Имя элемента управления, который требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="a3bca-112">The name of the control you want to update.</span></span> <span data-ttu-id="a3bca-113">Введите имя элемента управления в поле <strong>Имя элемента управления</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="a3bca-113">Enter the control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="a3bca-114">Следует использовать только имя элемента управления, не полный идентификатор (например, <strong>Forms</strong>!<em> имя_формы</em>! <em>ИмяЭлементаУправления</em>).</span><span class="sxs-lookup"><span data-stu-id="a3bca-114">You should use only the name of the control, not the fully qualified identifier (such as <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>).</span></span> <span data-ttu-id="a3bca-115">Этот аргумент оставьте поле пустым при обновлении активного объекта.</span><span class="sxs-lookup"><span data-stu-id="a3bca-115">Leave this argument blank to requery the source of the active object.</span></span> <span data-ttu-id="a3bca-116">Если активный объект является таблица или результат запроса задано, необходимо оставить этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="a3bca-116">If the active object is a datasheet or a query result set, you must leave this argument blank.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a3bca-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="a3bca-117">Remarks</span></span>

<span data-ttu-id="a3bca-118">Действие **повторный запрос** выполняет одно из следующих действия.</span><span class="sxs-lookup"><span data-stu-id="a3bca-118">The **Requery** action does one of the following:</span></span>

- <span data-ttu-id="a3bca-119">Повторно выполняет запрос, на котором основан элемент управления или объекта.</span><span class="sxs-lookup"><span data-stu-id="a3bca-119">Reruns the query on which the control or object is based.</span></span>

- <span data-ttu-id="a3bca-120">Отображает все новые или измененные записи и удаляет все удаленные записи из таблицы, на котором основан элемент управления или объекта.</span><span class="sxs-lookup"><span data-stu-id="a3bca-120">Displays any new or changed records, and removes any deleted records from the table on which the control or object is based.</span></span>

> [!NOTE]
> <span data-ttu-id="a3bca-121">Действие **повторный запрос** не влияет на положение указателя записи.</span><span class="sxs-lookup"><span data-stu-id="a3bca-121">The **Requery** action does not affect the position of the record pointer.</span></span>

<span data-ttu-id="a3bca-122">Следующие элементы управления на основе запроса или в таблице:</span><span class="sxs-lookup"><span data-stu-id="a3bca-122">Controls based on a query or table include:</span></span>

- <span data-ttu-id="a3bca-123">Списки и поля со списками.</span><span class="sxs-lookup"><span data-stu-id="a3bca-123">List boxes and combo boxes.</span></span>

- <span data-ttu-id="a3bca-124">Подчиненная форма элементов управления.</span><span class="sxs-lookup"><span data-stu-id="a3bca-124">Subform controls.</span></span>

- <span data-ttu-id="a3bca-125">Объекты OLE, такие как диаграммы.</span><span class="sxs-lookup"><span data-stu-id="a3bca-125">OLE objects, such as charts.</span></span>

- <span data-ttu-id="a3bca-126">Элементы управления, содержащий домен агрегатных функций, таких как **DSum**.</span><span class="sxs-lookup"><span data-stu-id="a3bca-126">Controls containing domain aggregate functions, such as **DSum**.</span></span>

<span data-ttu-id="a3bca-127">Если указанный элемент управления не на основе запроса или таблицы, приводит пересчета элемента управления.</span><span class="sxs-lookup"><span data-stu-id="a3bca-127">If the specified control isn't based on a query or table, this action forces a recalculation of the control.</span></span>

<span data-ttu-id="a3bca-128">Если аргумент **Имя элемента управления** не заполнено, действие **повторный запрос** имеет тот же эффект, как при нажатии клавиши SHIFT + F9, когда объект имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="a3bca-128">If you leave the **Control Name** argument blank, the **Requery** action has the same effect as pressing SHIFT+F9 when the object has the focus.</span></span> <span data-ttu-id="a3bca-129">Если элемент управления подчиненной формы имеет фокус, это действие вызывает повторный запрос только источника данных подчиненной формы (так же, как при нажатии клавиши SHIFT + F9).</span><span class="sxs-lookup"><span data-stu-id="a3bca-129">If a subform control has the focus, this action requeries only the source of the subform (just as pressing SHIFT+F9 does).</span></span>

> [!NOTE]
> <span data-ttu-id="a3bca-130">Действие **повторный запрос** вызывает повторный запрос источника элемента управления или объекта.</span><span class="sxs-lookup"><span data-stu-id="a3bca-130">The **Requery** action requeries the source of the control or object.</span></span> <span data-ttu-id="a3bca-131">С другой стороны **ОбновитьОбъект** перерисует элементов управления в указанном объекте, но не повторный запрос базы данных или отображения новых записей.</span><span class="sxs-lookup"><span data-stu-id="a3bca-131">In contrast, the **RepaintObject** action repaints controls in the specified object but doesn't requery the database or display new records.</span></span> <span data-ttu-id="a3bca-132">**ПоказатьВсеЗаписи** не только вызывает повторный запрос активного объекта, но оно также удаляет все примененные фильтры, которых не выполняет действие **повторный запрос** .</span><span class="sxs-lookup"><span data-stu-id="a3bca-132">The **ShowAllRecords** action not only requeries the active object, but it also removes any applied filters, which the **Requery** action doesn't do.</span></span>

<span data-ttu-id="a3bca-133">Если требуется повторный запрос элемент управления, который не для текущего объекта, необходимо использовать метод **запроса** в Visual Basic для приложений (VBA) модуль, не действие **повторный запрос** или его соответствующий метод **повторный запрос** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="a3bca-133">If you want to requery a control that isn't on the active object, you must use the **Requery** method in a Visual Basic for Applications (VBA) module, not the **Requery** action or its corresponding **Requery** method of the **DoCmd** object.</span></span> <span data-ttu-id="a3bca-134">Выполняется быстрее, чем действие **повторный запрос** или метод **DoCmd.Requery** **повторного VBA** .</span><span class="sxs-lookup"><span data-stu-id="a3bca-134">The **Requery** method in VBA is faster than the **Requery** action or the **DoCmd.Requery** method.</span></span> <span data-ttu-id="a3bca-135">Кроме того при использовании действие **повторный запрос** или метод **DoCmd.Requery** Microsoft Access закрывает запрос и перезагружает из базы данных, но при использовании метода **повторный запрос** повторно выполняет запрос без закрытия и перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="a3bca-135">In addition, when you use the **Requery** action or the **DoCmd.Requery** method, Microsoft Access closes the query and reloads it from the database, but when you use the **Requery** method, Access reruns the query without closing and reloading it.</span></span> <span data-ttu-id="a3bca-136">Обратите внимание, что объект данных ActiveX (ADO) **повторный запрос** метод работает так же, как метод доступа **повторный запрос** .</span><span class="sxs-lookup"><span data-stu-id="a3bca-136">Note that the ActiveX Data object (ADO) **Requery** method works the same way as the Access **Requery** method.</span></span>

