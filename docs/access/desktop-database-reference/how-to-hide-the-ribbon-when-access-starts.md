---
<span data-ttu-id="fa2cb-101">Заголовок: скрытие ленты при запуске Access TOCTitle: скрытие ленты при запуске Access <<<<<<< HEAD ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 09/18/2015 === Описание: загрузка настраиваемой ленты, который скрывает все встроенной вкладки в Access 2013.</span><span class="sxs-lookup"><span data-stu-id="fa2cb-101">title: Hide the ribbon when Access starts TOCTitle: Hide the ribbon when Access starts <<<<<<< HEAD ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 09/18/2015 ======= description: How to load a customized ribbon that hides all of the built-in tabs in Access 2013.</span></span>
<span data-ttu-id="fa2cb-102">MS:AssetId: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 10/16/2018</span><span class="sxs-lookup"><span data-stu-id="fa2cb-102">ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="fa2cb-103">главные mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="fa2cb-103">master mtps_version: v=office.15</span></span>
---

# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="fa2cb-104">Скрытие ленты при запуске Access</span><span class="sxs-lookup"><span data-stu-id="fa2cb-104">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="fa2cb-105">**Применимо к:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa2cb-105">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="fa2cb-106">По умолчанию Microsoft Access не предоставляет метод для скрытия на ленте.</span><span class="sxs-lookup"><span data-stu-id="fa2cb-106">By default, Microsoft Access does not provide a method for hiding the ribbon.</span></span> <span data-ttu-id="fa2cb-107">В этом разделе описывается, как загрузить настраиваемой ленты, который скрывает все встроенной вкладки.</span><span class="sxs-lookup"><span data-stu-id="fa2cb-107">This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="fa2cb-108">Чтобы загрузить настраиваемой ленты при запуске Access, следует хранить его параметры в таблице с именем **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="fa2cb-108">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="fa2cb-109"><<<<<<< В таблице **USysRibbons** должны создаваться с помощью имена определенных столбцов в порядке для настройки ленты для реализации HEAD.</span><span class="sxs-lookup"><span data-stu-id="fa2cb-109"><<<<<<< HEAD The **USysRibbons** table must be created using specific column names in order for the ribbon customizations to be implemented.</span></span> <span data-ttu-id="fa2cb-110">В следующей таблице перечислены параметры для использования при создании в таблице **USysRibbons** .</span><span class="sxs-lookup"><span data-stu-id="fa2cb-110">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
<span data-ttu-id="fa2cb-111">=== В таблице **USysRibbons** должны быть созданы с помощью имена определенных столбцов для настройки ленты для реализации.</span><span class="sxs-lookup"><span data-stu-id="fa2cb-111">======= The **USysRibbons** table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="fa2cb-112">В следующей таблице перечислены параметры для использования при создании в таблице **USysRibbons** .</span><span class="sxs-lookup"><span data-stu-id="fa2cb-112">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
>>>>>>> <span data-ttu-id="fa2cb-113">master</span><span class="sxs-lookup"><span data-stu-id="fa2cb-113">master</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<span data-ttu-id="fa2cb-114"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="fa2cb-114"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="fa2cb-115">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="fa2cb-115">Column Name</span></span></p></th>
<th><p><span data-ttu-id="fa2cb-116">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fa2cb-116">Data Type</span></span></p></th>
=======
<th><p><span data-ttu-id="fa2cb-117">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="fa2cb-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="fa2cb-118">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fa2cb-118">Data type</span></span></p></th><span data-ttu-id="fa2cb-119">
>>>>>>>Образец</span><span class="sxs-lookup"><span data-stu-id="fa2cb-119">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="fa2cb-120">Описание</span><span class="sxs-lookup"><span data-stu-id="fa2cb-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa2cb-121"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="fa2cb-121"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="fa2cb-122">Текст</span><span class="sxs-lookup"><span data-stu-id="fa2cb-122">Text</span></span></p></td>
<td><p><span data-ttu-id="fa2cb-123">Содержит имя настраиваемой ленты, который будет связан с этой настройкой.</span><span class="sxs-lookup"><span data-stu-id="fa2cb-123">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa2cb-124"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="fa2cb-124"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="fa2cb-125">Заметка</span><span class="sxs-lookup"><span data-stu-id="fa2cb-125">Memo</span></span></p></td>
<span data-ttu-id="fa2cb-126"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="fa2cb-126"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="fa2cb-127">Содержит XML расширяемости ленты (RibbonX), который определяет настройки ленты.</span><span class="sxs-lookup"><span data-stu-id="fa2cb-127">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
=======
<td><p><span data-ttu-id="fa2cb-128">Содержит расширяемость ленты XML (RibbonX), который определяет настройки ленты.</span><span class="sxs-lookup"><span data-stu-id="fa2cb-128">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td><span data-ttu-id="fa2cb-129">
>>>>>>>Образец</span><span class="sxs-lookup"><span data-stu-id="fa2cb-129">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>

<span data-ttu-id="fa2cb-130"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="fa2cb-130"><<<<<<< HEAD</span></span>

<span data-ttu-id="fa2cb-131">В следующей таблице перечислены параметры настройки ленты для хранения в таблице **USysRibbons** .</span><span class="sxs-lookup"><span data-stu-id="fa2cb-131">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa2cb-132">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="fa2cb-132">Column Name</span></span></p></th>
<th><p><span data-ttu-id="fa2cb-133">Значение</span><span class="sxs-lookup"><span data-stu-id="fa2cb-133">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa2cb-134"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="fa2cb-134"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="fa2cb-135">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="fa2cb-135">HideTheRibbon</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa2cb-136"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="fa2cb-136"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="fa2cb-137">&lt;CustomUI xmlns =&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot; &gt; &lt;ленты startFromScratch =&quot;значение true,&quot;/&gt;&lt;/CustomUI&gt;</span><span class="sxs-lookup"><span data-stu-id="fa2cb-137">&lt;CustomUI xmlns=&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot;&gt; &lt;ribbon startFromScratch=&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="applying-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="fa2cb-138">Применение настраиваемой ленты при запуске Access</span><span class="sxs-lookup"><span data-stu-id="fa2cb-138">Applying a Custom Ribbon When Access Starts</span></span>
=======
<br/>

<span data-ttu-id="fa2cb-139">В следующей таблице перечислены параметры настройки ленты для хранения в таблице **USysRibbons** .</span><span class="sxs-lookup"><span data-stu-id="fa2cb-139">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

|<span data-ttu-id="fa2cb-140">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="fa2cb-140">Column name</span></span>|<span data-ttu-id="fa2cb-141">Значение</span><span class="sxs-lookup"><span data-stu-id="fa2cb-141">Value</span></span>|
|:----------|:----|
|<span data-ttu-id="fa2cb-142">**RibbonName**</span><span class="sxs-lookup"><span data-stu-id="fa2cb-142">**RibbonName**</span></span>|<span data-ttu-id="fa2cb-143">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="fa2cb-143">HideTheRibbon</span></span>|
|<span data-ttu-id="fa2cb-144">**RibbonXML**</span><span class="sxs-lookup"><span data-stu-id="fa2cb-144">**RibbonXML**</span></span>|`<CustomUI xmlns="https://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="fa2cb-145">Применение настраиваемой ленты при запуске Access</span><span class="sxs-lookup"><span data-stu-id="fa2cb-145">Apply a custom ribbon when Access starts</span></span>
>>>>>>> <span data-ttu-id="fa2cb-146">master</span><span class="sxs-lookup"><span data-stu-id="fa2cb-146">master</span></span>

<span data-ttu-id="fa2cb-147">Чтобы применить настраиваемой ленты, чтобы оно доступно при запуске приложения, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="fa2cb-147">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="fa2cb-148">Выполните действия, описанные выше, чтобы сделать доступным для приложения настраиваемой ленты.</span><span class="sxs-lookup"><span data-stu-id="fa2cb-148">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="fa2cb-149">Закройте и перезапустите приложение.</span><span class="sxs-lookup"><span data-stu-id="fa2cb-149">Close and then restart the application.</span></span>

<span data-ttu-id="fa2cb-150"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="fa2cb-150"><<<<<<< HEAD</span></span>
3.  <span data-ttu-id="fa2cb-151">Нажмите **Кнопку Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") и нажмите кнопку **Параметры Access**.</span><span class="sxs-lookup"><span data-stu-id="fa2cb-151">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="fa2cb-152">Выберите параметр **Текущей базы данных** , а затем, в разделе **ленты и параметры панели инструментов** выберите в списке **Имя ленты** и выберите **HideTheRibbon**.</span><span class="sxs-lookup"><span data-stu-id="fa2cb-152">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select **HideTheRibbon**.</span></span>
=======
3.  <span data-ttu-id="fa2cb-153">Нажмите **Кнопку Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), а затем выберите **Параметры доступа**.</span><span class="sxs-lookup"><span data-stu-id="fa2cb-153">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="fa2cb-154">Выберите параметр **Текущей базы данных** и затем в разделе **ленты и параметры панели инструментов** выберите в списке **Имя ленты** и **HideTheRibbon**.</span><span class="sxs-lookup"><span data-stu-id="fa2cb-154">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select **HideTheRibbon**.</span></span>
>>>>>>> <span data-ttu-id="fa2cb-155">master</span><span class="sxs-lookup"><span data-stu-id="fa2cb-155">master</span></span>

5.  <span data-ttu-id="fa2cb-156">Закройте и перезапустите приложение.</span><span class="sxs-lookup"><span data-stu-id="fa2cb-156">Close and then restart the application.</span></span>

> [!NOTE]
> <span data-ttu-id="fa2cb-157">Дополнительные сведения о пользовательский Интерфейс ленты в других приложениях Office можно [Обзор ленты Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="fa2cb-157">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


