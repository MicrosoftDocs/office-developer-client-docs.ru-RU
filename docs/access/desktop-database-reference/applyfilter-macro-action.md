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
ms.openlocfilehash: f6f0511a1358e8d9b0d0ee820e83cf59d2400345
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025970"
---
# <a name="applyfilter-macro-action"></a><span data-ttu-id="9d490-102">Макрокоманда ApplyFilter</span><span class="sxs-lookup"><span data-stu-id="9d490-102">ApplyFilter macro action</span></span>

<span data-ttu-id="9d490-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d490-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9d490-104">Чтобы применить фильтр, запрос или инструкцию SQL в таблице, форму или отчет, чтобы ограничить или сортировки записей в таблице или записей из базовой таблицы или запроса формы или отчета можно использовать **ПрименитьФильтр** .</span><span class="sxs-lookup"><span data-stu-id="9d490-104">You can use the **ApplyFilter** action to apply a filter, a query, or an SQL WHERE clause to a table, form, or report to restrict or sort the records in the table, or the records from the underlying table or query of the form or report.</span></span> <span data-ttu-id="9d490-105">Для отчетов это действие можно использовать только в макросе, указанном в свойстве события **формы** отчета.</span><span class="sxs-lookup"><span data-stu-id="9d490-105">For reports, you can use this action only in a macro specified by the report's **OnOpen** event property.</span></span>

> [!NOTE]
> <span data-ttu-id="9d490-106">Это действие можно использовать для применения инструкцию SQL только при применении серверного фильтра.</span><span class="sxs-lookup"><span data-stu-id="9d490-106">You can use this action to apply an SQL WHERE clause only when applying a server filter.</span></span> <span data-ttu-id="9d490-107">Не удается применить фильтр сервера к источнику записей хранимую процедуру.</span><span class="sxs-lookup"><span data-stu-id="9d490-107">A server filter cannot be applied to a stored procedure's record source.</span></span>

## <a name="setting"></a><span data-ttu-id="9d490-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="9d490-108">Setting</span></span>

<span data-ttu-id="9d490-109">**ПрименитьФильтр** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="9d490-109">The **ApplyFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d490-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="9d490-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="9d490-111">Описание</span><span class="sxs-lookup"><span data-stu-id="9d490-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d490-112">Имя фильтра</span><span class="sxs-lookup"><span data-stu-id="9d490-112">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="9d490-113">Имя фильтра или запроса, который ограничивает число или сортировки записей таблицы, формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="9d490-113">The name of a filter or query that restricts or sorts the records of the table, form, or report.</span></span> <span data-ttu-id="9d490-114">Можно ввести имя существующего запроса или фильтр, который был сохранен как запроса в поле <strong>Имя фильтра</strong> в разделе <strong>Действие аргументы</strong> в области <strong>Построения макросов</strong> .</span><span class="sxs-lookup"><span data-stu-id="9d490-114">You can enter the name of either an existing query or a filter that has been saved as a query in the <strong>Filter Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane.</span></span></p><p><span data-ttu-id="9d490-115"><strong>Примечание</strong>: при использовании этого действия Применить фильтр сервера аргумента имя фильтра должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="9d490-115"><strong>NOTE</strong>: When you are using this action to apply a server filter, the Filter Name argument must be blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d490-116">Условие отбора</span><span class="sxs-lookup"><span data-stu-id="9d490-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="9d490-117">Оператор SQL WHERE (без слова ГДЕ) или выражение, которое ограничивает число записей таблицы, формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="9d490-117">A valid SQL WHERE clause (without the word WHERE) or an expression that restricts the records of the table, form, or report.</span></span></p>
<p><span data-ttu-id="9d490-118"><b>Примечание</b>: как правило, в котором аргумент выражение условия, в левой части выражения содержит имя поля из базовой таблицы или запроса для формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="9d490-118"><b>NOTE</b>: In a Where Condition argument expression, the left side of the expression typically contains a field name from the underlying table or query for the form or report.</span></span> <span data-ttu-id="9d490-119">В правой части выражения обычно содержит условия, которые необходимо применить к этому полю ли ограничить или отсортировать записи.</span><span class="sxs-lookup"><span data-stu-id="9d490-119">The right side of the expression typically contains the criteria you want to apply to this field to restrict or sort the records.</span></span> <span data-ttu-id="9d490-120">Например критерии может быть имя элемента управления на другой формы, которая содержит значение записей в первую форму в соответствии с.</span><span class="sxs-lookup"><span data-stu-id="9d490-120">For example, the criteria can be the name of a control on another form that contains the value you want the records in the first form to match.</span></span> <span data-ttu-id="9d490-121">Имя элемента управления, должен быть полным, например:</span><span class="sxs-lookup"><span data-stu-id="9d490-121">The name of the control should be fully qualified, for example:</span></span></p>
<p><span data-ttu-id="9d490-122"><strong>Forms</strong>! <em>имя_формы</em>! <em>ИмяЭлементаУправления</em> Имена полей должны быть заключены в двойные кавычки и литералы должны быть заключены в одинарные кавычки.</span><span class="sxs-lookup"><span data-stu-id="9d490-122"><strong>Forms</strong>!<em>formname</em>!<em>controlname</em> Field names should be surrounded by double quotation marks and string literals should be surrounded by single quotation marks.</span></span> <span data-ttu-id="9d490-123">Максимальная длина аргумента условие составляет 255 знаков.</span><span class="sxs-lookup"><span data-stu-id="9d490-123">The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="9d490-124">Если необходимо ввести более SQL предложение WHERE, используйте метод <strong>ApplyFilter</strong> <strong>объекта</strong> в Visual Basic для приложений (VBA) модуля.</span><span class="sxs-lookup"><span data-stu-id="9d490-124">If you need to enter a longer SQL WHERE clause, use the <strong>ApplyFilter</strong> method of the <strong>DoCmd</strong> object in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="9d490-125">Можно ввести предложение инструкции SQL до 32 768 знаков в VBA.</span><span class="sxs-lookup"><span data-stu-id="9d490-125">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="9d490-126">Аргумент имя фильтра можно использовать при указании фильтра, который предоставляет требуемые данные.</span><span class="sxs-lookup"><span data-stu-id="9d490-126">You can use the Filter Name argument if you have already defined a filter that provides the appropriate data.</span></span> <span data-ttu-id="9d490-127">Аргумент Условие можно использовать для ввода критериев ограничения напрямую.</span><span class="sxs-lookup"><span data-stu-id="9d490-127">You can use the Where Condition argument to enter the restriction criteria directly.</span></span> <span data-ttu-id="9d490-128">Если вы используете оба аргумента, Microsoft Office Access 2007 применяется предложение WHERE к фильтру.</span><span class="sxs-lookup"><span data-stu-id="9d490-128">If you use both arguments, Microsoft Office Access 2007 applies the WHERE clause to the results of the filter.</span></span> <span data-ttu-id="9d490-129">Необходимо использовать один или оба элемента.</span><span class="sxs-lookup"><span data-stu-id="9d490-129">You must use one or both arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d490-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="9d490-130">Remarks</span></span>

<span data-ttu-id="9d490-131">Можно применить фильтр или запрос в форму в режиме формы или таблицы.</span><span class="sxs-lookup"><span data-stu-id="9d490-131">You can apply a filter or query to a form in Form view or Datasheet view.</span></span>

<span data-ttu-id="9d490-132">Фильтр и условия WHERE, применяемые становятся формы или отчета **фильтра** или **ServerFilter** свойства.</span><span class="sxs-lookup"><span data-stu-id="9d490-132">The filter and WHERE condition you apply become the setting of the form's or report's **Filter** or **ServerFilter** property.</span></span>

<span data-ttu-id="9d490-133">Для таблиц и форм это действие аналогично **записей** выберите в меню команду **Применить фильтр** или **Применить фильтр сервера** .</span><span class="sxs-lookup"><span data-stu-id="9d490-133">For tables and forms, this action is similar to clicking **Apply Filter/Sort** or **Apply Server Filter** on the **Records** menu.</span></span> <span data-ttu-id="9d490-134">Команда меню применяет недавно созданного фильтра для таблицы или формы, в то время как **ПрименитьФильтр** применяет указанный фильтр или запрос.</span><span class="sxs-lookup"><span data-stu-id="9d490-134">The menu command applies the most recently created filter to the table or form, whereas the **ApplyFilter** action applies a specified filter or query.</span></span>

<span data-ttu-id="9d490-135">В базе данных Microsoft Access Если выберите **Фильтр** в меню **записи** и нажмите кнопку **Расширенный фильтр** после выполнения **ПрименитьФильтр** в окне Расширенный фильтр отображается условия фильтра выбора с Это действие.</span><span class="sxs-lookup"><span data-stu-id="9d490-135">In an Access database, if you point to **Filter** on the **Records** menu and then click **Advanced Filter/Sort** after running the **ApplyFilter** action, the Advanced Filter/Sort window shows the filter criteria you have selected with this action.</span></span>

<span data-ttu-id="9d490-136">Чтобы удалить фильтр и отображения всех записей в таблице или формы базы данных Microsoft Office Access 2007, можно использовать команду **Удалить фильтр** или **ПоказатьВсеЗаписи** меню **записи** .</span><span class="sxs-lookup"><span data-stu-id="9d490-136">To remove a filter and display all of the records for a table or form in an Office Access 2007 database, you can use the **ShowAllRecords** action or the **Remove Filter/Sort** command on the **Records** menu.</span></span> <span data-ttu-id="9d490-137">Чтобы удалить фильтр в проекте Microsoft Access (файлы с расширением ADP), можно вернуться в окно серверного фильтра и удалить все условия фильтра и затем нажмите кнопку **Применить фильтр сервера** в меню **записи** на панели инструментов или присвойте свойству **(ServerFilterByForm)** значение **False** (0).</span><span class="sxs-lookup"><span data-stu-id="9d490-137">To remove a filter in an Access project (.adp), you can return to the Server Filter By Form window and remove all filter criteria and then click **Apply Server Filter** on the **Records** menu on the toolbar, or set the **ServerFilterByForm** property to **False** (0).</span></span>

<span data-ttu-id="9d490-138">При сохранении таблицы или формы Access сохраняет ни одному фильтру, определенных в текущий момент в этот объект, но не будут автоматически применить фильтр следующего открытии объекта (хотя он будет автоматически применен любого вида, примененного к объекту перед ее сохранения).</span><span class="sxs-lookup"><span data-stu-id="9d490-138">When you save a table or form, Access saves any filter currently defined in that object, but won't apply the filter automatically the next time the object is opened (although it will automatically apply any sort you applied to the object before it was saved).</span></span> <span data-ttu-id="9d490-139">Если вы хотите применить фильтр автоматически при первом открытии формы, укажите макрос, содержащий **ПрименитьФильтр** или процедуру события, содержащий метод **ApplyFilter** \*\*объекта как события **формы** \*\* значение параметра свойства формы.</span><span class="sxs-lookup"><span data-stu-id="9d490-139">If you want to apply a filter automatically when a form is first opened, specify a macro containing the **ApplyFilter** action or an event procedure containing the **ApplyFilter** method of the **DoCmd** object as the **OnOpen** event property setting of the form.</span></span> <span data-ttu-id="9d490-140">Также можно применить фильтр с помощью действие **ОткрытьФорму** или **ОткрытьОтчет** или их соответствующими методами.</span><span class="sxs-lookup"><span data-stu-id="9d490-140">You can also apply a filter by using the **OpenForm** or **OpenReport** action, or their corresponding methods.</span></span> <span data-ttu-id="9d490-141">Для автоматического применения фильтра при первом открытии таблицы, можно открыть таблицы с помощью макроса, содержащего \*\*ОткрытьТаблицу, за которым следует по **ПрименитьФильтр** \*\* .</span><span class="sxs-lookup"><span data-stu-id="9d490-141">To apply a filter automatically when a table is first opened, you can open the table by using a macro containing the **OpenTable** action, followed immediately by the **ApplyFilter** action.</span></span>

## <a name="example"></a><span data-ttu-id="9d490-142">Пример</span><span class="sxs-lookup"><span data-stu-id="9d490-142">Example</span></span>

<span data-ttu-id="9d490-143">Следующем примере показано, как использовать ПрименитьФильтр для фильтрации frmFoods формы при ее открытии.</span><span class="sxs-lookup"><span data-stu-id="9d490-143">The following example shows how to use the ApplyFilter action to filter the frmFoods form as it is opened.</span></span>

<span data-ttu-id="9d490-144">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="9d490-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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



