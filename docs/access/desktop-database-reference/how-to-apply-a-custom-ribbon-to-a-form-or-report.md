---
title: Применение пользовательской ленты к форме или отчету
TOCTitle: Apply a custom ribbon to a form or report
description: Как применить настроенные ленты при загрузке формы или отчета в Access 2013.
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 10/16/2018
mtps_version: v=office.15
ms.openlocfilehash: e494985054ffd91440f3aff6eb671b781a5f65d7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888827"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a><span data-ttu-id="fc032-103">Применение пользовательской ленты к форме или отчету</span><span class="sxs-lookup"><span data-stu-id="fc032-103">Apply a custom ribbon to a form or report</span></span>

<span data-ttu-id="fc032-104">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc032-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fc032-105">Ленты использует текстовую декларативную разметку XML, упрощающую создание и настройку ленты.</span><span class="sxs-lookup"><span data-stu-id="fc032-105">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="fc032-106">С помощью нескольких строк XML можно создать только что правом интерфейс для пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc032-106">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="fc032-107">Access обеспечивает гибкость при настройке пользовательского интерфейса ленты.</span><span class="sxs-lookup"><span data-stu-id="fc032-107">Access provides flexibility in customizing the ribbon user interface.</span></span> 

<span data-ttu-id="fc032-108">Например разметку для настройки может быть хранятся в таблице, внедренные в процедуре VBA, хранящиеся в другую базу данных Access или по ссылке из листа Excel.</span><span class="sxs-lookup"><span data-stu-id="fc032-108">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="fc032-109">В этом разделе описывается применение настроенной ленты при загрузке формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="fc032-109">This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="fc032-110">Сделать доступными настройки ленты XML</span><span class="sxs-lookup"><span data-stu-id="fc032-110">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="fc032-111">Расширяемость ленты хранилища XML в таблице</span><span class="sxs-lookup"><span data-stu-id="fc032-111">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="fc032-112">— Это один метод, который можно использовать для настройки ленты доступны для их хранения в таблице.</span><span class="sxs-lookup"><span data-stu-id="fc032-112">One method that you can use to make ribbon customizations available is to store them in a table.</span></span> <span data-ttu-id="fc032-113">При сохранении настроек в таблице с именем **USysRibbons**настроек может быть реализовано без с помощью макросов или кода VBA.</span><span class="sxs-lookup"><span data-stu-id="fc032-113">If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="fc032-114">**USysRibbons** — это таблица системы, созданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="fc032-114">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="fc032-115">В таблице должны быть созданы с помощью имена определенных столбцов для настройки ленты для реализации.</span><span class="sxs-lookup"><span data-stu-id="fc032-115">The table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="fc032-116">В следующей таблице перечислены параметры для использования при создании в таблице **USysRibbons** .</span><span class="sxs-lookup"><span data-stu-id="fc032-116">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc032-117">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="fc032-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="fc032-118">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fc032-118">Data type</span></span></p></th>
<th><p><span data-ttu-id="fc032-119">Описание</span><span class="sxs-lookup"><span data-stu-id="fc032-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc032-120"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="fc032-120"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="fc032-121">Текст</span><span class="sxs-lookup"><span data-stu-id="fc032-121">Text</span></span></p></td>
<td><p><span data-ttu-id="fc032-122">Содержит имя настраиваемой ленты, который будет связан с этой настройкой.</span><span class="sxs-lookup"><span data-stu-id="fc032-122">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc032-123"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="fc032-123"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="fc032-124">Заметка</span><span class="sxs-lookup"><span data-stu-id="fc032-124">Memo</span></span></p></td>
<td><p><span data-ttu-id="fc032-125">Содержит расширяемость ленты XML (RibbonX), который определяет настройки ленты.</span><span class="sxs-lookup"><span data-stu-id="fc032-125">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="fc032-126">Загрузить расширения ленты XML программным путем</span><span class="sxs-lookup"><span data-stu-id="fc032-126">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="fc032-127">Можно использовать метод **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** для загрузки настроек ленты программными средствами.</span><span class="sxs-lookup"><span data-stu-id="fc032-127">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically.</span></span> <span data-ttu-id="fc032-128">Как правило чтобы создать и становится доступной для приложения ленты, сначала создайте модуль в базе данных с помощью процедуры, вызывающий метод **LoadCustomUI** , передавая имя ленты и разметки XML для настройки.</span><span class="sxs-lookup"><span data-stu-id="fc032-128">Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="fc032-129">XML-разметка могут поступать из объекта **набора записей** , созданных из таблицы, из источника, внешними по отношению к базы данных, например XML-файл, который проанализировать в строку или из XML-разметка внедрена непосредственно в процедуру.</span><span class="sxs-lookup"><span data-stu-id="fc032-129">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure.</span></span> <span data-ttu-id="fc032-130">Можно выполнять различные ленты с помощью нескольких звонков на метод **LoadCustomUI** , передав в различных XML-разметка, поскольку имя каждой ленты и вкладки, которые составляют ленты для атрибута **id** — уникальный.</span><span class="sxs-lookup"><span data-stu-id="fc032-130">You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="fc032-131">После завершения процедуры нажмите Создать макрос AutoExec, который вызывает процедуру с использованием действием RunCode.</span><span class="sxs-lookup"><span data-stu-id="fc032-131">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="fc032-132">Таким образом, при запуске приложения метод **LoadCustomUI** выполняется автоматически и все настраиваемые ленты доступны для приложения.</span><span class="sxs-lookup"><span data-stu-id="fc032-132">That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="assign-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="fc032-133">Назначение настраиваемой ленты для форм и отчетов</span><span class="sxs-lookup"><span data-stu-id="fc032-133">Assign custom ribbons to forms or reports</span></span>

1.  <span data-ttu-id="fc032-134">Выполните действия, описанные выше, чтобы сделать доступным для приложения настраиваемой ленты.</span><span class="sxs-lookup"><span data-stu-id="fc032-134">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="fc032-135">Откройте форму или отчет в режиме конструктора.</span><span class="sxs-lookup"><span data-stu-id="fc032-135">Open the form or report in Design view.</span></span>

3.  <span data-ttu-id="fc032-136">На вкладке конструктор выберите **Страницы свойств**.</span><span class="sxs-lookup"><span data-stu-id="fc032-136">On the Design tab, choose **Property Sheet**.</span></span>

4.  <span data-ttu-id="fc032-137">На вкладке **все** окна Свойства выберите в списке **Имя ленты** и затем выберите ленты.</span><span class="sxs-lookup"><span data-stu-id="fc032-137">On the **All** tab of the Property window, choose the **Ribbon Name** list and then select a ribbon.</span></span>

5.  <span data-ttu-id="fc032-138">Сохраните, закройте и снова откройте форму или отчет.</span><span class="sxs-lookup"><span data-stu-id="fc032-138">Save, close, and then reopen the form or report.</span></span> <span data-ttu-id="fc032-139">Отображается пользовательский Интерфейс, выбранный ленты.</span><span class="sxs-lookup"><span data-stu-id="fc032-139">The ribbon UI you selected is displayed.</span></span>


> [!NOTE]
> <span data-ttu-id="fc032-140">Вкладки на ленте пользовательского интерфейса-дополнительная.</span><span class="sxs-lookup"><span data-stu-id="fc032-140">The tabs displayed in the ribbon UI are additive.</span></span> <span data-ttu-id="fc032-141">То есть до специально скрытия вкладки или *с самого начала* атрибуту присваивается **значение True**, вкладки отображаются в форме или пользовательского интерфейса ленты отчета, в дополнение к существующих вкладок.</span><span class="sxs-lookup"><span data-stu-id="fc032-141">That is, unless you specifically hide the tabs or set the *Start from Scratch* attribute to **True**, the tabs displayed in a form's or report's ribbon user interface are in addition to the existing tabs.</span></span>

> [!NOTE]
> <span data-ttu-id="fc032-142">Дополнительные сведения о пользовательский Интерфейс ленты в других приложениях Office можно [Обзор ленты Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="fc032-142">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


