---
title: Применение настраиваемой ленты при запуске Access
TOCTitle: Apply a custom ribbon when starting Access
ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15)
ms:contentKeyID: 48546659
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 575834f818386a7ba536e826fff2b7da00b324d5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483280"
---
# <a name="apply-a-custom-ribbon-when-starting-access"></a><span data-ttu-id="2cc4b-102">Применение настраиваемой ленты при запуске Access</span><span class="sxs-lookup"><span data-stu-id="2cc4b-102">Apply a custom ribbon when starting Access</span></span>

<span data-ttu-id="2cc4b-103">**Применимо к:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2cc4b-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="2cc4b-104">Ленты использует текстовую декларативную разметку XML, упрощающую создание и настройку ленты.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-104">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="2cc4b-105">С помощью нескольких строк XML можно создать только что правом интерфейс для пользователя.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-105">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="2cc4b-106">Access предоставляет чрезвычайно гибкие возможности настройки ленты.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-106">Access provides tremendous flexibility in customizing the ribbon UI.</span></span> <span data-ttu-id="2cc4b-107">Например разметку для настройки может быть хранятся в таблице, внедренные в процедуре VBA, хранящиеся в другую базу данных Access или по ссылке из листа Excel.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-107">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="2cc4b-108">В этом разделе описывается применение настроенной ленты при открытии базы данных.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-108">This topic describes how to apply customized ribbons when opening a database.</span></span>

## <a name="making-the-ribbon-customization-xml-available"></a><span data-ttu-id="2cc4b-109">Предоставление XML настройки ленты</span><span class="sxs-lookup"><span data-stu-id="2cc4b-109">Making the Ribbon Customization XML Available</span></span>

### <a name="storing-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="2cc4b-110">Хранение расширяемость ленты XML в таблице</span><span class="sxs-lookup"><span data-stu-id="2cc4b-110">Storing Ribbon Extensibility XML in a Table</span></span>

<span data-ttu-id="2cc4b-111">— Это один метод, который можно использовать для настройки ленты доступны для их хранения в таблице.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-111">One method that you can use to make ribbon customizations available is to store them in a table.</span></span> <span data-ttu-id="2cc4b-112">При сохранении настроек в таблице с именем **USysRibbons**настроек может быть реализовано без с помощью макросов или кода VBA.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-112">If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="2cc4b-113">**USysRibbons** — это таблица системы, созданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-113">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="2cc4b-114">В таблице должны быть созданы с помощью имена определенных столбцов в порядке для настройки ленты для реализации.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-114">The table must be created using specific column names in order for the ribbon customizations to be implemented.</span></span> <span data-ttu-id="2cc4b-115">В следующей таблице перечислены параметры для использования при создании в таблице **USysRibbons** .</span><span class="sxs-lookup"><span data-stu-id="2cc4b-115">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2cc4b-116">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="2cc4b-116">Column Name</span></span></p></th>
<th><p><span data-ttu-id="2cc4b-117">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2cc4b-117">Data Type</span></span></p></th>
<th><p><span data-ttu-id="2cc4b-118">Описание</span><span class="sxs-lookup"><span data-stu-id="2cc4b-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cc4b-119"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="2cc4b-119"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="2cc4b-120">Текст</span><span class="sxs-lookup"><span data-stu-id="2cc4b-120">Text</span></span></p></td>
<td><p><span data-ttu-id="2cc4b-121">Содержит имя настраиваемой ленты, который будет связан с этой настройкой.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-121">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cc4b-122"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="2cc4b-122"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="2cc4b-123">Заметка</span><span class="sxs-lookup"><span data-stu-id="2cc4b-123">Memo</span></span></p></td>
<td><p><span data-ttu-id="2cc4b-124">Содержит XML расширяемости ленты (RibbonX), который определяет настройки ленты.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-124">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="loading-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="2cc4b-125">Загрузка расширяемость XML ленты программными средствами</span><span class="sxs-lookup"><span data-stu-id="2cc4b-125">Loading Ribbon Extensibility XML Programmatically</span></span>

<span data-ttu-id="2cc4b-126">Можно использовать метод **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** для загрузки настроек ленты программными средствами.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-126">You can use the **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** method to load ribbon customizations programmatically.</span></span> <span data-ttu-id="2cc4b-127">Как правило чтобы создать и становится доступной для приложения ленты, сначала создайте модуль в базе данных с помощью процедуры, вызывающий метод **LoadCustomUI** , передавая имя ленты и разметки XML для настройки.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-127">Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="2cc4b-128">XML-разметка могут поступать из объекта **набора записей** , созданных из таблицы, из источника, внешними по отношению к базы данных, например XML-файл, который проанализировать в строку или из XML-разметка внедрена непосредственно в процедуру.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-128">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure.</span></span> <span data-ttu-id="2cc4b-129">Можно выполнять различные ленты с помощью нескольких звонков на метод **LoadCustomUI** , передав в различных XML-разметка, поскольку имя каждой ленты и вкладки, которые составляют ленты для атрибута **id** — уникальный.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-129">You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="2cc4b-130">После завершения процедуры нажмите Создать макрос AutoExec, который вызывает процедуру с использованием действием RunCode.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-130">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="2cc4b-131">Таким образом, при запуске приложения метод **LoadCustomUI** выполняется автоматически и все настраиваемые ленты доступны для приложения.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-131">That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="applying-customized-ribbons-when-access-starts"></a><span data-ttu-id="2cc4b-132">Применение настроенной ленты при запуске Access</span><span class="sxs-lookup"><span data-stu-id="2cc4b-132">Applying Customized Ribbons When Access Starts</span></span>

<span data-ttu-id="2cc4b-133">Для применения настраиваемых элементов пользовательского интерфейса, чтобы оно доступно при запуске приложения, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="2cc4b-133">To apply a custom UI so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="2cc4b-134">Выполните действия, описанные выше, чтобы сделать настроенные ленты доступными для приложения.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-134">Follow the process described previously to make the customized ribbons available to the application.</span></span>

2.  <span data-ttu-id="2cc4b-135">Закройте и перезапустите приложение.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-135">Close and then restart the application.</span></span>

3.  <span data-ttu-id="2cc4b-136">Нажмите **Кнопку Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") и нажмите кнопку **Параметры Access**.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-136">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="2cc4b-137">Выберите параметр **Текущей базы данных** , а затем, в разделе **ленты и параметры панели инструментов** выберите в списке **Имя ленты** и выберите ленты.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-137">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select a ribbon.</span></span>

5.  <span data-ttu-id="2cc4b-138">Теперь закройте и перезапустите приложение.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-138">Now close and restart the application.</span></span> <span data-ttu-id="2cc4b-139">Отображается выбранный Интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-139">The UI you selected is displayed.</span></span>

> [!NOTE]
> <span data-ttu-id="2cc4b-140">Дополнительные сведения о пользовательский Интерфейс ленты в других приложениях Office можно [Обзор ленты Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="2cc4b-140">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


