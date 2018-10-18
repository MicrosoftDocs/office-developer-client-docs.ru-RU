---
<span data-ttu-id="b3035-101">Заголовок: применение настраиваемой ленты при запуске TOCTitle доступа: применение настраиваемой ленты при запуске Access <<<<<<< HEAD ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15) ms:contentKeyID: 48546659 ms.date: 09/18 / 2015 === Описание: применение настроенной ленты при открытии базы данных в Access 2013.</span><span class="sxs-lookup"><span data-stu-id="b3035-101">title: Apply a custom ribbon when starting Access TOCTitle: Apply a custom ribbon when starting Access <<<<<<< HEAD ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15) ms:contentKeyID: 48546659 ms.date: 09/18/2015 ======= description: How to apply customized ribbons when opening a database in Access 2013.</span></span> <span data-ttu-id="b3035-102">MS:AssetId: 9e8ddf95-35aa-4e57-8422-d770da14711e ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15) ms:contentKeyID: 48546659 ms.date: 10/16/2018</span><span class="sxs-lookup"><span data-stu-id="b3035-102">ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15) ms:contentKeyID: 48546659 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="b3035-103">главные mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="b3035-103">master mtps_version: v=office.15</span></span>
---

# <a name="apply-a-custom-ribbon-when-starting-access"></a><span data-ttu-id="b3035-104">Применение настраиваемой ленты при запуске Access</span><span class="sxs-lookup"><span data-stu-id="b3035-104">Apply a custom ribbon when starting Access</span></span>

<span data-ttu-id="b3035-105">**Применимо к:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3035-105">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="b3035-106">Ленты использует текстовую декларативную разметку XML, упрощающую создание и настройку ленты.</span><span class="sxs-lookup"><span data-stu-id="b3035-106">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="b3035-107">С помощью нескольких строк XML можно создать только что правом интерфейс для пользователя.</span><span class="sxs-lookup"><span data-stu-id="b3035-107">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="b3035-108">Access предоставляет чрезвычайно гибкие возможности настройки ленты.</span><span class="sxs-lookup"><span data-stu-id="b3035-108">Access provides tremendous flexibility in customizing the ribbon UI.</span></span> <span data-ttu-id="b3035-109">Например разметку для настройки может быть хранятся в таблице, внедренные в процедуре VBA, хранящиеся в другую базу данных Access или по ссылке из листа Excel.</span><span class="sxs-lookup"><span data-stu-id="b3035-109">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="b3035-110">В этом разделе описывается применение настроенной ленты при открытии базы данных.</span><span class="sxs-lookup"><span data-stu-id="b3035-110">This topic describes how to apply customized ribbons when opening a database.</span></span>

<span data-ttu-id="b3035-111"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="b3035-111"><<<<<<< HEAD</span></span>
## <a name="making-the-ribbon-customization-xml-available"></a><span data-ttu-id="b3035-112">Предоставление XML настройки ленты</span><span class="sxs-lookup"><span data-stu-id="b3035-112">Making the Ribbon Customization XML Available</span></span>

### <a name="storing-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="b3035-113">Хранение расширяемость ленты XML в таблице</span><span class="sxs-lookup"><span data-stu-id="b3035-113">Storing Ribbon Extensibility XML in a Table</span></span>

<span data-ttu-id="b3035-114">— Это один метод, который можно использовать для настройки ленты доступны для их хранения в таблице.</span><span class="sxs-lookup"><span data-stu-id="b3035-114">One method that you can use to make ribbon customizations available is to store them in a table.</span></span> <span data-ttu-id="b3035-115">При сохранении настроек в таблице с именем **USysRibbons**настроек может быть реализовано без с помощью макросов или кода VBA.</span><span class="sxs-lookup"><span data-stu-id="b3035-115">If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<a name="usysribbons-is-a-user-created-system-table-the-table-must-be-created-using-specific-column-names-in-order-for-the-ribbon-customizations-to-be-implemented-the-following-table-lists-the-settings-to-use-when-creating-the-usysribbons-table"></a><span data-ttu-id="b3035-116">**USysRibbons** — это таблица системы, созданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="b3035-116">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="b3035-117">В таблице должны быть созданы с помощью имена определенных столбцов в порядке для настройки ленты для реализации.</span><span class="sxs-lookup"><span data-stu-id="b3035-117">The table must be created using specific column names in order for the ribbon customizations to be implemented.</span></span> <span data-ttu-id="b3035-118">В следующей таблице перечислены параметры для использования при создании в таблице **USysRibbons** .</span><span class="sxs-lookup"><span data-stu-id="b3035-118">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
=======
## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="b3035-119">Сделать доступными настройки ленты XML</span><span class="sxs-lookup"><span data-stu-id="b3035-119">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="b3035-120">Расширяемость ленты хранилища XML в таблице</span><span class="sxs-lookup"><span data-stu-id="b3035-120">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="b3035-121">— Это один метод, который можно использовать для настройки ленты доступны для их хранения в таблице.</span><span class="sxs-lookup"><span data-stu-id="b3035-121">One method that you can use to make ribbon customizations available is to store them in a table.</span></span> <span data-ttu-id="b3035-122">При сохранении настроек в таблице с именем **USysRibbons**настроек может быть реализовано без с помощью макросов или кода VBA.</span><span class="sxs-lookup"><span data-stu-id="b3035-122">If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="b3035-123">**USysRibbons** — это таблица системы, созданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="b3035-123">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="b3035-124">В таблице должны быть созданы с помощью имена определенных столбцов для настройки ленты для реализации.</span><span class="sxs-lookup"><span data-stu-id="b3035-124">The table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="b3035-125">В следующей таблице перечислены параметры для использования при создании в таблице **USysRibbons** .</span><span class="sxs-lookup"><span data-stu-id="b3035-125">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
>>>>>>> <span data-ttu-id="b3035-126">master</span><span class="sxs-lookup"><span data-stu-id="b3035-126">master</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<span data-ttu-id="b3035-127"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="b3035-127"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="b3035-128">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="b3035-128">Column Name</span></span></p></th>
<th><p><span data-ttu-id="b3035-129">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b3035-129">Data Type</span></span></p></th>
=======
<th><p><span data-ttu-id="b3035-130">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="b3035-130">Column name</span></span></p></th>
<th><p><span data-ttu-id="b3035-131">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b3035-131">Data type</span></span></p></th><span data-ttu-id="b3035-132">
>>>>>>>Образец</span><span class="sxs-lookup"><span data-stu-id="b3035-132">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="b3035-133">Описание</span><span class="sxs-lookup"><span data-stu-id="b3035-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3035-134"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="b3035-134"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="b3035-135">Текст</span><span class="sxs-lookup"><span data-stu-id="b3035-135">Text</span></span></p></td>
<td><p><span data-ttu-id="b3035-136">Содержит имя настраиваемой ленты, который будет связан с этой настройкой.</span><span class="sxs-lookup"><span data-stu-id="b3035-136">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3035-137"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="b3035-137"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="b3035-138">Заметка</span><span class="sxs-lookup"><span data-stu-id="b3035-138">Memo</span></span></p></td>
<span data-ttu-id="b3035-139"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="b3035-139"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="b3035-140">Содержит XML расширяемости ленты (RibbonX), который определяет настройки ленты.</span><span class="sxs-lookup"><span data-stu-id="b3035-140">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
=======
<td><p><span data-ttu-id="b3035-141">Содержит расширяемость ленты XML (RibbonX), который определяет настройки ленты.</span><span class="sxs-lookup"><span data-stu-id="b3035-141">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td><span data-ttu-id="b3035-142">
>>>>>>>Образец</span><span class="sxs-lookup"><span data-stu-id="b3035-142">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>


<span data-ttu-id="b3035-143"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="b3035-143"><<<<<<< HEAD</span></span>
### <a name="loading-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="b3035-144">Загрузка расширяемость XML ленты программными средствами</span><span class="sxs-lookup"><span data-stu-id="b3035-144">Loading Ribbon Extensibility XML Programmatically</span></span>

<span data-ttu-id="b3035-145">Можно использовать метод **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** для загрузки настроек ленты программными средствами.</span><span class="sxs-lookup"><span data-stu-id="b3035-145">You can use the **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** method to load ribbon customizations programmatically.</span></span> <span data-ttu-id="b3035-146">Как правило чтобы создать и становится доступной для приложения ленты, сначала создайте модуль в базе данных с помощью процедуры, вызывающий метод **LoadCustomUI** , передавая имя ленты и разметки XML для настройки.</span><span class="sxs-lookup"><span data-stu-id="b3035-146">Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="b3035-147">XML-разметка могут поступать из объекта **набора записей** , созданных из таблицы, из источника, внешними по отношению к базы данных, например XML-файл, который проанализировать в строку или из XML-разметка внедрена непосредственно в процедуру.</span><span class="sxs-lookup"><span data-stu-id="b3035-147">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure.</span></span> <span data-ttu-id="b3035-148">Можно выполнять различные ленты с помощью нескольких звонков на метод **LoadCustomUI** , передав в различных XML-разметка, поскольку имя каждой ленты и вкладки, которые составляют ленты для атрибута **id** — уникальный.</span><span class="sxs-lookup"><span data-stu-id="b3035-148">You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="b3035-149">После завершения процедуры нажмите Создать макрос AutoExec, который вызывает процедуру с использованием действием RunCode.</span><span class="sxs-lookup"><span data-stu-id="b3035-149">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="b3035-150">Таким образом, при запуске приложения метод **LoadCustomUI** выполняется автоматически и все настраиваемые ленты доступны для приложения.</span><span class="sxs-lookup"><span data-stu-id="b3035-150">That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="applying-customized-ribbons-when-access-starts"></a><span data-ttu-id="b3035-151">Применение настроенной ленты при запуске Access</span><span class="sxs-lookup"><span data-stu-id="b3035-151">Applying Customized Ribbons When Access Starts</span></span>
=======
### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="b3035-152">Загрузить расширения ленты XML программным путем</span><span class="sxs-lookup"><span data-stu-id="b3035-152">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="b3035-153">Можно использовать метод **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** для загрузки настроек ленты программными средствами.</span><span class="sxs-lookup"><span data-stu-id="b3035-153">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically.</span></span> <span data-ttu-id="b3035-154">Как правило чтобы создать и становится доступной для приложения ленты, сначала создайте модуль в базе данных с помощью процедуры, вызывающий метод **LoadCustomUI** , передавая имя ленты и разметки XML для настройки.</span><span class="sxs-lookup"><span data-stu-id="b3035-154">Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="b3035-155">XML-разметка могут поступать из объекта **набора записей** , созданных из таблицы, из источника, внешними по отношению к базы данных, например XML-файл, который проанализировать в строку или из XML-разметка внедрена непосредственно в процедуру.</span><span class="sxs-lookup"><span data-stu-id="b3035-155">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure.</span></span> <span data-ttu-id="b3035-156">Можно выполнять различные ленты с помощью нескольких звонков на метод **LoadCustomUI** , передав в различных XML-разметка, поскольку имя каждой ленты и вкладки, которые составляют ленты для атрибута **id** — уникальный.</span><span class="sxs-lookup"><span data-stu-id="b3035-156">You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="b3035-157">После завершения процедуры нажмите Создать макрос AutoExec, который вызывает процедуру с использованием действием RunCode.</span><span class="sxs-lookup"><span data-stu-id="b3035-157">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="b3035-158">Таким образом, при запуске приложения метод **LoadCustomUI** выполняется автоматически и все настраиваемые ленты доступны для приложения.</span><span class="sxs-lookup"><span data-stu-id="b3035-158">That way, when the application is started, the **LoadCustomUI** method is automatically executed, and all of the custom ribbons are made available to the application.</span></span>

## <a name="apply-customized-ribbons-when-access-starts"></a><span data-ttu-id="b3035-159">Применение настроенной ленты при запуске Access</span><span class="sxs-lookup"><span data-stu-id="b3035-159">Apply customized ribbons when Access starts</span></span>
>>>>>>> <span data-ttu-id="b3035-160">master</span><span class="sxs-lookup"><span data-stu-id="b3035-160">master</span></span>

<span data-ttu-id="b3035-161">Для применения настраиваемых элементов пользовательского интерфейса, чтобы оно доступно при запуске приложения, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="b3035-161">To apply a custom UI so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="b3035-162">Выполните действия, описанные выше, чтобы сделать настроенные ленты доступными для приложения.</span><span class="sxs-lookup"><span data-stu-id="b3035-162">Follow the process described previously to make the customized ribbons available to the application.</span></span>

2.  <span data-ttu-id="b3035-163">Закройте и перезапустите приложение.</span><span class="sxs-lookup"><span data-stu-id="b3035-163">Close and then restart the application.</span></span>

<span data-ttu-id="b3035-164"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="b3035-164"><<<<<<< HEAD</span></span>
3.  <span data-ttu-id="b3035-165">Нажмите **Кнопку Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") и нажмите кнопку **Параметры Access**.</span><span class="sxs-lookup"><span data-stu-id="b3035-165">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="b3035-166">Выберите параметр **Текущей базы данных** , а затем, в разделе **ленты и параметры панели инструментов** выберите в списке **Имя ленты** и выберите ленты.</span><span class="sxs-lookup"><span data-stu-id="b3035-166">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select a ribbon.</span></span>
=======
3.  <span data-ttu-id="b3035-167">Нажмите **Кнопку Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") и выберите пункт **Параметры доступа**.</span><span class="sxs-lookup"><span data-stu-id="b3035-167">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="b3035-168">Выберите параметр **Текущей базы данных** и затем в разделе **ленты и параметры панели инструментов** выберите в списке **Имя ленты** и ленты.</span><span class="sxs-lookup"><span data-stu-id="b3035-168">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select a ribbon.</span></span>
>>>>>>> <span data-ttu-id="b3035-169">master</span><span class="sxs-lookup"><span data-stu-id="b3035-169">master</span></span>

5.  <span data-ttu-id="b3035-170">Теперь закройте и перезапустите приложение.</span><span class="sxs-lookup"><span data-stu-id="b3035-170">Now close and restart the application.</span></span> <span data-ttu-id="b3035-171">Отображается выбранный Интерфейс.</span><span class="sxs-lookup"><span data-stu-id="b3035-171">The UI you selected is displayed.</span></span>

> [!NOTE]
> <span data-ttu-id="b3035-172">Дополнительные сведения о пользовательский Интерфейс ленты в других приложениях Office можно [Обзор ленты Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="b3035-172">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


