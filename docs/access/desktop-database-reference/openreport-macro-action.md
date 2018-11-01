---
title: Действия ОткрытьОтчет макроса
TOCTitle: OpenReport Macro Action
ms:assetid: cd35faf2-190d-ac48-cf59-81c1599eb764
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834462(v=office.15)
ms:contentKeyID: 48547758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm188079
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ef2a1f5afd4b8828fdc39744e92d0a4e92ca7bd6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871495"
---
# <a name="openreport-macro-action"></a><span data-ttu-id="69a90-102">Действия ОткрытьОтчет макроса</span><span class="sxs-lookup"><span data-stu-id="69a90-102">OpenReport Macro Action</span></span>

<span data-ttu-id="69a90-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69a90-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69a90-104">Чтобы открыть отчет в режиме конструктора или просмотра или отправить отчет на принтер, можно использовать **ОткрытьОтчет** .</span><span class="sxs-lookup"><span data-stu-id="69a90-104">You can use the **OpenReport** action to open a report in Design view or Print Preview, or to send the report directly to the printer.</span></span> <span data-ttu-id="69a90-105">Можно также ограничить записей, которые печатаются в отчете.</span><span class="sxs-lookup"><span data-stu-id="69a90-105">You can also restrict the records that are printed in the report.</span></span>

## <a name="setting"></a><span data-ttu-id="69a90-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="69a90-106">Setting</span></span>

<span data-ttu-id="69a90-107">**ОткрытьОтчет** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="69a90-107">The **OpenReport** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="69a90-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="69a90-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="69a90-109">Описание</span><span class="sxs-lookup"><span data-stu-id="69a90-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69a90-110">Имя отчета</span><span class="sxs-lookup"><span data-stu-id="69a90-110">Report Name</span></span></p></td>
<td><p><span data-ttu-id="69a90-111">Имя отчета, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="69a90-111">The name of the report to open.</span></span> <span data-ttu-id="69a90-112">В поле <strong>Имя отчета</strong> в разделе <strong>Действие аргументы</strong> в области <strong>Построения макросов</strong> содержит все отчеты в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="69a90-112">The <strong>Report Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane shows all reports in the current database.</span></span> <span data-ttu-id="69a90-113">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="69a90-113">This is a required argument.</span></span> <span data-ttu-id="69a90-114">Если макрос, содержащий ОткрытьОтчет в базе данных библиотеки, Microsoft Access сначала выполняет поиск отчета с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="69a90-114">If you run a macro containing the OpenReport action in a library database, Microsoft Access first looks for the report with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69a90-115">Представление</span><span class="sxs-lookup"><span data-stu-id="69a90-115">View</span></span></p></td>
<td><p><span data-ttu-id="69a90-116">Представление, в котором будет открыть отчет.</span><span class="sxs-lookup"><span data-stu-id="69a90-116">The view in which the report will open.</span></span> <span data-ttu-id="69a90-117">Нажмите кнопку <strong>Печать</strong> (выводит отчет на печать), <strong>проекта</strong>или <strong>Предварительный</strong> в поле <strong>View</strong> .</span><span class="sxs-lookup"><span data-stu-id="69a90-117">Click <strong>Print</strong> (print the report immediately), <strong>Design</strong>, or <strong>Print Preview</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="69a90-118">Значение по умолчанию — <strong>Print</strong>.</span><span class="sxs-lookup"><span data-stu-id="69a90-118">The default is <strong>Print</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69a90-119">Имя фильтра</span><span class="sxs-lookup"><span data-stu-id="69a90-119">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="69a90-120">Фильтр, который ограничивает число записей отчета.</span><span class="sxs-lookup"><span data-stu-id="69a90-120">A filter that restricts the report's records.</span></span> <span data-ttu-id="69a90-121">Можно ввести имя существующего запроса или фильтр, который был сохранен в виде запроса.</span><span class="sxs-lookup"><span data-stu-id="69a90-121">You can enter the name of either an existing query or a filter that was saved as a query.</span></span> <span data-ttu-id="69a90-122">Тем не менее запрос должен включать все поля в отчете открывают или свойству <strong>Вывод всех полей</strong> , значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="69a90-122">However, the query must include all the fields in the report you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69a90-123">Условие отбора</span><span class="sxs-lookup"><span data-stu-id="69a90-123">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="69a90-124">Оператор SQL WHERE (без слова ГДЕ) или выражение, которое следует использовать для выбора записей из отчета базовым таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="69a90-124">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the report's underlying table or query.</span></span> <span data-ttu-id="69a90-125">Если выбран параметр аргумента имя фильтра, доступа применяется это предложение WHERE к фильтру.</span><span class="sxs-lookup"><span data-stu-id="69a90-125">If you select a filter with the Filter Name argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="69a90-126">Чтобы открыть отчет и отобрать те указанное значение элемента управления на форме ее записи, используйте следующее выражение:</span><span class="sxs-lookup"><span data-stu-id="69a90-126">To open a report and restrict its records to those specified by the value of a control on a form, use the following expression:</span></span><br /><span data-ttu-id="69a90-127">
<strong>[</strong><em>fieldname</em><strong>] = формы! [</strong><em>имя_формы</em><strong>]! [</strong><em>имяЭлементаВФорме</em><strong>]</strong></span><span class="sxs-lookup"><span data-stu-id="69a90-127">
<strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on form</em><strong>]</strong></span></span><br />
<span data-ttu-id="69a90-128">Замените <em>fieldname</em> имя поля в базовой таблицы или запроса отчета, который необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="69a90-128">Replace <em>fieldname</em> with the name of a field in the underlying table or query of the report you want to open.</span></span> <span data-ttu-id="69a90-129">Замените имя формы и элемента управления на форме, которая содержит значение записи в отчет в соответствии с <em>имя_формы</em> и <em>имяЭлементаВФорме</em> .</span><span class="sxs-lookup"><span data-stu-id="69a90-129">Replace <em>formname</em> and <em>controlname on form</em> with the name of the form and the control on the form that contains the value you want records in the report to match.</span></span></p>
<p><span data-ttu-id="69a90-130"><b>Примечание</b>: максимальная длина аргумента условие составляет 255 знаков.</span><span class="sxs-lookup"><span data-stu-id="69a90-130"><b>NOTE</b>: The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="69a90-131">Если необходимо ввести более сложных SQL предложение WHERE большее, используйте метод <b>OpenReport</b> <b>объекта</b> в Visual Basic для приложений (VBA) модуля.</span><span class="sxs-lookup"><span data-stu-id="69a90-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <b>OpenReport</b> method of the <b>DoCmd</b> object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="69a90-132">Можно ввести предложение инструкции SQL до 32 768 знаков в VBA.</span><span class="sxs-lookup"><span data-stu-id="69a90-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69a90-133">Режим окна</span><span class="sxs-lookup"><span data-stu-id="69a90-133">Window Mode</span></span></p></td>
<td><p><span data-ttu-id="69a90-134">Режим, в котором будет открыть отчет.</span><span class="sxs-lookup"><span data-stu-id="69a90-134">The mode in which the report will open.</span></span> <span data-ttu-id="69a90-135">Выберите <strong>Обычный</strong>, <strong>скрытые</strong>, <strong>значок</strong>или <strong>диалоговое окно</strong> в поле <strong>Режим окна</strong> .</span><span class="sxs-lookup"><span data-stu-id="69a90-135">Click <strong>Normal</strong>, <strong>Hidden</strong>, <strong>Icon</strong>, or <strong>Dialog</strong> in the <strong>Window Mode</strong> box.</span></span> <span data-ttu-id="69a90-136">Значение по умолчанию — <strong>Normal</strong>.</span><span class="sxs-lookup"><span data-stu-id="69a90-136">The default is <strong>Normal</strong>.</span></span></p>
<p><span data-ttu-id="69a90-137"><b>Примечание</b>: некоторые режим окна аргумент параметры не применяются при с помощью с вкладками документы.</span><span class="sxs-lookup"><span data-stu-id="69a90-137"><b>NOTE</b>: Some Window Mode argument settings do not apply when using tabbed documents.</span></span> <span data-ttu-id="69a90-138">Чтобы переключиться на перекрывающиеся windows:</span><span class="sxs-lookup"><span data-stu-id="69a90-138">To switch to overlapping windows:</span></span>
<ol>
<li><p><span data-ttu-id="69a90-139">Нажмите кнопку <strong>Параметры</strong>.</span><span class="sxs-lookup"><span data-stu-id="69a90-139">Click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="69a90-140">В диалоговом окне <strong>Параметры доступа</strong> щелкните <strong>Текущей базы данных</strong>.</span><span class="sxs-lookup"><span data-stu-id="69a90-140">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="69a90-141">В разделе <strong>Параметры приложения</strong> в разделе <strong>Параметры окна документа</strong>нажмите кнопку <strong>Перекрывающиеся Windows</strong>.</span><span class="sxs-lookup"><span data-stu-id="69a90-141">In the <strong>Application Options</strong> section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="69a90-142">Нажмите кнопку <strong>ОК</strong>и закройте и снова откройте базу данных.</span><span class="sxs-lookup"><span data-stu-id="69a90-142">Click <strong>OK</strong>, and then close and reopen the database.</span></span></p></li>
</ol>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="69a90-143">Замечания</span><span class="sxs-lookup"><span data-stu-id="69a90-143">Remarks</span></span>

<span data-ttu-id="69a90-144">Параметр **печати** для аргумента **представления** печать отчета с использованием текущих настроек принтера, не открывая диалогового окна **Печать** .</span><span class="sxs-lookup"><span data-stu-id="69a90-144">The **Print** setting for the **View** argument prints the report immediately by using the current printer settings, without bringing up the **Print** dialog box.</span></span> <span data-ttu-id="69a90-145">Можно также использовать **ОткрытьОтчет** Открытие и настройка отчета и затем использовать макрокоманду для печати.</span><span class="sxs-lookup"><span data-stu-id="69a90-145">You can also use the **OpenReport** action to open and set up a report and then use the PrintOut action to print it.</span></span> <span data-ttu-id="69a90-146">Например может потребоваться изменить отчет или использовать **макрокоманду** , чтобы изменить параметры принтера перед печатью.</span><span class="sxs-lookup"><span data-stu-id="69a90-146">For example, you may want to modify the report or use the **PrintOut** action to change the printer settings before you print.</span></span>

<span data-ttu-id="69a90-147">Фильтр и условия WHERE, применяемые становятся свойства **фильтра** отчета.</span><span class="sxs-lookup"><span data-stu-id="69a90-147">The filter and WHERE condition you apply become the setting of the report's **Filter** property.</span></span>

<span data-ttu-id="69a90-148">**ОткрытьОтчет** аналогично дважды щелкнуть отчет на панели навигации или щелкнув правой кнопкой мыши отчет на левой панели навигации и выбрав команду **Print** или представления.</span><span class="sxs-lookup"><span data-stu-id="69a90-148">The **OpenReport** action is similar to double-clicking the report in the Navigation Pane, or right-clicking the report in the Navigation Pane and selecting a view or the **Print** command.</span></span>

> [!TIP] 
> - <span data-ttu-id="69a90-149">Чтобы распечатать аналогичные отчеты для разных наборов данных, используйте фильтр или предложение WHERE для ограничения записей при выводе на печать в отчете.</span><span class="sxs-lookup"><span data-stu-id="69a90-149">To print similar reports for different sets of data, use a filter or a WHERE clause to restrict the records printed in the report.</span></span> <span data-ttu-id="69a90-150">Затем измените макрос, чтобы применить другой фильтр или изменить аргумент условие.</span><span class="sxs-lookup"><span data-stu-id="69a90-150">Then edit the macro to apply a different filter or change the Where Condition argument.</span></span>
> 
> - <span data-ttu-id="69a90-151">Отчет можно перетаскивать из области переходов в строку действие в макросе.</span><span class="sxs-lookup"><span data-stu-id="69a90-151">You can drag a report from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="69a90-152">Это автоматически создает **ОткрытьОтчет, который открывает отчет в представлении отчета** .</span><span class="sxs-lookup"><span data-stu-id="69a90-152">This automatically creates an **OpenReport** action that opens the report in Report view.</span></span>

## <a name="example"></a><span data-ttu-id="69a90-153">Пример</span><span class="sxs-lookup"><span data-stu-id="69a90-153">Example</span></span>

<span data-ttu-id="69a90-154">Приведенный ниже показано, как использовать ОткрытьОтчет передать параметр, выполняющий фильтрацию отчета, как она открывается.</span><span class="sxs-lookup"><span data-stu-id="69a90-154">The following example shows how to use the OpenReport action to pass a parameter that filters a report as it is opened.</span></span> <span data-ttu-id="69a90-155">В отчете **rptChapters** отображаются записи для указанного автора, передав элемента, выбранного в поле со списком **cboAuthors** для параметра SelectedAuthor.</span><span class="sxs-lookup"><span data-stu-id="69a90-155">The **rptChapters** report displays the records for the specified author by passing the item selected in the **cboAuthors** combo box to the SelectedAuthor parameter.</span></span>

<span data-ttu-id="69a90-156">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="69a90-156">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OpenReport
        Report Name rptChapters
        View Report
        Filter Name
        Where Condition
        Window Mode Normal
    
    Parameters
        SelectedAuthor =[cboAuthor]
```
