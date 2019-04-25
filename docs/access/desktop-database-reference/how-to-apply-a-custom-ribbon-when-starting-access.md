---
title: Применение пользовательской ленты при запуске Access
TOCTitle: Apply a custom ribbon when starting Access
description: Узнайте, как применять пользовательские ленты при открытии базы данных в Access 2013.
ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15)
ms:contentKeyID: 48546659
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 0acd99a498a74f098b08814e9f11d49b28bae097
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291959"
---
# <a name="apply-a-custom-ribbon-when-starting-access"></a><span data-ttu-id="400b3-103">Применение пользовательской ленты при запуске Access</span><span class="sxs-lookup"><span data-stu-id="400b3-103">Apply a custom ribbon when starting Access</span></span>

<span data-ttu-id="400b3-104">**Область применения**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="400b3-104">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="400b3-105">На ленте используется текстовая, декларативная разметка XML, которая упрощает создание и настройку ленты.</span><span class="sxs-lookup"><span data-stu-id="400b3-105">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="400b3-106">С помощью нескольких строк кода XML вы можете создать идеально подходящий для пользователя интерфейс.</span><span class="sxs-lookup"><span data-stu-id="400b3-106">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="400b3-107">В Access доступны широчайшие возможности настройки пользовательского интерфейса ленты.</span><span class="sxs-lookup"><span data-stu-id="400b3-107">Access provides flexibility in customizing the ribbon user interface.</span></span> <span data-ttu-id="400b3-108">Например, разметку для настройки можно сохранить в таблице, внедрить в процедуру VBA или сохранить в другой базе данных Access. На нее также можно сослаться с листа Excel.</span><span class="sxs-lookup"><span data-stu-id="400b3-108">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="400b3-109">В этой статье описывается применение пользовательских лент при открытии базы данных.</span><span class="sxs-lookup"><span data-stu-id="400b3-109">This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="400b3-110">Предоставление доступа к коду XML для настройки ленты</span><span class="sxs-lookup"><span data-stu-id="400b3-110">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="400b3-111">Сохранение кода XML для расширения ленты в таблице</span><span class="sxs-lookup"><span data-stu-id="400b3-111">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="400b3-112">Один из способов предоставления доступа к настройкам ленты — сохранить их в таблице.</span><span class="sxs-lookup"><span data-stu-id="400b3-112">One method that you can use to make ribbon customizations available is to store them in a table.</span></span> <span data-ttu-id="400b3-113">Сохранив настройки в таблице **USysRibbons**, их можно реализовать без использования макросов и кода VBA.</span><span class="sxs-lookup"><span data-stu-id="400b3-113">If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="400b3-114">**USysRibbons** — это созданная пользователем системная таблица.</span><span class="sxs-lookup"><span data-stu-id="400b3-114">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="400b3-115">Таблицу необходимо создать с использованием конкретных имен столбцов для реализуемых настроек ленты.</span><span class="sxs-lookup"><span data-stu-id="400b3-115">The table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="400b3-116">В приведенной ниже таблице перечислены параметры, используемые при создании таблицы **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="400b3-116">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="400b3-117">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="400b3-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="400b3-118">Тип данных</span><span class="sxs-lookup"><span data-stu-id="400b3-118">Data type</span></span></p></th>
<th><p><span data-ttu-id="400b3-119">Описание</span><span class="sxs-lookup"><span data-stu-id="400b3-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="400b3-120"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="400b3-120"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="400b3-121">Текст</span><span class="sxs-lookup"><span data-stu-id="400b3-121">Text</span></span></p></td>
<td><p><span data-ttu-id="400b3-122">Содержит имя пользовательской ленты, которая будет связана с этой настройкой.</span><span class="sxs-lookup"><span data-stu-id="400b3-122">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="400b3-123"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="400b3-123"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="400b3-124">Заметка</span><span class="sxs-lookup"><span data-stu-id="400b3-124">Memo</span></span></p></td>
<td><p><span data-ttu-id="400b3-125">Содержит код XML для расширения ленты (RibbonX), определяющий настройку ленты.</span><span class="sxs-lookup"><span data-stu-id="400b3-125">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="400b3-126">Программная загрузка кода XML для расширения ленты</span><span class="sxs-lookup"><span data-stu-id="400b3-126">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="400b3-127">Вы можете использовать метод **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** для загрузки настроек ленты программным образом.</span><span class="sxs-lookup"><span data-stu-id="400b3-127">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically.</span></span> <span data-ttu-id="400b3-128">Как правило, чтобы создать ленту и сделать ее доступной приложению, необходимо сначала создать модуль в базе данных с помощью процедуры, вызывающей метод **LoadCustomUI**, передав имя ленты в разметку настройки XML.</span><span class="sxs-lookup"><span data-stu-id="400b3-128">Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="400b3-129">Разметка XML может быть взята из объекта **Recordset**, созданного с помощью таблицы, из источника за пределами базы данных, например XML-файла, преобразованного в строку, или из разметки XML, внедренной непосредственно в процедуру.</span><span class="sxs-lookup"><span data-stu-id="400b3-129">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure.</span></span> <span data-ttu-id="400b3-130">Вы можете создавать различные ленты с помощью нескольких вызовов метода **LoadCustomUI**, передавая разную разметку XML, при условии что имя каждой ленты и атрибуты **id** вкладок, из которых состоит лента, будут уникальными.</span><span class="sxs-lookup"><span data-stu-id="400b3-130">You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="400b3-131">По завершении процедуры можно создать макрос AutoExec, вызывающий процедуру с помощью действия RunCode.</span><span class="sxs-lookup"><span data-stu-id="400b3-131">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="400b3-132">Таким образом, при запуске приложения автоматически выполняется метод **LoadCustomUI**, а приложению предоставляется доступ ко всем пользовательским лентам.</span><span class="sxs-lookup"><span data-stu-id="400b3-132">That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="apply-customized-ribbons-when-access-starts"></a><span data-ttu-id="400b3-133">Применение пользовательских лент при запуске Access</span><span class="sxs-lookup"><span data-stu-id="400b3-133">Apply customized ribbons when Access starts</span></span>

<span data-ttu-id="400b3-134">Чтобы применить настраиваемый пользовательский интерфейс, который будет доступен при запуске приложения, используйте описанную ниже процедуру.</span><span class="sxs-lookup"><span data-stu-id="400b3-134">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="400b3-135">Выполните описанные выше действия, чтобы сделать настроенные ленты доступными приложению.</span><span class="sxs-lookup"><span data-stu-id="400b3-135">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="400b3-136">Закройте и перезапустите приложение.</span><span class="sxs-lookup"><span data-stu-id="400b3-136">Close and then restart the application.</span></span>

3.  <span data-ttu-id="400b3-137">Нажмите **кнопку Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") и выберите пункт **Параметры Access**.</span><span class="sxs-lookup"><span data-stu-id="400b3-137">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="400b3-138">Выберите вариант **Текущая база данных**, а затем в разделе **Параметры ленты и панелей инструментов** щелкните список **Имя ленты** и выберите ленту.</span><span class="sxs-lookup"><span data-stu-id="400b3-138">Choose the Current Database option and then, in the Ribbon and Toolbar Options section, choose the Ribbon Name list and select HideTheRibbon.</span></span>

5.  <span data-ttu-id="400b3-139">Теперь закройте и перезапустите приложение.</span><span class="sxs-lookup"><span data-stu-id="400b3-139">Now close and restart the application.</span></span> <span data-ttu-id="400b3-140">Появится выбранный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="400b3-140">The ribbon UI you selected is displayed.</span></span>

> [!NOTE]
> <span data-ttu-id="400b3-141">Дополнительные сведения о пользовательском интерфейсе ленты в других приложениях Office см. в статье [Обзор ленты Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="400b3-141">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


