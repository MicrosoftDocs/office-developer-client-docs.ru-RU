---
title: Скрытие ленты при запуске Access
TOCTitle: Hide the ribbon when Access starts
description: Узнайте, как загрузить в Access 2013 настроенную ленту, на которой скрыты все встроенные вкладки.
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 4ce9327790f620ba9163f5cdbe7b5c8900de4341
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704107"
---
# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="f26be-103">Скрытие ленты при запуске Access</span><span class="sxs-lookup"><span data-stu-id="f26be-103">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="f26be-104">**Область применения**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f26be-104">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="f26be-105">По умолчанию Microsoft Access не предоставляет метод для скрытия ленты.</span><span class="sxs-lookup"><span data-stu-id="f26be-105">By default, Microsoft Access does not provide a method for hiding the ribbon.</span></span> <span data-ttu-id="f26be-106">В этой статье описывается, как загрузить пользовательскую ленту, на которой скрыты все встроенные вкладки.</span><span class="sxs-lookup"><span data-stu-id="f26be-106">This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="f26be-107">Чтобы загрузить пользовательскую ленту при запуске Access, необходимо сохранить ее параметры в таблице с именем **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="f26be-107">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="f26be-108">Таблицу **USysRibbons** необходимо создать с использованием конкретных имен столбцов для реализуемых настроек ленты.</span><span class="sxs-lookup"><span data-stu-id="f26be-108">The **USysRibbons** table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="f26be-109">В приведенной ниже таблице перечислены параметры, используемые при создании таблицы **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="f26be-109">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f26be-110">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="f26be-110">Column name</span></span></p></th>
<th><p><span data-ttu-id="f26be-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f26be-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="f26be-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f26be-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f26be-113"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="f26be-113"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="f26be-114">Текст</span><span class="sxs-lookup"><span data-stu-id="f26be-114">Text</span></span></p></td>
<td><p><span data-ttu-id="f26be-115">Содержит имя пользовательской ленты, которая будет связана с этой настройкой.</span><span class="sxs-lookup"><span data-stu-id="f26be-115">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f26be-116"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="f26be-116"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="f26be-117">Заметка</span><span class="sxs-lookup"><span data-stu-id="f26be-117">Memo</span></span></p></td>
<td><p><span data-ttu-id="f26be-118">Содержит код XML для расширения ленты (RibbonX), определяющий настройку ленты.</span><span class="sxs-lookup"><span data-stu-id="f26be-118">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="f26be-119">В приведенной ниже таблице перечислены параметры для настройки ленты, которые будут храниться в таблице **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="f26be-119">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

|<span data-ttu-id="f26be-120">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="f26be-120">Column name</span></span>|<span data-ttu-id="f26be-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f26be-121">Value</span></span>|
|:----------|:----|
|<span data-ttu-id="f26be-122">**RibbonName**</span><span class="sxs-lookup"><span data-stu-id="f26be-122">**RibbonName**</span></span>|<span data-ttu-id="f26be-123">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="f26be-123">HideTheRibbon</span></span>|
|<span data-ttu-id="f26be-124">**RibbonXML**</span><span class="sxs-lookup"><span data-stu-id="f26be-124">**RibbonXML**</span></span>|`<CustomUI xmlns="https://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="f26be-125">Применение пользовательской ленты при запуске Access</span><span class="sxs-lookup"><span data-stu-id="f26be-125">Apply a custom ribbon when starting Access</span></span>

<span data-ttu-id="f26be-126">Чтобы применить пользовательскую ленту, которая будет доступна при запуске приложения, используйте описанную ниже процедуру.</span><span class="sxs-lookup"><span data-stu-id="f26be-126">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="f26be-127">Выполните описанные выше действия, чтобы сделать настроенную ленту доступной приложению.</span><span class="sxs-lookup"><span data-stu-id="f26be-127">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="f26be-128">Закройте и перезапустите приложение.</span><span class="sxs-lookup"><span data-stu-id="f26be-128">Close and restart the Office application.</span></span>

3.  <span data-ttu-id="f26be-129">Нажмите **кнопку Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") и выберите пункт **Параметры Access**.</span><span class="sxs-lookup"><span data-stu-id="f26be-129">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="f26be-130">Выберите вариант **Текущая база данных**, а затем в разделе **Параметры ленты и панелей инструментов** выберите список **Имя ленты** и нажмите **HideTheRibbon**.</span><span class="sxs-lookup"><span data-stu-id="f26be-130">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select **HideTheRibbon**.</span></span>

5.  <span data-ttu-id="f26be-131">Закройте и перезапустите приложение.</span><span class="sxs-lookup"><span data-stu-id="f26be-131">Close and restart the Office application.</span></span>

> [!NOTE]
> <span data-ttu-id="f26be-132">Дополнительные сведения о пользовательском интерфейсе ленты в других приложениях Office см. в статье [Обзор ленты Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="f26be-132">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


