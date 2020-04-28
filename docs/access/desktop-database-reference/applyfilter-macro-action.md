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
# <a name="applyfilter-macro-action"></a><span data-ttu-id="eb094-102">Макрокоманда ApplyFilter</span><span class="sxs-lookup"><span data-stu-id="eb094-102">ApplyFilter macro action</span></span>

<span data-ttu-id="eb094-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb094-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eb094-104">Макрокоманду **ПрименитьФильтр** можно использовать для применения фильтра, запроса или предложения WHERE SQL к таблице, форме или отчету, чтобы ограничить или отсортировать записи в таблице, или записи из базовой таблицы или запроса формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="eb094-104">You can use the **ApplyFilter** action to apply a filter, a query, or an SQL WHERE clause to a table, form, or report to restrict or sort the records in the table, or the records from the underlying table or query of the form or report.</span></span> <span data-ttu-id="eb094-105">Для отчетов это действие можно использовать только в макросе, указанном в свойстве события **OnOpen** отчета.</span><span class="sxs-lookup"><span data-stu-id="eb094-105">For reports, you can use this action only in a macro specified by the report's **OnOpen** event property.</span></span>

> [!NOTE]
> <span data-ttu-id="eb094-106">Это действие можно использовать для применения предложения WHERE в SQL только при применении серверного фильтра.</span><span class="sxs-lookup"><span data-stu-id="eb094-106">You can use this action to apply an SQL WHERE clause only when applying a server filter.</span></span> <span data-ttu-id="eb094-107">Фильтр сервера нельзя применить к источнику записи хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="eb094-107">A server filter cannot be applied to a stored procedure's record source.</span></span>

## <a name="setting"></a><span data-ttu-id="eb094-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="eb094-108">Setting</span></span>

<span data-ttu-id="eb094-109">Макрокоманда **ПрименитьФильтр** использует следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="eb094-109">The **ApplyFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb094-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="eb094-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="eb094-111">Описание</span><span class="sxs-lookup"><span data-stu-id="eb094-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb094-112">Имя фильтра</span><span class="sxs-lookup"><span data-stu-id="eb094-112">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="eb094-113">Имя фильтра или запроса, которые ограничивают или отсортирует записи таблицы, формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="eb094-113">The name of a filter or query that restricts or sorts the records of the table, form, or report.</span></span> <span data-ttu-id="eb094-114">Можно ввести имя существующего запроса или фильтра, сохраненного в виде запроса, в поле <strong>имя фильтра</strong> в разделе <strong>аргументы макрокоманды</strong> в области <strong>построителя макросов</strong> .</span><span class="sxs-lookup"><span data-stu-id="eb094-114">You can enter the name of either an existing query or a filter that has been saved as a query in the <strong>Filter Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane.</span></span></p><p><span data-ttu-id="eb094-115"><strong>Примечание</strong>. при использовании этого действия для применения серверного фильтра аргумент "имя фильтра" должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="eb094-115"><strong>NOTE</strong>: When you are using this action to apply a server filter, the Filter Name argument must be blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb094-116">Условие отбора</span><span class="sxs-lookup"><span data-stu-id="eb094-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="eb094-117">Допустимое предложение WHERE (SQL) (без слова WHERE) или выражение, которое ограничит записи таблицы, формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="eb094-117">A valid SQL WHERE clause (without the word WHERE) or an expression that restricts the records of the table, form, or report.</span></span></p>
<p><span data-ttu-id="eb094-118"><b>Примечание</b>. в выражении аргумента WHERE в выражении левая часть выражения обычно содержит имя поля из базовой таблицы или запроса для формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="eb094-118"><b>NOTE</b>: In a Where Condition argument expression, the left side of the expression typically contains a field name from the underlying table or query for the form or report.</span></span> <span data-ttu-id="eb094-119">Правая часть выражения обычно содержит критерии, которые необходимо применить к этому полю, чтобы ограничить или отсортировать записи.</span><span class="sxs-lookup"><span data-stu-id="eb094-119">The right side of the expression typically contains the criteria you want to apply to this field to restrict or sort the records.</span></span> <span data-ttu-id="eb094-120">Например, критерием может быть имя элемента управления в другой форме, которое содержит значение, которое должно совпадать с записями в первой форме.</span><span class="sxs-lookup"><span data-stu-id="eb094-120">For example, the criteria can be the name of a control on another form that contains the value you want the records in the first form to match.</span></span> <span data-ttu-id="eb094-121">Имя элемента управления должно быть полным, например:</span><span class="sxs-lookup"><span data-stu-id="eb094-121">The name of the control should be fully qualified, for example:</span></span></p>
<p><span data-ttu-id="eb094-122"><strong>Формы</strong>! <em>FormName</em>! <em>контролнаме</em> Имена полей должны быть заключены в двойные кавычки, а строковые литералы должны быть заключены в одинарные кавычки.</span><span class="sxs-lookup"><span data-stu-id="eb094-122"><strong>Forms</strong>!<em>formname</em>!<em>controlname</em> Field names should be surrounded by double quotation marks and string literals should be surrounded by single quotation marks.</span></span> <span data-ttu-id="eb094-123">Максимальная длина аргумента условия WHERE — 255 символов.</span><span class="sxs-lookup"><span data-stu-id="eb094-123">The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="eb094-124">Если необходимо ввести более длинное предложение WHERE SQL, используйте метод <strong>ApplyFilter</strong> объекта <strong>DoCmd</strong> в модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="eb094-124">If you need to enter a longer SQL WHERE clause, use the <strong>ApplyFilter</strong> method of the <strong>DoCmd</strong> object in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="eb094-125">Вы можете ввести инструкции SQL WHERE, содержащие до 32 768 символов в VBA.</span><span class="sxs-lookup"><span data-stu-id="eb094-125">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="eb094-126">Вы можете использовать аргумент имя фильтра, если вы уже определили фильтр, который предоставляет соответствующие данные.</span><span class="sxs-lookup"><span data-stu-id="eb094-126">You can use the Filter Name argument if you have already defined a filter that provides the appropriate data.</span></span> <span data-ttu-id="eb094-127">Аргумент условия WHERE можно использовать для непосредственного ввода критериев ограничения.</span><span class="sxs-lookup"><span data-stu-id="eb094-127">You can use the Where Condition argument to enter the restriction criteria directly.</span></span> <span data-ttu-id="eb094-128">Если вы используете оба аргумента, Microsoft Office Access 2007 применяет предложение WHERE к результатам фильтра.</span><span class="sxs-lookup"><span data-stu-id="eb094-128">If you use both arguments, Microsoft Office Access 2007 applies the WHERE clause to the results of the filter.</span></span> <span data-ttu-id="eb094-129">Необходимо использовать один или оба аргумента.</span><span class="sxs-lookup"><span data-stu-id="eb094-129">You must use one or both arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb094-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="eb094-130">Remarks</span></span>

<span data-ttu-id="eb094-131">Вы можете применить фильтр или запрос к форме в режиме формы или таблицы.</span><span class="sxs-lookup"><span data-stu-id="eb094-131">You can apply a filter or query to a form in Form view or Datasheet view.</span></span>

<span data-ttu-id="eb094-132">Фильтр и условие, в котором вы хотите применить, становятся значением **фильтра** формы или отчета или свойства **ServerFilter** .</span><span class="sxs-lookup"><span data-stu-id="eb094-132">The filter and WHERE condition you apply become the setting of the form's or report's **Filter** or **ServerFilter** property.</span></span>

<span data-ttu-id="eb094-133">Для таблиц и форм это действие аналогично нажатию кнопки **Применить фильтр/сортировка** или **Применить фильтр сервера** в меню **записи** .</span><span class="sxs-lookup"><span data-stu-id="eb094-133">For tables and forms, this action is similar to clicking **Apply Filter/Sort** or **Apply Server Filter** on the **Records** menu.</span></span> <span data-ttu-id="eb094-134">Команда меню применяет последний созданный фильтр к таблице или форме, а Макрокоманда **ПрименитьФильтр** применяет указанный фильтр или запрос.</span><span class="sxs-lookup"><span data-stu-id="eb094-134">The menu command applies the most recently created filter to the table or form, whereas the **ApplyFilter** action applies a specified filter or query.</span></span>

<span data-ttu-id="eb094-135">Если в базе данных Access навести указатель мыши на пункт **Фильтр** в меню **записи** , а затем выбрать команду **Расширенный фильтр/сортировка** после выполнения макрокоманды **ПрименитьФильтр** , в поле Расширенная фильтрация/сортировка отображаются условия фильтрации, выбранные с этим действием.</span><span class="sxs-lookup"><span data-stu-id="eb094-135">In an Access database, if you point to **Filter** on the **Records** menu and then click **Advanced Filter/Sort** after running the **ApplyFilter** action, the Advanced Filter/Sort window shows the filter criteria you have selected with this action.</span></span>

<span data-ttu-id="eb094-136">Чтобы удалить фильтр и отобразить все записи таблицы или формы в базе данных Office Access 2007, вы можете использовать действие **шоваллрекордс** или команду **удалить фильтр/сортировку** в меню **записи** .</span><span class="sxs-lookup"><span data-stu-id="eb094-136">To remove a filter and display all of the records for a table or form in an Office Access 2007 database, you can use the **ShowAllRecords** action or the **Remove Filter/Sort** command on the **Records** menu.</span></span> <span data-ttu-id="eb094-137">Чтобы удалить фильтр в проекте Access (ADP), можно вернуться в окно "серверный фильтр" и удалить все условия фильтра, а затем щелкнуть **Применить фильтр сервера** в меню **записи** на панели инструментов или задать для свойства **серверфилтербиформ** **значение false** (0).</span><span class="sxs-lookup"><span data-stu-id="eb094-137">To remove a filter in an Access project (.adp), you can return to the Server Filter By Form window and remove all filter criteria and then click **Apply Server Filter** on the **Records** menu on the toolbar, or set the **ServerFilterByForm** property to **False** (0).</span></span>

<span data-ttu-id="eb094-138">При сохранении таблицы или формы Access сохраняет все фильтры, определенные в этом объекте, но не применяет фильтр автоматически при следующем открытии объекта (хотя он автоматически применяет любые виды сортировки, примененные к объекту перед его сохранением).</span><span class="sxs-lookup"><span data-stu-id="eb094-138">When you save a table or form, Access saves any filter currently defined in that object, but won't apply the filter automatically the next time the object is opened (although it will automatically apply any sort you applied to the object before it was saved).</span></span> <span data-ttu-id="eb094-139">Если вы хотите применить фильтр автоматически при первом открытии формы, укажите макрос, содержащий макрокоманду **ПрименитьФильтр** , или процедуру обработки события, содержащую метод **ApplyFilter** объекта **DoCmd** , в качестве значения свойства события **OnOpen** формы.</span><span class="sxs-lookup"><span data-stu-id="eb094-139">If you want to apply a filter automatically when a form is first opened, specify a macro containing the **ApplyFilter** action or an event procedure containing the **ApplyFilter** method of the **DoCmd** object as the **OnOpen** event property setting of the form.</span></span> <span data-ttu-id="eb094-140">Фильтр можно также применить с помощью макрокоманды « **ОткрытьФорму** » или « **ОткрытьОтчет** » или соответствующих методов.</span><span class="sxs-lookup"><span data-stu-id="eb094-140">You can also apply a filter by using the **OpenForm** or **OpenReport** action, or their corresponding methods.</span></span> <span data-ttu-id="eb094-141">Чтобы применить фильтр автоматически при первом открытии таблицы, можно открыть таблицу с помощью макроса, содержащего действие **опентабле** , за которым следует действие **ПрименитьФильтр** сразу же.</span><span class="sxs-lookup"><span data-stu-id="eb094-141">To apply a filter automatically when a table is first opened, you can open the table by using a macro containing the **OpenTable** action, followed immediately by the **ApplyFilter** action.</span></span>

## <a name="example"></a><span data-ttu-id="eb094-142">Пример</span><span class="sxs-lookup"><span data-stu-id="eb094-142">Example</span></span>

<span data-ttu-id="eb094-143">В приведенном ниже примере показано, как с помощью макрокоманды ПрименитьФильтр отфильтровать форму Фрмфудс при ее открытии.</span><span class="sxs-lookup"><span data-stu-id="eb094-143">The following example shows how to use the ApplyFilter action to filter the frmFoods form as it is opened.</span></span>

<span data-ttu-id="eb094-144">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="eb094-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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



