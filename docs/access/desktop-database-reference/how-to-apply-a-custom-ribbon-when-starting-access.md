---
title: Применение пользовательской ленты при запуске Access
TOCTitle: Apply a custom ribbon when starting Access
description: Как применить настроенные ленты при открытии базы данных в Access 2013.
ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15)
ms:contentKeyID: 48546659
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 0acd99a498a74f098b08814e9f11d49b28bae097
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709623"
---
# <a name="apply-a-custom-ribbon-when-starting-access"></a><span data-ttu-id="495ae-103">Применение пользовательской ленты при запуске Access</span><span class="sxs-lookup"><span data-stu-id="495ae-103">Apply a custom ribbon when starting Access</span></span>

<span data-ttu-id="495ae-104">**Применимо к:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="495ae-104">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="495ae-105">Ленты использует текстовую декларативную разметку XML, упрощающую создание и настройку ленты.</span><span class="sxs-lookup"><span data-stu-id="495ae-105">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="495ae-106">С помощью нескольких строк XML можно создать только что правом интерфейс для пользователя.</span><span class="sxs-lookup"><span data-stu-id="495ae-106">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="495ae-107">Access предоставляет чрезвычайно гибкие возможности настройки ленты.</span><span class="sxs-lookup"><span data-stu-id="495ae-107">Access provides tremendous flexibility in customizing the ribbon UI.</span></span> <span data-ttu-id="495ae-108">Например разметку для настройки может быть хранятся в таблице, внедренные в процедуре VBA, хранящиеся в другую базу данных Access или по ссылке из листа Excel.</span><span class="sxs-lookup"><span data-stu-id="495ae-108">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="495ae-109">В этом разделе описывается применение настроенной ленты при открытии базы данных.</span><span class="sxs-lookup"><span data-stu-id="495ae-109">This topic describes how to apply customized ribbons when opening a database.</span></span>

## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="495ae-110">Сделать доступными настройки ленты XML</span><span class="sxs-lookup"><span data-stu-id="495ae-110">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="495ae-111">Расширяемость ленты хранилища XML в таблице</span><span class="sxs-lookup"><span data-stu-id="495ae-111">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="495ae-112">— Это один метод, который можно использовать для настройки ленты доступны для их хранения в таблице.</span><span class="sxs-lookup"><span data-stu-id="495ae-112">One method that you can use to make ribbon customizations available is to store them in a table.</span></span> <span data-ttu-id="495ae-113">При сохранении настроек в таблице с именем **USysRibbons**настроек может быть реализовано без с помощью макросов или кода VBA.</span><span class="sxs-lookup"><span data-stu-id="495ae-113">If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="495ae-114">**USysRibbons** — это таблица системы, созданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="495ae-114">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="495ae-115">В таблице должны быть созданы с помощью имена определенных столбцов для настройки ленты для реализации.</span><span class="sxs-lookup"><span data-stu-id="495ae-115">The table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="495ae-116">В следующей таблице перечислены параметры для использования при создании в таблице **USysRibbons** .</span><span class="sxs-lookup"><span data-stu-id="495ae-116">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="495ae-117">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="495ae-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="495ae-118">Тип данных</span><span class="sxs-lookup"><span data-stu-id="495ae-118">Data type</span></span></p></th>
<th><p><span data-ttu-id="495ae-119">Описание</span><span class="sxs-lookup"><span data-stu-id="495ae-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="495ae-120"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="495ae-120"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="495ae-121">Текст</span><span class="sxs-lookup"><span data-stu-id="495ae-121">Text</span></span></p></td>
<td><p><span data-ttu-id="495ae-122">Содержит имя настраиваемой ленты, который будет связан с этой настройкой.</span><span class="sxs-lookup"><span data-stu-id="495ae-122">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="495ae-123"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="495ae-123"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="495ae-124">Заметка</span><span class="sxs-lookup"><span data-stu-id="495ae-124">Memo</span></span></p></td>
<td><p><span data-ttu-id="495ae-125">Содержит расширяемость ленты XML (RibbonX), который определяет настройки ленты.</span><span class="sxs-lookup"><span data-stu-id="495ae-125">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="495ae-126">Загрузить расширения ленты XML программным путем</span><span class="sxs-lookup"><span data-stu-id="495ae-126">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="495ae-127">Можно использовать метод **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** для загрузки настроек ленты программными средствами.</span><span class="sxs-lookup"><span data-stu-id="495ae-127">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically.</span></span> <span data-ttu-id="495ae-128">Как правило чтобы создать и становится доступной для приложения ленты, сначала создайте модуль в базе данных с помощью процедуры, вызывающий метод **LoadCustomUI** , передавая имя ленты и разметки XML для настройки.</span><span class="sxs-lookup"><span data-stu-id="495ae-128">Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="495ae-129">XML-разметка могут поступать из объекта **набора записей** , созданных из таблицы, из источника, внешними по отношению к базы данных, например XML-файл, который проанализировать в строку или из XML-разметка внедрена непосредственно в процедуру.</span><span class="sxs-lookup"><span data-stu-id="495ae-129">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure.</span></span> <span data-ttu-id="495ae-130">Можно выполнять различные ленты с помощью нескольких звонков на метод **LoadCustomUI** , передав в различных XML-разметка, поскольку имя каждой ленты и вкладки, которые составляют ленты для атрибута **id** — уникальный.</span><span class="sxs-lookup"><span data-stu-id="495ae-130">You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="495ae-131">После завершения процедуры нажмите Создать макрос AutoExec, который вызывает процедуру с использованием действием RunCode.</span><span class="sxs-lookup"><span data-stu-id="495ae-131">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="495ae-132">Таким образом, при запуске приложения метод **LoadCustomUI** выполняется автоматически и все настраиваемые ленты доступны для приложения.</span><span class="sxs-lookup"><span data-stu-id="495ae-132">That way, when the application is started, the **LoadCustomUI** method is automatically executed, and all of the custom ribbons are made available to the application.</span></span>

## <a name="apply-customized-ribbons-when-access-starts"></a><span data-ttu-id="495ae-133">Применение настроенной ленты при запуске Access</span><span class="sxs-lookup"><span data-stu-id="495ae-133">Apply customized ribbons when Access starts</span></span>

<span data-ttu-id="495ae-134">Для применения настраиваемых элементов пользовательского интерфейса, чтобы оно доступно при запуске приложения, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="495ae-134">To apply a custom UI so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="495ae-135">Выполните действия, описанные выше, чтобы сделать настроенные ленты доступными для приложения.</span><span class="sxs-lookup"><span data-stu-id="495ae-135">Follow the process described previously to make the customized ribbons available to the application.</span></span>

2.  <span data-ttu-id="495ae-136">Закройте и перезапустите приложение.</span><span class="sxs-lookup"><span data-stu-id="495ae-136">Close and then restart the application.</span></span>

3.  <span data-ttu-id="495ae-137">Нажмите **Кнопку Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") и выберите пункт **Параметры доступа**.</span><span class="sxs-lookup"><span data-stu-id="495ae-137">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="495ae-138">Выберите параметр **Текущей базы данных** и затем в разделе **ленты и параметры панели инструментов** выберите в списке **Имя ленты** и ленты.</span><span class="sxs-lookup"><span data-stu-id="495ae-138">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select a ribbon.</span></span>

5.  <span data-ttu-id="495ae-139">Теперь закройте и перезапустите приложение.</span><span class="sxs-lookup"><span data-stu-id="495ae-139">Now close and restart the application.</span></span> <span data-ttu-id="495ae-140">Отображается выбранный Интерфейс.</span><span class="sxs-lookup"><span data-stu-id="495ae-140">The UI you selected is displayed.</span></span>

> [!NOTE]
> <span data-ttu-id="495ae-141">Дополнительные сведения о пользовательский Интерфейс ленты в других приложениях Office можно [Обзор ленты Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="495ae-141">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


