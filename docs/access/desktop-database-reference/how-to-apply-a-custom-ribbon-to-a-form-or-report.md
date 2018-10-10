---
title: Применение настраиваемой ленты в форму или отчет
TOCTitle: Apply a custom ribbon to a form or report
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4fb0155b1a1ed36b6fe924f72a4da385197cc21
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482357"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a><span data-ttu-id="245d0-102">Применение настраиваемой ленты в форму или отчет</span><span class="sxs-lookup"><span data-stu-id="245d0-102">Apply a custom ribbon to a form or report</span></span>


<span data-ttu-id="245d0-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="245d0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="245d0-104">Ленты использует текстовую декларативную разметку XML, упрощающую создание и настройку ленты.</span><span class="sxs-lookup"><span data-stu-id="245d0-104">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="245d0-105">С помощью нескольких строк XML можно создать только что правом интерфейс для пользователя.</span><span class="sxs-lookup"><span data-stu-id="245d0-105">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="245d0-106">Access обеспечивает гибкость при настройке пользовательского интерфейса ленты.</span><span class="sxs-lookup"><span data-stu-id="245d0-106">Access provides flexibility in customizing the ribbon user interface.</span></span> <span data-ttu-id="245d0-107">Например разметку для настройки может быть хранятся в таблице, внедренные в процедуре VBA, хранящиеся в другую базу данных Access или по ссылке из листа Excel.</span><span class="sxs-lookup"><span data-stu-id="245d0-107">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="245d0-108">В этом разделе описывается применение настроенной ленты при загрузке формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="245d0-108">This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="making-the-ribbon-customization-xml-available"></a><span data-ttu-id="245d0-109">Предоставление XML настройки ленты</span><span class="sxs-lookup"><span data-stu-id="245d0-109">Making the Ribbon Customization XML Available</span></span>

<span data-ttu-id="245d0-110">**Хранение расширяемость ленты XML в таблице**</span><span class="sxs-lookup"><span data-stu-id="245d0-110">**Storing Ribbon Extensibility XML in a Table**</span></span>

<span data-ttu-id="245d0-111">— Это один метод, который можно использовать для настройки ленты доступны для их хранения в таблице.</span><span class="sxs-lookup"><span data-stu-id="245d0-111">One method that you can use to make ribbon customizations available is to store them in a table.</span></span> <span data-ttu-id="245d0-112">При сохранении настроек в таблице с именем **USysRibbons**настроек может быть реализовано без с помощью макросов или кода VBA.</span><span class="sxs-lookup"><span data-stu-id="245d0-112">If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="245d0-113">**USysRibbons** — это таблица системы, созданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="245d0-113">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="245d0-114">В таблице должны быть созданы с помощью имена определенных столбцов в порядке для настройки ленты для реализации.</span><span class="sxs-lookup"><span data-stu-id="245d0-114">The table must be created using specific column names in order for the ribbon customizations to be implemented.</span></span> <span data-ttu-id="245d0-115">В следующей таблице перечислены параметры для использования при создании в таблице **USysRibbons** .</span><span class="sxs-lookup"><span data-stu-id="245d0-115">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="245d0-116">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="245d0-116">Column Name</span></span></p></th>
<th><p><span data-ttu-id="245d0-117">Тип данных</span><span class="sxs-lookup"><span data-stu-id="245d0-117">Data Type</span></span></p></th>
<th><p><span data-ttu-id="245d0-118">Описание</span><span class="sxs-lookup"><span data-stu-id="245d0-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="245d0-119"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="245d0-119"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="245d0-120">Текст</span><span class="sxs-lookup"><span data-stu-id="245d0-120">Text</span></span></p></td>
<td><p><span data-ttu-id="245d0-121">Содержит имя настраиваемой ленты, который будет связан с этой настройкой</span><span class="sxs-lookup"><span data-stu-id="245d0-121">Contains the name of the custom ribbon to be associated with this customization</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="245d0-122"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="245d0-122"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="245d0-123">Заметка</span><span class="sxs-lookup"><span data-stu-id="245d0-123">Memo</span></span></p></td>
<td><p><span data-ttu-id="245d0-124">Содержит расширения XML-кодом ленты (RibbonX), который определяет настройки ленты</span><span class="sxs-lookup"><span data-stu-id="245d0-124">Contains the ribbon Extensibility XML (RibbonX) that defines the ribbon customization</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="245d0-125">**Загрузка расширяемость XML ленты программными средствами**</span><span class="sxs-lookup"><span data-stu-id="245d0-125">**Loading Ribbon Extensibility XML Programmatically**</span></span>

<span data-ttu-id="245d0-126">Можно использовать метод **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** для загрузки настроек ленты программными средствами.</span><span class="sxs-lookup"><span data-stu-id="245d0-126">You can use the **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** method to load ribbon customizations programmatically.</span></span> <span data-ttu-id="245d0-127">Как правило чтобы создать и становится доступной для приложения ленты, сначала создайте модуль в базе данных с помощью процедуры, вызывающий метод **LoadCustomUI** , передавая имя ленты и разметки XML для настройки.</span><span class="sxs-lookup"><span data-stu-id="245d0-127">Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="245d0-128">XML-разметка могут поступать из объекта **набора записей** , созданных из таблицы, из источника, внешними по отношению к базы данных, например XML-файл, который проанализировать в строку или из XML-разметка внедрена непосредственно в процедуру.</span><span class="sxs-lookup"><span data-stu-id="245d0-128">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure.</span></span> <span data-ttu-id="245d0-129">Можно выполнять различные ленты с помощью нескольких звонков на метод **LoadCustomUI** , передав в различных XML-разметка, поскольку имя каждой ленты и вкладки, которые составляют ленты для атрибута **id** — уникальный.</span><span class="sxs-lookup"><span data-stu-id="245d0-129">You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="245d0-130">После завершения процедуры нажмите Создать макрос AutoExec, который вызывает процедуру с использованием действием RunCode.</span><span class="sxs-lookup"><span data-stu-id="245d0-130">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="245d0-131">Таким образом, при запуске приложения метод **LoadCustomUI** выполняется автоматически и все настраиваемые ленты доступны для приложения.</span><span class="sxs-lookup"><span data-stu-id="245d0-131">That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="assigning-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="245d0-132">Назначение настраиваемой ленты для форм и отчетов</span><span class="sxs-lookup"><span data-stu-id="245d0-132">Assigning Custom Ribbons to Forms or Reports</span></span>

1.  <span data-ttu-id="245d0-133">Выполните действия, описанные выше, чтобы сделать доступным для приложения настраиваемой ленты.</span><span class="sxs-lookup"><span data-stu-id="245d0-133">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="245d0-134">Откройте форму или отчет в режиме конструктора.</span><span class="sxs-lookup"><span data-stu-id="245d0-134">Open the form or report in Design view.</span></span>

3.  <span data-ttu-id="245d0-135">На вкладке "Конструктор" нажмите кнопку **Свойств**.</span><span class="sxs-lookup"><span data-stu-id="245d0-135">On the Design tab, click **Property Sheet**.</span></span>

4.  <span data-ttu-id="245d0-136">На вкладке **все** окна Свойства выберите в списке **Имя ленты** и выберите ленты.</span><span class="sxs-lookup"><span data-stu-id="245d0-136">On the **All** tab of the Property window, click the **Ribbon Name** list and then select a ribbon.</span></span>

5.  <span data-ttu-id="245d0-137">Сохраните, закройте и снова откройте форму или отчет.</span><span class="sxs-lookup"><span data-stu-id="245d0-137">Save, close, and then reopen the form or report.</span></span> <span data-ttu-id="245d0-138">Отображается пользовательский Интерфейс, выбранный ленты.</span><span class="sxs-lookup"><span data-stu-id="245d0-138">The ribbon UI you selected is displayed.</span></span>


> [!NOTE]
> <span data-ttu-id="245d0-139">Вкладки на ленте пользовательского интерфейса-дополнительная.</span><span class="sxs-lookup"><span data-stu-id="245d0-139">The tabs displayed in the ribbon UI are additive.</span></span> <span data-ttu-id="245d0-140">То есть до специально скрытия вкладки или *с самого начала* атрибуту присваивается **значение True**, вкладки отображаются в форме или пользовательского интерфейса ленты отчета, в дополнение к существующих вкладок.</span><span class="sxs-lookup"><span data-stu-id="245d0-140">That is, unless you specifically hide the tabs or set the *Start from Scratch* attribute to **True**, the tabs displayed in a form's or report's ribbon user interface are in addition to the existing tabs.</span></span>

> [!NOTE]
> <span data-ttu-id="245d0-141">Дополнительные сведения о пользовательский Интерфейс ленты в других приложениях Office можно [Обзор ленты Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="245d0-141">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


