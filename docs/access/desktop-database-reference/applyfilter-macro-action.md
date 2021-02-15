---
title: Макрокоманда ApplyFilter
TOCTitle: ApplyFilter macro action
ms:assetid: c63988c4-4506-cc51-98f7-478d1f3fe668
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823130(v=office.15)
ms:contentKeyID: 48547623
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm79035
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e79ab56778f9429e7f1a985f0f81864ae4363606
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296999"
---
# <a name="applyfilter-macro-action"></a><span data-ttu-id="05cf3-102">Макрокоманда ApplyFilter</span><span class="sxs-lookup"><span data-stu-id="05cf3-102">ApplyFilter macro action</span></span>

<span data-ttu-id="05cf3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="05cf3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="05cf3-104">Действие **ApplyFilter** можно использовать для применения фильтра, запроса или предложения SQL WHERE к таблице, форме или отчету, чтобы ограничить или отсортировать записи в таблице или записях из таблицы или запроса формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="05cf3-104">You can use the **ApplyFilter** action to apply a filter, a query, or an SQL WHERE clause to a table, form, or report to restrict or sort the records in the table, or the records from the underlying table or query of the form or report.</span></span> <span data-ttu-id="05cf3-105">Для отчетов это действие можно использовать только в макросах, указанных свойством события **OnOpen** отчета.</span><span class="sxs-lookup"><span data-stu-id="05cf3-105">For reports, you can use this action only in a macro specified by the report's **OnOpen** event property.</span></span>

> [!NOTE]
> <span data-ttu-id="05cf3-106">Это действие можно использовать для применения SQL WHERE только при применении фильтра сервера.</span><span class="sxs-lookup"><span data-stu-id="05cf3-106">You can use this action to apply an SQL WHERE clause only when applying a server filter.</span></span> <span data-ttu-id="05cf3-107">К источнику записей хранимой процедуры нельзя применить фильтр сервера.</span><span class="sxs-lookup"><span data-stu-id="05cf3-107">A server filter cannot be applied to a stored procedure's record source.</span></span>

## <a name="setting"></a><span data-ttu-id="05cf3-108">Setting</span><span class="sxs-lookup"><span data-stu-id="05cf3-108">Setting</span></span>

<span data-ttu-id="05cf3-109">Действие **ApplyFilter** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="05cf3-109">The **ApplyFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05cf3-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="05cf3-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="05cf3-111">Описание</span><span class="sxs-lookup"><span data-stu-id="05cf3-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05cf3-112">Имя фильтра</span><span class="sxs-lookup"><span data-stu-id="05cf3-112">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="05cf3-113">Имя фильтра или запроса, ограничивающего или сортировать записи таблицы, формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="05cf3-113">The name of a filter or query that restricts or sorts the records of the table, form, or report.</span></span> <span data-ttu-id="05cf3-114">Можно ввести имя существующего запроса или фильтра, сохраненного <strong></strong> в качестве запроса, в поле "Имя фильтра" в разделе "Аргументы действий" области <strong></strong> <strong>построитель</strong> макроса.</span><span class="sxs-lookup"><span data-stu-id="05cf3-114">You can enter the name of either an existing query or a filter that has been saved as a query in the <strong>Filter Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane.</span></span></p><p><span data-ttu-id="05cf3-115"><strong>ПРИМЕЧАНИЕ.</strong>При использовании этого действия для применения фильтра сервера аргумент "Имя фильтра" должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="05cf3-115"><strong>NOTE</strong>: When you are using this action to apply a server filter, the Filter Name argument must be blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05cf3-116">Where Condition</span><span class="sxs-lookup"><span data-stu-id="05cf3-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="05cf3-117">Допустимый SQL WHERE (без слова WHERE) или выражение, ограничивающее записи таблицы, формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="05cf3-117">A valid SQL WHERE clause (without the word WHERE) or an expression that restricts the records of the table, form, or report.</span></span></p>
<p><span data-ttu-id="05cf3-118"><b>ПРИМЕЧАНИЕ.</b>В выражении аргумента Where Condition левая сторона выражения обычно содержит имя поля из таблицы или запроса формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="05cf3-118"><b>NOTE</b>: In a Where Condition argument expression, the left side of the expression typically contains a field name from the underlying table or query for the form or report.</span></span> <span data-ttu-id="05cf3-119">Правая сторона выражения обычно содержит критерии, которые необходимо применить к этому полю для ограничения или сортировки записей.</span><span class="sxs-lookup"><span data-stu-id="05cf3-119">The right side of the expression typically contains the criteria you want to apply to this field to restrict or sort the records.</span></span> <span data-ttu-id="05cf3-120">Например, критерием может быть имя управления в другой форме, содержа содержа которое должно совпадать со значениями, которые должны соответствовать записям в первой форме.</span><span class="sxs-lookup"><span data-stu-id="05cf3-120">For example, the criteria can be the name of a control on another form that contains the value you want the records in the first form to match.</span></span> <span data-ttu-id="05cf3-121">Имя этого управления должно быть полностью квалифицировано, например:</span><span class="sxs-lookup"><span data-stu-id="05cf3-121">The name of the control should be fully qualified, for example:</span></span></p>
<p><span data-ttu-id="05cf3-122"><strong>Формы!</strong> <em>formname</em>! <em>controlname</em> Имена полей должны быть окружяться двойными кавычками, а строки литералов должны быть окружяться одиночными кавычками.</span><span class="sxs-lookup"><span data-stu-id="05cf3-122"><strong>Forms</strong>!<em>formname</em>!<em>controlname</em> Field names should be surrounded by double quotation marks and string literals should be surrounded by single quotation marks.</span></span> <span data-ttu-id="05cf3-123">Максимальная длина аргумента Where Condition составляет 255 символов.</span><span class="sxs-lookup"><span data-stu-id="05cf3-123">The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="05cf3-124">Если требуется ввести более SQL where, используйте метод <strong>ApplyFilter</strong> объекта <strong>DoCmd</strong> в модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="05cf3-124">If you need to enter a longer SQL WHERE clause, use the <strong>ApplyFilter</strong> method of the <strong>DoCmd</strong> object in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="05cf3-125">В VBA SQL ввести заявления о предложении WHERE до 32 768 символов.</span><span class="sxs-lookup"><span data-stu-id="05cf3-125">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="05cf3-126">Аргумент "Имя фильтра" можно использовать, если вы уже определили фильтр, который предоставляет соответствующие данные.</span><span class="sxs-lookup"><span data-stu-id="05cf3-126">You can use the Filter Name argument if you have already defined a filter that provides the appropriate data.</span></span> <span data-ttu-id="05cf3-127">Вы можете использовать аргумент Where Condition, чтобы ввести критерии ограничения напрямую.</span><span class="sxs-lookup"><span data-stu-id="05cf3-127">You can use the Where Condition argument to enter the restriction criteria directly.</span></span> <span data-ttu-id="05cf3-128">Если вы используете оба аргумента, Microsoft Office Access 2007 применяет предложение WHERE к результатам фильтра.</span><span class="sxs-lookup"><span data-stu-id="05cf3-128">If you use both arguments, Microsoft Office Access 2007 applies the WHERE clause to the results of the filter.</span></span> <span data-ttu-id="05cf3-129">Необходимо использовать один или оба аргумента.</span><span class="sxs-lookup"><span data-stu-id="05cf3-129">You must use one or both arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="05cf3-130">Заметки</span><span class="sxs-lookup"><span data-stu-id="05cf3-130">Remarks</span></span>

<span data-ttu-id="05cf3-131">Вы можете применить фильтр или запрос к форме в представлении формы или в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="05cf3-131">You can apply a filter or query to a form in Form view or Datasheet view.</span></span>

<span data-ttu-id="05cf3-132">Применяемое условие фильтра и WHERE становится параметром свойства **Filter** или **ServerFilter** формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="05cf3-132">The filter and WHERE condition you apply become the setting of the form's or report's **Filter** or **ServerFilter** property.</span></span>

<span data-ttu-id="05cf3-133">Для таблиц и форм это действие аналогично нажатию кнопки **"Применить фильтр",** "Сортировка" или "Применить **серверный фильтр"** в меню **"Записи".**</span><span class="sxs-lookup"><span data-stu-id="05cf3-133">For tables and forms, this action is similar to clicking **Apply Filter/Sort** or **Apply Server Filter** on the **Records** menu.</span></span> <span data-ttu-id="05cf3-134">Команда меню применяет к таблице или форме последний созданный фильтр, а действие **ApplyFilter** применяет указанный фильтр или запрос.</span><span class="sxs-lookup"><span data-stu-id="05cf3-134">The menu command applies the most recently created filter to the table or form, whereas the **ApplyFilter** action applies a specified filter or query.</span></span>

<span data-ttu-id="05cf3-135">Если в базе данных Access  после  запуска действия **ApplyFilter** нажать кнопку "Фильтр" в меню "Записи", а затем щелкнуть "Расширенный **фильтр/сортировка",** в окне "Расширенный фильтр/сортировка" будут показаны критерии фильтра, выбранные с помощью этого действия.</span><span class="sxs-lookup"><span data-stu-id="05cf3-135">In an Access database, if you point to **Filter** on the **Records** menu and then click **Advanced Filter/Sort** after running the **ApplyFilter** action, the Advanced Filter/Sort window shows the filter criteria you have selected with this action.</span></span>

<span data-ttu-id="05cf3-136">Чтобы удалить фильтр и отобразить все записи для таблицы или формы в базе данных Office Access 2007, можно использовать  действие **ShowAllRecords** или команду "Удалить **фильтр/сортировку"** в меню "Записи".</span><span class="sxs-lookup"><span data-stu-id="05cf3-136">To remove a filter and display all of the records for a table or form in an Office Access 2007 database, you can use the **ShowAllRecords** action or the **Remove Filter/Sort** command on the **Records** menu.</span></span> <span data-ttu-id="05cf3-137">Чтобы удалить фильтр в проекте Access (ADP), можно вернуться в окно "Фильтр сервера  по форме"  и удалить все критерии фильтрации, а затем щелкнуть "Применить фильтр сервера" в меню "Записи" на панели инструментов или установить для свойства **ServerFilterByForm** свойство **False** (0).</span><span class="sxs-lookup"><span data-stu-id="05cf3-137">To remove a filter in an Access project (.adp), you can return to the Server Filter By Form window and remove all filter criteria and then click **Apply Server Filter** on the **Records** menu on the toolbar, or set the **ServerFilterByForm** property to **False** (0).</span></span>

<span data-ttu-id="05cf3-138">При сохранения таблицы или формы Access сохраняет любой фильтр, определенный в настоящее время в этом объекте, но не применяет его автоматически при следующем открытом объекте (хотя он автоматически применяет любую сортировку, примененную к объекту до его сохранения).</span><span class="sxs-lookup"><span data-stu-id="05cf3-138">When you save a table or form, Access saves any filter currently defined in that object, but won't apply the filter automatically the next time the object is opened (although it will automatically apply any sort you applied to the object before it was saved).</span></span> <span data-ttu-id="05cf3-139">Если вы хотите применить фильтр автоматически при первом открытие формы, укажите макрос, содержащий действие **ApplyFilter** или процедуру события, содержащую метод **ApplyFilter** объекта **DoCmd** в качестве параметра свойства события **OnOpen** формы.</span><span class="sxs-lookup"><span data-stu-id="05cf3-139">If you want to apply a filter automatically when a form is first opened, specify a macro containing the **ApplyFilter** action or an event procedure containing the **ApplyFilter** method of the **DoCmd** object as the **OnOpen** event property setting of the form.</span></span> <span data-ttu-id="05cf3-140">Вы также можете применить фильтр с помощью действия **OpenForm** или **OpenReport** или соответствующих им методов.</span><span class="sxs-lookup"><span data-stu-id="05cf3-140">You can also apply a filter by using the **OpenForm** or **OpenReport** action, or their corresponding methods.</span></span> <span data-ttu-id="05cf3-141">Чтобы автоматически применить фильтр при первом открытие таблицы, можно открыть таблицу с помощью макроса, содержащего действие **OpenTable,** а затем сразу же последует действие **ApplyFilter.**</span><span class="sxs-lookup"><span data-stu-id="05cf3-141">To apply a filter automatically when a table is first opened, you can open the table by using a macro containing the **OpenTable** action, followed immediately by the **ApplyFilter** action.</span></span>

## <a name="example"></a><span data-ttu-id="05cf3-142">Пример</span><span class="sxs-lookup"><span data-stu-id="05cf3-142">Example</span></span>

<span data-ttu-id="05cf3-143">В следующем примере показано, как использовать действие ApplyFilter для фильтрации формы frmFoods при ее открытие.</span><span class="sxs-lookup"><span data-stu-id="05cf3-143">The following example shows how to use the ApplyFilter action to filter the frmFoods form as it is opened.</span></span>

<span data-ttu-id="05cf3-144">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="05cf3-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    ApplyFilter
        Filter Name
        Where Condition=[display_name] Link "*cheese*"
        Control Name
```



