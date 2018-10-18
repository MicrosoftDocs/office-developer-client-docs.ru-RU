---
<span data-ttu-id="1c134-101">Заголовок: применение настраиваемой ленты в форму или отчет TOCTitle: применение настраиваемой ленты в форму или отчет <<<<<<< HEAD ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: 48545865 ms.date: 09/18/2015 === === Описание: применение настроенной ленты при загрузке формы или отчета в Access 2013.</span><span class="sxs-lookup"><span data-stu-id="1c134-101">title: Apply a custom ribbon to a form or report TOCTitle: Apply a custom ribbon to a form or report <<<<<<< HEAD ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: 48545865 ms.date: 09/18/2015 ======= description: How to apply customized ribbons when loading a form or report in Access 2013.</span></span>
<span data-ttu-id="1c134-102">MS:AssetId: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: 48545865 ms.date: 10/16/2018</span><span class="sxs-lookup"><span data-stu-id="1c134-102">ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: 48545865 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="1c134-103">главные mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="1c134-103">master mtps_version: v=office.15</span></span>
---

# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a><span data-ttu-id="1c134-104">Применение настраиваемой ленты в форму или отчет</span><span class="sxs-lookup"><span data-stu-id="1c134-104">Apply a custom ribbon to a form or report</span></span>

<span data-ttu-id="1c134-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="1c134-105"><<<<<<< HEAD</span></span>

<span data-ttu-id="1c134-106">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c134-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1c134-107">Ленты использует текстовую декларативную разметку XML, упрощающую создание и настройку ленты.</span><span class="sxs-lookup"><span data-stu-id="1c134-107">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="1c134-108">С помощью нескольких строк XML можно создать только что правом интерфейс для пользователя.</span><span class="sxs-lookup"><span data-stu-id="1c134-108">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="1c134-109">Access обеспечивает гибкость при настройке пользовательского интерфейса ленты.</span><span class="sxs-lookup"><span data-stu-id="1c134-109">Access provides flexibility in customizing the ribbon user interface.</span></span> <span data-ttu-id="1c134-110">Например разметку для настройки может быть хранятся в таблице, внедренные в процедуре VBA, хранящиеся в другую базу данных Access или по ссылке из листа Excel.</span><span class="sxs-lookup"><span data-stu-id="1c134-110">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="1c134-111">В этом разделе описывается применение настроенной ленты при загрузке формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="1c134-111">This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="making-the-ribbon-customization-xml-available"></a><span data-ttu-id="1c134-112">Предоставление XML настройки ленты</span><span class="sxs-lookup"><span data-stu-id="1c134-112">Making the Ribbon Customization XML Available</span></span>

<span data-ttu-id="1c134-113">**Хранение расширяемость ленты XML в таблице**</span><span class="sxs-lookup"><span data-stu-id="1c134-113">**Storing Ribbon Extensibility XML in a Table**</span></span>

<span data-ttu-id="1c134-114">— Это один метод, который можно использовать для настройки ленты доступны для их хранения в таблице.</span><span class="sxs-lookup"><span data-stu-id="1c134-114">One method that you can use to make ribbon customizations available is to store them in a table.</span></span> <span data-ttu-id="1c134-115">При сохранении настроек в таблице с именем **USysRibbons**настроек может быть реализовано без с помощью макросов или кода VBA.</span><span class="sxs-lookup"><span data-stu-id="1c134-115">If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<a name="usysribbons-is-a-user-created-system-table-the-table-must-be-created-using-specific-column-names-in-order-for-the-ribbon-customizations-to-be-implemented-the-following-table-lists-the-settings-to-use-when-creating-the-usysribbons-table"></a><span data-ttu-id="1c134-116">**USysRibbons** — это таблица системы, созданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="1c134-116">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="1c134-117">В таблице должны быть созданы с помощью имена определенных столбцов в порядке для настройки ленты для реализации.</span><span class="sxs-lookup"><span data-stu-id="1c134-117">The table must be created using specific column names in order for the ribbon customizations to be implemented.</span></span> <span data-ttu-id="1c134-118">В следующей таблице перечислены параметры для использования при создании в таблице **USysRibbons** .</span><span class="sxs-lookup"><span data-stu-id="1c134-118">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
=======
<span data-ttu-id="1c134-119">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c134-119">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1c134-120">Ленты использует текстовую декларативную разметку XML, упрощающую создание и настройку ленты.</span><span class="sxs-lookup"><span data-stu-id="1c134-120">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="1c134-121">С помощью нескольких строк XML можно создать только что правом интерфейс для пользователя.</span><span class="sxs-lookup"><span data-stu-id="1c134-121">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="1c134-122">Access обеспечивает гибкость при настройке пользовательского интерфейса ленты.</span><span class="sxs-lookup"><span data-stu-id="1c134-122">Access provides flexibility in customizing the ribbon user interface.</span></span> 

<span data-ttu-id="1c134-123">Например разметку для настройки может быть хранятся в таблице, внедренные в процедуре VBA, хранящиеся в другую базу данных Access или по ссылке из листа Excel.</span><span class="sxs-lookup"><span data-stu-id="1c134-123">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="1c134-124">В этом разделе описывается применение настроенной ленты при загрузке формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="1c134-124">This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="1c134-125">Сделать доступными настройки ленты XML</span><span class="sxs-lookup"><span data-stu-id="1c134-125">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="1c134-126">Расширяемость ленты хранилища XML в таблице</span><span class="sxs-lookup"><span data-stu-id="1c134-126">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="1c134-127">— Это один метод, который можно использовать для настройки ленты доступны для их хранения в таблице.</span><span class="sxs-lookup"><span data-stu-id="1c134-127">One method that you can use to make ribbon customizations available is to store them in a table.</span></span> <span data-ttu-id="1c134-128">При сохранении настроек в таблице с именем **USysRibbons**настроек может быть реализовано без с помощью макросов или кода VBA.</span><span class="sxs-lookup"><span data-stu-id="1c134-128">If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="1c134-129">**USysRibbons** — это таблица системы, созданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="1c134-129">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="1c134-130">В таблице должны быть созданы с помощью имена определенных столбцов для настройки ленты для реализации.</span><span class="sxs-lookup"><span data-stu-id="1c134-130">The table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="1c134-131">В следующей таблице перечислены параметры для использования при создании в таблице **USysRibbons** .</span><span class="sxs-lookup"><span data-stu-id="1c134-131">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
>>>>>>> <span data-ttu-id="1c134-132">master</span><span class="sxs-lookup"><span data-stu-id="1c134-132">master</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<span data-ttu-id="1c134-133"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="1c134-133"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="1c134-134">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="1c134-134">Column Name</span></span></p></th>
<th><p><span data-ttu-id="1c134-135">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1c134-135">Data Type</span></span></p></th>
=======
<th><p><span data-ttu-id="1c134-136">Имя столбца</span><span class="sxs-lookup"><span data-stu-id="1c134-136">Column name</span></span></p></th>
<th><p><span data-ttu-id="1c134-137">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1c134-137">Data type</span></span></p></th><span data-ttu-id="1c134-138">
>>>>>>>Образец</span><span class="sxs-lookup"><span data-stu-id="1c134-138">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="1c134-139">Описание</span><span class="sxs-lookup"><span data-stu-id="1c134-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c134-140"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="1c134-140"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="1c134-141">Текст</span><span class="sxs-lookup"><span data-stu-id="1c134-141">Text</span></span></p></td>
<span data-ttu-id="1c134-142"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="1c134-142"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="1c134-143">Содержит имя настраиваемой ленты, который будет связан с этой настройкой</span><span class="sxs-lookup"><span data-stu-id="1c134-143">Contains the name of the custom ribbon to be associated with this customization</span></span></p></td>
=======
<td><p><span data-ttu-id="1c134-144">Содержит имя настраиваемой ленты, который будет связан с этой настройкой.</span><span class="sxs-lookup"><span data-stu-id="1c134-144">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td><span data-ttu-id="1c134-145">
>>>>>>>Образец</span><span class="sxs-lookup"><span data-stu-id="1c134-145">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c134-146"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="1c134-146"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="1c134-147">Заметка</span><span class="sxs-lookup"><span data-stu-id="1c134-147">Memo</span></span></p></td>
<span data-ttu-id="1c134-148"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="1c134-148"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="1c134-149">Содержит расширения XML-кодом ленты (RibbonX), который определяет настройки ленты</span><span class="sxs-lookup"><span data-stu-id="1c134-149">Contains the ribbon Extensibility XML (RibbonX) that defines the ribbon customization</span></span></p></td>
=======
<td><p><span data-ttu-id="1c134-150">Содержит расширяемость ленты XML (RibbonX), который определяет настройки ленты.</span><span class="sxs-lookup"><span data-stu-id="1c134-150">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td><span data-ttu-id="1c134-151">
>>>>>>>Образец</span><span class="sxs-lookup"><span data-stu-id="1c134-151">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>


<span data-ttu-id="1c134-152"><<<<<<< HEAD **Загрузка расширяемость ленты XML программным путем**</span><span class="sxs-lookup"><span data-stu-id="1c134-152"><<<<<<< HEAD **Loading Ribbon Extensibility XML Programmatically**</span></span>

<a name="you-can-use-the-loadcustomuihttpsmsdnmicrosoftcomlibraryff194416voffice15-method-to-load-ribbon-customizations-programmatically-typically-to-create-and-make-the-ribbon-available-to-the-application-you-first-create-a-module-in-the-database-with-a-procedure-that-calls-the-loadcustomui-method-passing-in-the-name-of-the-ribbon-and-the-xml-customization-markup"></a><span data-ttu-id="1c134-153">Можно использовать метод **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** для загрузки настроек ленты программными средствами.</span><span class="sxs-lookup"><span data-stu-id="1c134-153">You can use the **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** method to load ribbon customizations programmatically.</span></span> <span data-ttu-id="1c134-154">Как правило чтобы создать и становится доступной для приложения ленты, сначала создайте модуль в базе данных с помощью процедуры, вызывающий метод **LoadCustomUI** , передавая имя ленты и разметки XML для настройки.</span><span class="sxs-lookup"><span data-stu-id="1c134-154">Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>
=======
### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="1c134-155">Загрузить расширения ленты XML программным путем</span><span class="sxs-lookup"><span data-stu-id="1c134-155">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="1c134-156">Можно использовать метод **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** для загрузки настроек ленты программными средствами.</span><span class="sxs-lookup"><span data-stu-id="1c134-156">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically.</span></span> <span data-ttu-id="1c134-157">Как правило чтобы создать и становится доступной для приложения ленты, сначала создайте модуль в базе данных с помощью процедуры, вызывающий метод **LoadCustomUI** , передавая имя ленты и разметки XML для настройки.</span><span class="sxs-lookup"><span data-stu-id="1c134-157">Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>
>>>>>>> <span data-ttu-id="1c134-158">master</span><span class="sxs-lookup"><span data-stu-id="1c134-158">master</span></span>

<span data-ttu-id="1c134-159">XML-разметка могут поступать из объекта **набора записей** , созданных из таблицы, из источника, внешними по отношению к базы данных, например XML-файл, который проанализировать в строку или из XML-разметка внедрена непосредственно в процедуру.</span><span class="sxs-lookup"><span data-stu-id="1c134-159">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure.</span></span> <span data-ttu-id="1c134-160">Можно выполнять различные ленты с помощью нескольких звонков на метод **LoadCustomUI** , передав в различных XML-разметка, поскольку имя каждой ленты и вкладки, которые составляют ленты для атрибута **id** — уникальный.</span><span class="sxs-lookup"><span data-stu-id="1c134-160">You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="1c134-161">После завершения процедуры нажмите Создать макрос AutoExec, который вызывает процедуру с использованием действием RunCode.</span><span class="sxs-lookup"><span data-stu-id="1c134-161">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="1c134-162">Таким образом, при запуске приложения метод **LoadCustomUI** выполняется автоматически и все настраиваемые ленты доступны для приложения.</span><span class="sxs-lookup"><span data-stu-id="1c134-162">That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

<span data-ttu-id="1c134-163"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="1c134-163"><<<<<<< HEAD</span></span>
## <a name="assigning-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="1c134-164">Назначение настраиваемой ленты для форм и отчетов</span><span class="sxs-lookup"><span data-stu-id="1c134-164">Assigning Custom Ribbons to Forms or Reports</span></span>
=======
## <a name="assign-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="1c134-165">Назначение настраиваемой ленты для форм и отчетов</span><span class="sxs-lookup"><span data-stu-id="1c134-165">Assign custom ribbons to forms or reports</span></span>
>>>>>>> <span data-ttu-id="1c134-166">master</span><span class="sxs-lookup"><span data-stu-id="1c134-166">master</span></span>

1.  <span data-ttu-id="1c134-167">Выполните действия, описанные выше, чтобы сделать доступным для приложения настраиваемой ленты.</span><span class="sxs-lookup"><span data-stu-id="1c134-167">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="1c134-168">Откройте форму или отчет в режиме конструктора.</span><span class="sxs-lookup"><span data-stu-id="1c134-168">Open the form or report in Design view.</span></span>

<span data-ttu-id="1c134-169"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="1c134-169"><<<<<<< HEAD</span></span>
3.  <span data-ttu-id="1c134-170">На вкладке "Конструктор" нажмите кнопку **Свойств**.</span><span class="sxs-lookup"><span data-stu-id="1c134-170">On the Design tab, click **Property Sheet**.</span></span>

4.  <span data-ttu-id="1c134-171">На вкладке **все** окна Свойства выберите в списке **Имя ленты** и выберите ленты.</span><span class="sxs-lookup"><span data-stu-id="1c134-171">On the **All** tab of the Property window, click the **Ribbon Name** list and then select a ribbon.</span></span>
=======
3.  <span data-ttu-id="1c134-172">На вкладке конструктор выберите **Страницы свойств**.</span><span class="sxs-lookup"><span data-stu-id="1c134-172">On the Design tab, choose **Property Sheet**.</span></span>

4.  <span data-ttu-id="1c134-173">На вкладке **все** окна Свойства выберите в списке **Имя ленты** и затем выберите ленты.</span><span class="sxs-lookup"><span data-stu-id="1c134-173">On the **All** tab of the Property window, choose the **Ribbon Name** list and then select a ribbon.</span></span>
>>>>>>> <span data-ttu-id="1c134-174">master</span><span class="sxs-lookup"><span data-stu-id="1c134-174">master</span></span>

5.  <span data-ttu-id="1c134-175">Сохраните, закройте и снова откройте форму или отчет.</span><span class="sxs-lookup"><span data-stu-id="1c134-175">Save, close, and then reopen the form or report.</span></span> <span data-ttu-id="1c134-176">Отображается пользовательский Интерфейс, выбранный ленты.</span><span class="sxs-lookup"><span data-stu-id="1c134-176">The ribbon UI you selected is displayed.</span></span>


> [!NOTE]
> <span data-ttu-id="1c134-177">Вкладки на ленте пользовательского интерфейса-дополнительная.</span><span class="sxs-lookup"><span data-stu-id="1c134-177">The tabs displayed in the ribbon UI are additive.</span></span> <span data-ttu-id="1c134-178">То есть до специально скрытия вкладки или *с самого начала* атрибуту присваивается **значение True**, вкладки отображаются в форме или пользовательского интерфейса ленты отчета, в дополнение к существующих вкладок.</span><span class="sxs-lookup"><span data-stu-id="1c134-178">That is, unless you specifically hide the tabs or set the *Start from Scratch* attribute to **True**, the tabs displayed in a form's or report's ribbon user interface are in addition to the existing tabs.</span></span>

> [!NOTE]
> <span data-ttu-id="1c134-179">Дополнительные сведения о пользовательский Интерфейс ленты в других приложениях Office можно [Обзор ленты Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="1c134-179">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


