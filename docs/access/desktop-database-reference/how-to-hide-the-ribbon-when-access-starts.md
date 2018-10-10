---
title: Скрытие ленты при запуске Access
TOCTitle: Hide the ribbon when Access starts
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b2b3e28157662a585fa03353da92a598b96bd2c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480437"
---
# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="721ba-102">Скрытие ленты при запуске Access</span><span class="sxs-lookup"><span data-stu-id="721ba-102">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="721ba-103">**Применимо к:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="721ba-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="721ba-104">По умолчанию Microsoft Access не предоставляет метод для скрытия на ленте.</span><span class="sxs-lookup"><span data-stu-id="721ba-104">By default, Microsoft Access does not provide a method for hiding the ribbon.</span></span> <span data-ttu-id="721ba-105">В этом разделе описывается, как загрузить настраиваемой ленты, который скрывает все встроенной вкладки.</span><span class="sxs-lookup"><span data-stu-id="721ba-105">This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="721ba-106">Чтобы загрузить настраиваемой ленты при запуске Access, следует хранить его параметры в таблице с именем **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="721ba-106">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="721ba-107">В таблице **USysRibbons** должны быть созданы с помощью имена определенных столбцов в порядке для настройки ленты для реализации.</span><span class="sxs-lookup"><span data-stu-id="721ba-107">The **USysRibbons** table must be created using specific column names in order for the ribbon customizations to be implemented.</span></span> <span data-ttu-id="721ba-108">В следующей таблице перечислены параметры для использования при создании в таблице **USysRibbons** .</span><span class="sxs-lookup"><span data-stu-id="721ba-108">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="721ba-109">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="721ba-109">Column Name</span></span></p></th>
<th><p><span data-ttu-id="721ba-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="721ba-110">Data Type</span></span></p></th>
<th><p><span data-ttu-id="721ba-111">Описание</span><span class="sxs-lookup"><span data-stu-id="721ba-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="721ba-112"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="721ba-112"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="721ba-113">Текст</span><span class="sxs-lookup"><span data-stu-id="721ba-113">Text</span></span></p></td>
<td><p><span data-ttu-id="721ba-114">Содержит имя настраиваемой ленты, который будет связан с этой настройкой.</span><span class="sxs-lookup"><span data-stu-id="721ba-114">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="721ba-115"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="721ba-115"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="721ba-116">Заметка</span><span class="sxs-lookup"><span data-stu-id="721ba-116">Memo</span></span></p></td>
<td><p><span data-ttu-id="721ba-117">Содержит XML расширяемости ленты (RibbonX), который определяет настройки ленты.</span><span class="sxs-lookup"><span data-stu-id="721ba-117">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="721ba-118">В следующей таблице перечислены параметры настройки ленты для хранения в таблице **USysRibbons** .</span><span class="sxs-lookup"><span data-stu-id="721ba-118">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="721ba-119">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="721ba-119">Column Name</span></span></p></th>
<th><p><span data-ttu-id="721ba-120">Значение</span><span class="sxs-lookup"><span data-stu-id="721ba-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="721ba-121"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="721ba-121"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="721ba-122">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="721ba-122">HideTheRibbon</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="721ba-123"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="721ba-123"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="721ba-124">&lt;CustomUI xmlns =&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot; &gt; &lt;ленты startFromScratch =&quot;значение true,&quot;/&gt;&lt;/CustomUI&gt;</span><span class="sxs-lookup"><span data-stu-id="721ba-124">&lt;CustomUI xmlns=&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot;&gt; &lt;ribbon startFromScratch=&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="applying-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="721ba-125">Применение настраиваемой ленты при запуске Access</span><span class="sxs-lookup"><span data-stu-id="721ba-125">Applying a Custom Ribbon When Access Starts</span></span>

<span data-ttu-id="721ba-126">Чтобы применить настраиваемой ленты, чтобы оно доступно при запуске приложения, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="721ba-126">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="721ba-127">Выполните действия, описанные выше, чтобы сделать доступным для приложения настраиваемой ленты.</span><span class="sxs-lookup"><span data-stu-id="721ba-127">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="721ba-128">Закройте и перезапустите приложение.</span><span class="sxs-lookup"><span data-stu-id="721ba-128">Close and then restart the application.</span></span>

3.  <span data-ttu-id="721ba-129">Нажмите **Кнопку Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") и нажмите кнопку **Параметры Access**.</span><span class="sxs-lookup"><span data-stu-id="721ba-129">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="721ba-130">Выберите параметр **Текущей базы данных** , а затем, в разделе **ленты и параметры панели инструментов** выберите в списке **Имя ленты** и выберите **HideTheRibbon**.</span><span class="sxs-lookup"><span data-stu-id="721ba-130">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select **HideTheRibbon**.</span></span>

5.  <span data-ttu-id="721ba-131">Закройте и перезапустите приложение.</span><span class="sxs-lookup"><span data-stu-id="721ba-131">Close and then restart the application.</span></span>

> [!NOTE]
> <span data-ttu-id="721ba-132">Дополнительные сведения о пользовательский Интерфейс ленты в других приложениях Office можно [Обзор ленты Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="721ba-132">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


