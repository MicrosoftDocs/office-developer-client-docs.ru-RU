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
# <a name="applyfilter-macro-action"></a><span data-ttu-id="8539d-102">Макрокоманда ApplyFilter</span><span class="sxs-lookup"><span data-stu-id="8539d-102">ApplyFilter macro action</span></span>

<span data-ttu-id="8539d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8539d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8539d-104">Действие **ApplyFilter** можно использовать для применения фильтра, запроса или положения SQL WHERE к таблице, форме или отчету для ограничения или сортировки записей в таблице или записей из таблицы или запроса формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="8539d-104">You can use the **ApplyFilter** action to apply a filter, a query, or an SQL WHERE clause to a table, form, or report to restrict or sort the records in the table, or the records from the underlying table or query of the form or report.</span></span> <span data-ttu-id="8539d-105">Для отчетов это действие можно использовать только в макросе, указанном свойством **событий OnOpen** отчета.</span><span class="sxs-lookup"><span data-stu-id="8539d-105">For reports, you can use this action only in a macro specified by the report's **OnOpen** event property.</span></span>

> [!NOTE]
> <span data-ttu-id="8539d-106">Это действие можно использовать для применения пункта SQL WHERE только при применении фильтра сервера.</span><span class="sxs-lookup"><span data-stu-id="8539d-106">You can use this action to apply an SQL WHERE clause only when applying a server filter.</span></span> <span data-ttu-id="8539d-107">Серверный фильтр не может применяться к источнику записей сохраненной процедуры.</span><span class="sxs-lookup"><span data-stu-id="8539d-107">A server filter cannot be applied to a stored procedure's record source.</span></span>

## <a name="setting"></a><span data-ttu-id="8539d-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="8539d-108">Setting</span></span>

<span data-ttu-id="8539d-109">Действие **ApplyFilter** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="8539d-109">The **ApplyFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8539d-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="8539d-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8539d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8539d-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8539d-112">Имя фильтра</span><span class="sxs-lookup"><span data-stu-id="8539d-112">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="8539d-113">Имя фильтра или запроса, который ограничивает или сортит записи таблицы, формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="8539d-113">The name of a filter or query that restricts or sorts the records of the table, form, or report.</span></span> <span data-ttu-id="8539d-114">Вы можете ввести имя существующего запроса или фильтра, сохраненного в поле <strong>Имя</strong> фильтра в разделе <strong>Аргументы</strong> действий области <strong>Macro Builder.</strong></span><span class="sxs-lookup"><span data-stu-id="8539d-114">You can enter the name of either an existing query or a filter that has been saved as a query in the <strong>Filter Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane.</span></span></p><p><span data-ttu-id="8539d-115"><strong>ПРИМЕЧАНИЕ.</strong>При использовании этого действия для применения фильтра сервера аргумент Filter Name должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="8539d-115"><strong>NOTE</strong>: When you are using this action to apply a server filter, the Filter Name argument must be blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8539d-116">Где состояние</span><span class="sxs-lookup"><span data-stu-id="8539d-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="8539d-117">Допустимый SQL WHERE (без слова WHERE) или выражение, ограничивающее записи таблицы, формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="8539d-117">A valid SQL WHERE clause (without the word WHERE) or an expression that restricts the records of the table, form, or report.</span></span></p>
<p><span data-ttu-id="8539d-118"><b>ПРИМЕЧАНИЕ.</b>В выражении аргумента Where Condition левая сторона выражения обычно содержит имя поля из таблицы или запроса формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="8539d-118"><b>NOTE</b>: In a Where Condition argument expression, the left side of the expression typically contains a field name from the underlying table or query for the form or report.</span></span> <span data-ttu-id="8539d-119">Правая сторона выражения обычно содержит критерии, которые необходимо применить к этому полю для ограничения или сортировки записей.</span><span class="sxs-lookup"><span data-stu-id="8539d-119">The right side of the expression typically contains the criteria you want to apply to this field to restrict or sort the records.</span></span> <span data-ttu-id="8539d-120">Например, критериями может быть имя управления в другой форме, содержа содержа которое содержит необходимое значение записей в первой форме для соответствия.</span><span class="sxs-lookup"><span data-stu-id="8539d-120">For example, the criteria can be the name of a control on another form that contains the value you want the records in the first form to match.</span></span> <span data-ttu-id="8539d-121">Имя управления должно быть полностью квалифицировано, например:</span><span class="sxs-lookup"><span data-stu-id="8539d-121">The name of the control should be fully qualified, for example:</span></span></p>
<p><span data-ttu-id="8539d-122"><strong>Формы</strong>! <em>formname!</em> <em>имя управления</em> Имена полей должны быть окружены двойными кавычками, а строковая буква должна быть окружена одними кавычками.</span><span class="sxs-lookup"><span data-stu-id="8539d-122"><strong>Forms</strong>!<em>formname</em>!<em>controlname</em> Field names should be surrounded by double quotation marks and string literals should be surrounded by single quotation marks.</span></span> <span data-ttu-id="8539d-123">Максимальная длина аргумента Where Condition — 255 символов.</span><span class="sxs-lookup"><span data-stu-id="8539d-123">The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="8539d-124">Если вам необходимо ввести более длинную оговорку SQL WHERE, используйте метод <strong>ApplyFilter</strong> объекта <strong>DoCmd</strong> в модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="8539d-124">If you need to enter a longer SQL WHERE clause, use the <strong>ApplyFilter</strong> method of the <strong>DoCmd</strong> object in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="8539d-125">Вы можете ввести SQL, где в VBA можно ввести утверждения о клаузулах до 32 768 знаков.</span><span class="sxs-lookup"><span data-stu-id="8539d-125">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8539d-126">Вы можете использовать аргумент Filter Name, если вы уже определили фильтр, который предоставляет соответствующие данные.</span><span class="sxs-lookup"><span data-stu-id="8539d-126">You can use the Filter Name argument if you have already defined a filter that provides the appropriate data.</span></span> <span data-ttu-id="8539d-127">Для прямого ввода критериев ограничения можно использовать аргумент Where Condition.</span><span class="sxs-lookup"><span data-stu-id="8539d-127">You can use the Where Condition argument to enter the restriction criteria directly.</span></span> <span data-ttu-id="8539d-128">Если вы используете оба аргумента, Microsoft Office Access 2007 применяет пункт WHERE к результатам фильтра.</span><span class="sxs-lookup"><span data-stu-id="8539d-128">If you use both arguments, Microsoft Office Access 2007 applies the WHERE clause to the results of the filter.</span></span> <span data-ttu-id="8539d-129">Необходимо использовать один или оба аргумента.</span><span class="sxs-lookup"><span data-stu-id="8539d-129">You must use one or both arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="8539d-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="8539d-130">Remarks</span></span>

<span data-ttu-id="8539d-131">Вы можете применить фильтр или запрос к форме в представлении формы или представлении таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="8539d-131">You can apply a filter or query to a form in Form view or Datasheet view.</span></span>

<span data-ttu-id="8539d-132">Фильтр и условия WHERE, которые вы применяете, становятся параметром свойства Фильтр формы или отчета **или** **ServerFilter.**</span><span class="sxs-lookup"><span data-stu-id="8539d-132">The filter and WHERE condition you apply become the setting of the form's or report's **Filter** or **ServerFilter** property.</span></span>

<span data-ttu-id="8539d-133">Для таблиц и форм это действие аналогично нажатию применить **фильтр/сортировку** или применить серверный фильтр **в** меню **Records.**</span><span class="sxs-lookup"><span data-stu-id="8539d-133">For tables and forms, this action is similar to clicking **Apply Filter/Sort** or **Apply Server Filter** on the **Records** menu.</span></span> <span data-ttu-id="8539d-134">Команда меню применяет недавно созданный фильтр к таблице или форме, в то время как действие **ApplyFilter** применяет указанный фильтр или запрос.</span><span class="sxs-lookup"><span data-stu-id="8539d-134">The menu command applies the most recently created filter to the table or form, whereas the **ApplyFilter** action applies a specified filter or query.</span></span>

<span data-ttu-id="8539d-135">В базе данных Доступа,  если вы указываете на фильтр в меню **Records,** а затем щелкните Расширенный **фильтр/Сортировка** после запуска действия **ApplyFilter,** в окне Advanced Filter/Sort показаны критерии фильтра, выбранные с помощью этого действия.</span><span class="sxs-lookup"><span data-stu-id="8539d-135">In an Access database, if you point to **Filter** on the **Records** menu and then click **Advanced Filter/Sort** after running the **ApplyFilter** action, the Advanced Filter/Sort window shows the filter criteria you have selected with this action.</span></span>

<span data-ttu-id="8539d-136">Чтобы удалить фильтр и отобразить все записи для таблицы или формы в базе данных Office Access 2007, можно использовать действие **ShowAllRecords** или команду **Remove Filter/Sort** в меню **Records.**</span><span class="sxs-lookup"><span data-stu-id="8539d-136">To remove a filter and display all of the records for a table or form in an Office Access 2007 database, you can use the **ShowAllRecords** action or the **Remove Filter/Sort** command on the **Records** menu.</span></span> <span data-ttu-id="8539d-137">Чтобы удалить фильтр в проекте Access (.adp), можно вернуться в окно Фильтр сервера  по форме и удалить все критерии фильтра, а затем нажмите кнопку Применить фильтр сервера в меню **Records** на панели инструментов или задать свойство **ServerFilterByForm** false  (0).</span><span class="sxs-lookup"><span data-stu-id="8539d-137">To remove a filter in an Access project (.adp), you can return to the Server Filter By Form window and remove all filter criteria and then click **Apply Server Filter** on the **Records** menu on the toolbar, or set the **ServerFilterByForm** property to **False** (0).</span></span>

<span data-ttu-id="8539d-138">При сохранения таблицы или формы Access сохраняет любой фильтр, определенный в настоящее время в этом объекте, но не будет применять фильтр автоматически при следующем открываемом объекте (хотя он автоматически применяет любой вид, примененный к объекту до его сохранения).</span><span class="sxs-lookup"><span data-stu-id="8539d-138">When you save a table or form, Access saves any filter currently defined in that object, but won't apply the filter automatically the next time the object is opened (although it will automatically apply any sort you applied to the object before it was saved).</span></span> <span data-ttu-id="8539d-139">Если требуется автоматически применять фильтр при первом открывлении формы, укажите макрос, содержащий действие **ApplyFilter,** или процедуру событий, содержащую метод **ApplyFilter** объекта **DoCmd** в качестве параметра свойства **события OnOpen** формы.</span><span class="sxs-lookup"><span data-stu-id="8539d-139">If you want to apply a filter automatically when a form is first opened, specify a macro containing the **ApplyFilter** action or an event procedure containing the **ApplyFilter** method of the **DoCmd** object as the **OnOpen** event property setting of the form.</span></span> <span data-ttu-id="8539d-140">Фильтр также можно применить с помощью **действия OpenForm** или **OpenReport** или соответствующих методов.</span><span class="sxs-lookup"><span data-stu-id="8539d-140">You can also apply a filter by using the **OpenForm** or **OpenReport** action, or their corresponding methods.</span></span> <span data-ttu-id="8539d-141">Чтобы автоматически применить фильтр при первом вскрытии таблицы, можно открыть таблицу с помощью макроса, содержащего действие **OpenTable,** а затем сразу же последует действие **ApplyFilter.**</span><span class="sxs-lookup"><span data-stu-id="8539d-141">To apply a filter automatically when a table is first opened, you can open the table by using a macro containing the **OpenTable** action, followed immediately by the **ApplyFilter** action.</span></span>

## <a name="example"></a><span data-ttu-id="8539d-142">Пример</span><span class="sxs-lookup"><span data-stu-id="8539d-142">Example</span></span>

<span data-ttu-id="8539d-143">В следующем примере показано, как использовать действие ApplyFilter для фильтрации формы frmFoods по мере ее открытия.</span><span class="sxs-lookup"><span data-stu-id="8539d-143">The following example shows how to use the ApplyFilter action to filter the frmFoods form as it is opened.</span></span>

<span data-ttu-id="8539d-144">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="8539d-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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



