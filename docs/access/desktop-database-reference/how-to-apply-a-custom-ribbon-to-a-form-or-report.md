---
title: Применение пользовательской ленты к форме или отчету
TOCTitle: Apply a custom ribbon to a form or report
description: Узнайте, как применять пользовательские ленты при загрузке формы или отчета в Access 2013.
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 329f184a1bcd3c856ccfd0b15c3fa92bc6230c98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291917"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a><span data-ttu-id="7d5a4-103">Применение пользовательской ленты к форме или отчету</span><span class="sxs-lookup"><span data-stu-id="7d5a4-103">Apply a custom ribbon to a form or report</span></span>

<span data-ttu-id="7d5a4-104">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d5a4-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7d5a4-105">На ленте используется текстовая, декларативная разметка XML, которая упрощает создание и настройку ленты.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-105">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="7d5a4-106">С помощью нескольких строк кода XML вы можете создать идеально подходящий для пользователя интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-106">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="7d5a4-107">В Access доступны широкие возможности настройки пользовательского интерфейса ленты.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-107">Access provides flexibility in customizing the ribbon user interface.</span></span> 

<span data-ttu-id="7d5a4-108">Например, разметку для настройки можно сохранить в таблице, внедрить в процедуру VBA или сохранить в другой базе данных Access. На нее также можно сослаться с листа Excel.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-108">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="7d5a4-109">В этой статье описывается применение пользовательских лент при загрузке формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-109">This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="7d5a4-110">Предоставление доступа к коду XML для настройки ленты</span><span class="sxs-lookup"><span data-stu-id="7d5a4-110">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="7d5a4-111">Сохранение кода XML для расширения ленты в таблице</span><span class="sxs-lookup"><span data-stu-id="7d5a4-111">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="7d5a4-112">Один из способов предоставления доступа к настройкам ленты — сохранить их в таблице.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-112">One method that you can use to make ribbon customizations available is to store them in a table.</span></span> <span data-ttu-id="7d5a4-113">Сохранив настройки в таблице **USysRibbons**, их можно реализовать без использования макросов и кода VBA.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-113">If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="7d5a4-114">**USysRibbons** — это созданная пользователем системная таблица.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-114">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="7d5a4-115">Таблицу необходимо создать с использованием конкретных имен столбцов для реализуемых настроек ленты.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-115">The table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="7d5a4-116">В приведенной ниже таблице перечислены параметры, используемые при создании таблицы **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-116">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d5a4-117">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="7d5a4-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="7d5a4-118">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7d5a4-118">Data type</span></span></p></th>
<th><p><span data-ttu-id="7d5a4-119">Описание</span><span class="sxs-lookup"><span data-stu-id="7d5a4-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d5a4-120"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="7d5a4-120"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="7d5a4-121">Текст</span><span class="sxs-lookup"><span data-stu-id="7d5a4-121">Text</span></span></p></td>
<td><p><span data-ttu-id="7d5a4-122">Содержит имя пользовательской ленты, которая будет связана с этой настройкой.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-122">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d5a4-123"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="7d5a4-123"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="7d5a4-124">Заметка</span><span class="sxs-lookup"><span data-stu-id="7d5a4-124">Memo</span></span></p></td>
<td><p><span data-ttu-id="7d5a4-125">Содержит код XML для расширения ленты (RibbonX), определяющий настройку ленты.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-125">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="7d5a4-126">Программная загрузка кода XML для расширения ленты</span><span class="sxs-lookup"><span data-stu-id="7d5a4-126">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="7d5a4-127">Вы можете использовать метод **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** для загрузки настроек ленты программным образом.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-127">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically.</span></span> <span data-ttu-id="7d5a4-128">Как правило, чтобы создать ленту и сделать ее доступной приложению, необходимо сначала создать модуль в базе данных с помощью процедуры, вызывающей метод **LoadCustomUI**, передав имя ленты в разметку настройки XML.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-128">Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="7d5a4-129">Разметка XML может быть взята из объекта **Recordset**, созданного с помощью таблицы, из источника за пределами базы данных, например XML-файла, преобразованного в строку, или из разметки XML, внедренной непосредственно в процедуру.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-129">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure.</span></span> <span data-ttu-id="7d5a4-130">Вы можете создавать различные ленты с помощью нескольких вызовов метода **LoadCustomUI**, передавая разную разметку XML, при условии что имя каждой ленты и атрибуты **id** вкладок, из которых состоит лента, будут уникальными.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-130">You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="7d5a4-131">По завершении процедуры можно создать макрос AutoExec, вызывающий процедуру с помощью действия RunCode.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-131">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="7d5a4-132">Таким образом, при запуске приложения автоматически выполняется метод **LoadCustomUI**, а приложению предоставляется доступ ко всем пользовательским лентам.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-132">That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="assign-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="7d5a4-133">Назначение пользовательских лент формам и отчетам</span><span class="sxs-lookup"><span data-stu-id="7d5a4-133">Assign custom ribbons to forms or reports</span></span>

1.  <span data-ttu-id="7d5a4-134">Выполните описанные выше действия, чтобы сделать настроенную ленту доступной приложению.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-134">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="7d5a4-135">Откройте форму или отчет в режиме конструктора.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-135">Open the form or report in Design view.</span></span>

3.  <span data-ttu-id="7d5a4-136">На вкладке "Конструктор" выберите элемент **Страница свойств**.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-136">On the Design tab, choose **Property Sheet**.</span></span>

4.  <span data-ttu-id="7d5a4-137">На вкладке **Все** окна свойств выберите список **Имя ленты**, а затем выберите ленту.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-137">On the **All** tab of the Property window, choose the **Ribbon Name** list and then select a ribbon.</span></span>

5.  <span data-ttu-id="7d5a4-138">Сохраните, закройте и заново откройте форму или отчет.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-138">Save, close, and then reopen the form or report.</span></span> <span data-ttu-id="7d5a4-139">Появится выбранный пользовательский интерфейс ленты.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-139">The ribbon UI you selected is displayed.</span></span>


> [!NOTE]
> <span data-ttu-id="7d5a4-140">Вкладки пользовательского интерфейса ленты является аддитивными.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-140">The tabs displayed in the ribbon UI are additive.</span></span> <span data-ttu-id="7d5a4-141">Это означает, что если вкладки не скрыты явным образом, а для атрибута *Начать с нуля* не задано значения **True**, то вкладки, отображаемые в пользовательском интерфейсе ленты для формы или отчета, будут добавлены к имеющимся вкладкам.</span><span class="sxs-lookup"><span data-stu-id="7d5a4-141">That is, unless you specifically hide the tabs or set the *Start from Scratch* attribute to **True**, the tabs displayed in a form's or report's ribbon user interface are in addition to the existing tabs.</span></span>

> [!NOTE]
> <span data-ttu-id="7d5a4-142">Дополнительные сведения о пользовательском интерфейсе ленты в других приложениях Office см. в статье [Обзор ленты Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="7d5a4-142">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


