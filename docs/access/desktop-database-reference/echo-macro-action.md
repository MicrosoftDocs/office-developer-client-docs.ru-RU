---
title: Макро макрос Echo (справочник по базе данных Access для настольных пк)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d536ed47c780b7f9f1675a9879e86aeff80b67f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293625"
---
# <a name="echo-macro-action"></a><span data-ttu-id="ad0c3-102">Макрокоманда Echo</span><span class="sxs-lookup"><span data-stu-id="ad0c3-102">Echo macro action</span></span>

<span data-ttu-id="ad0c3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad0c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ad0c3-104">Вы можете использовать действие **Echo,** чтобы указать, включено ли эхо.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-104">You can use the **Echo** action to specify whether echo is turned on.</span></span> <span data-ttu-id="ad0c3-105">Например, это действие можно использовать для скрытие или показа результатов макроса во время его работы.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-105">For example, you can use this action to hide or show the results of a macro while it runs.</span></span>

## <a name="setting"></a><span data-ttu-id="ad0c3-106">Setting</span><span class="sxs-lookup"><span data-stu-id="ad0c3-106">Setting</span></span>

> [!NOTE]
> <span data-ttu-id="ad0c3-107">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-107">This action will not be allowed if the database is not trusted.</span></span>

<span data-ttu-id="ad0c3-108">Действие **Echo** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-108">The **Echo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ad0c3-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="ad0c3-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ad0c3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ad0c3-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad0c3-111"><strong>Эхо в ветвях</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-111"><strong>Echo On</strong></span></span></p></td>
<td><p><span data-ttu-id="ad0c3-112">Нажмите <strong>кнопку "Да"</strong> (включить эхо) или <strong>"Нет"</strong> <strong></strong> (отключить эхо) в поле <strong>"Эхо в</strong> действии" в разделе "Аргументы действий" области построитель макроса.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-112">Click <strong>Yes</strong> (turn echo on) or <strong>No</strong> (turn echo off) in the <strong>Echo On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="ad0c3-113">Значение по умолчанию <strong>— Да.</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-113">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad0c3-114"><strong>Текст в панели состояния</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-114"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="ad0c3-115">Текст, который будет отображаться в панели состояния, когда эхо отключено.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-115">The text to display in the status bar when echo is turned off.</span></span> <span data-ttu-id="ad0c3-116">Например, если эхо отключено, в панели состояния может отображаться &quot; запущенный макрос.&quot;</span><span class="sxs-lookup"><span data-stu-id="ad0c3-116">For example, when echo is turned off, the status bar can display &quot;The macro is running.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ad0c3-117">При запуске макроса при обновлении экрана часто показываются сведения, не важные для работы макроса.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-117">When a macro runs, screen updating often shows information not essential to the functioning of the macro.</span></span> <span data-ttu-id="ad0c3-118">Если для аргумента **Echo On** установлено **"Нет",** макрос выполняется без обновления экрана.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-118">When you set the **Echo On** argument to **No**, the macro runs without updating the screen.</span></span> <span data-ttu-id="ad0c3-119">После завершения макроса Access автоматически включает эхо и повторно обновляет окно.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-119">When the macro finishes, Access automatically turns echo back on and repaints the window.</span></span> <span data-ttu-id="ad0c3-120">Параметр **"Нет"** для аргумента **Echo On** не влияет на функциональность макроса и его результаты.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-120">The **No** setting for the **Echo On** argument doesn't affect the functionality of the macro or its results.</span></span>

<span data-ttu-id="ad0c3-121">Действие **Echo** не подавляет отображение модальных диалоговых окной, таких как сообщения об ошибках или всплывающие формы, такие как листы свойств.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-121">The **Echo** action doesn't suppress the display of modal dialog boxes, such as error messages, or pop-up forms, such as property sheets.</span></span> <span data-ttu-id="ad0c3-122">Для сбора или отображения информации можно использовать диалоговое окно и всплывающие формы, даже если эхо отключено.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-122">You can use dialog boxes and pop-up forms to gather or display information, even if echo is turned off.</span></span> <span data-ttu-id="ad0c3-123">Чтобы подавлять все сообщения или диалоги, кроме полей сообщений об ошибках и диалогов, которые требуют ввода информации пользователем, используйте действие **SetWarnings.**</span><span class="sxs-lookup"><span data-stu-id="ad0c3-123">To suppress all message or dialog boxes except error message boxes and dialog boxes that require the user to enter information, use the **SetWarnings** action.</span></span>

<span data-ttu-id="ad0c3-124">Макрос может **запускать макрос** несколько раз.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-124">You can run the **Echo** action more than once in a macro.</span></span> <span data-ttu-id="ad0c3-125">Это позволяет изменять текст в панели состояния во время макроса.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-125">This allows you to change the status bar text while the macro runs.</span></span>

<span data-ttu-id="ad0c3-126">Если вы отключите эхо, вы можете использовать действие **DisplayHourglassPointer,** чтобы изменить указатель мыши на значок песочных часов (или любой значок указателя мыши, заданный для "Занят"), чтобы показать, что макрос запущен.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-126">If you turn echo off, you can use the **DisplayHourglassPointer** action to change the mouse pointer into an hourglass icon (or whatever mouse pointer icon you've set for "Busy") to provide a visual indication that the macro is running.</span></span>

<span data-ttu-id="ad0c3-127">Чтобы запустить действие **Echo** в модуле Visual Basic для приложений (VBA), используйте метод **Echo** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="ad0c3-127">To run the **Echo** action in a Visual Basic for Applications (VBA) module, use the **Echo** method of the **DoCmd** object.</span></span>

## <a name="examples"></a><span data-ttu-id="ad0c3-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="ad0c3-128">Examples</span></span>

### <a name="set-the-value-of-a-control-by-using-a-macro"></a><span data-ttu-id="ad0c3-129">Установка значения элемента управления с помощью макроса</span><span class="sxs-lookup"><span data-stu-id="ad0c3-129">Set the value of a control by using a macro</span></span>

<span data-ttu-id="ad0c3-130">Следующий макрос открывает форму "Добавить товары" с помощью кнопки в форме "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="ad0c3-130">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="ad0c3-131">Он демонстрирует применение макрокоманд **ВыводНаЭкран**, **ЗакрытьОкно**, **ОткрытьФорму**, **ЗадатьЗначение** и **КЭлементуУправления**.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-131">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="ad0c3-132">Действие **SetValue** задает для контроля "ИД поставщика" в форме "Продукты" текущего поставщика в форме "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="ad0c3-132">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="ad0c3-133">Затем **действие GoToControl** перемещает фокус на поле "ИД категории", где можно начать ввод данных для нового продукта.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-133">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="ad0c3-134">Этот макрос должен быть привязан к кнопке "Добавить товары" в форме "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="ad0c3-134">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ad0c3-135">Макрокоманда</span><span class="sxs-lookup"><span data-stu-id="ad0c3-135">Action</span></span></p></th>
<th><p><span data-ttu-id="ad0c3-136">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="ad0c3-136">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="ad0c3-137">Примечание</span><span class="sxs-lookup"><span data-stu-id="ad0c3-137">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad0c3-138"><strong>ВыводНаЭкран</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-138"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="ad0c3-139"><strong>Включить вывод</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-139"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="ad0c3-140">Приостанавливает обновление экрана, пока выполняется макрос.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-140">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad0c3-141"><strong>ЗакрытьОкно</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-141"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="ad0c3-142"><strong>Тип объекта</strong>: <strong>FormObject Имя</strong>: Список товаров <strong>Сохранить</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-142"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="ad0c3-143">Закрывает форму "Список товаров".</span><span class="sxs-lookup"><span data-stu-id="ad0c3-143">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad0c3-144"><strong>ОткрытьФорму</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-144"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="ad0c3-145"><strong>Имя формы</strong>: Товары <strong>Представление</strong>: <strong>FormData Режим</strong>: <strong>AddWindow Режим</strong>: <strong>Обычный</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-145"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="ad0c3-146">Открывает форму "Товары".</span><span class="sxs-lookup"><span data-stu-id="ad0c3-146">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad0c3-147"><strong>ЗадатьЗначение</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-147"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="ad0c3-148"><strong>Элемент</strong>: [Forms]![Товары]![КодПоставщика] <strong>Выражение</strong>: КодПоставщика</span><span class="sxs-lookup"><span data-stu-id="ad0c3-148"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="ad0c3-149">Установите для управления "ИД поставщика" текущего поставщика в форме "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="ad0c3-149">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad0c3-150"><strong>КЭлементуУправления</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-150"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="ad0c3-151"><strong>Имя элемента управления</strong>: КодКатегории</span><span class="sxs-lookup"><span data-stu-id="ad0c3-151"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="ad0c3-152">Перейдите к окни управления "ИД категории".</span><span class="sxs-lookup"><span data-stu-id="ad0c3-152">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a><span data-ttu-id="ad0c3-153">Синхронизация форм с помощью макроса</span><span class="sxs-lookup"><span data-stu-id="ad0c3-153">Synchronize forms by using a macro</span></span>

<span data-ttu-id="ad0c3-154">Следующий макрос открывает форму "Список продуктов" в правом нижнем углу формы "Поставщики", отображая продукты текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-154">The following macro opens the Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="ad0c3-155">Здесь показано использование действий **Echo,** **MessageBox,** **GoToControl,** **StopMacro,** **OpenForm** и **MoveAndSizeWindow.**</span><span class="sxs-lookup"><span data-stu-id="ad0c3-155">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="ad0c3-156">Здесь также показано использование условного выражения с действиями **MessageBox,** **GoToControl** и **StopMacro.**</span><span class="sxs-lookup"><span data-stu-id="ad0c3-156">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="ad0c3-157">Этот макрос следует прикрепить к кнопке "Обзор продуктов" в форме "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="ad0c3-157">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ad0c3-158">Condition</span><span class="sxs-lookup"><span data-stu-id="ad0c3-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="ad0c3-159">Макрокоманда</span><span class="sxs-lookup"><span data-stu-id="ad0c3-159">Action</span></span></p></th>
<th><p><span data-ttu-id="ad0c3-160">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="ad0c3-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="ad0c3-161">Примечание</span><span class="sxs-lookup"><span data-stu-id="ad0c3-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ad0c3-162"><strong>ВыводНаЭкран</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="ad0c3-163"><strong>Включить вывод</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="ad0c3-164">Приостанавливает обновление экрана, пока выполняется макрос.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad0c3-165">IsNull([ИД поставщика])</span><span class="sxs-lookup"><span data-stu-id="ad0c3-165">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="ad0c3-166"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="ad0c3-167"><strong>Сообщение:</strong>перейдите к записи поставщика, продукты которой вы хотите просмотреть, а затем снова нажмите кнопку "Просмотреть продукты".</span><span class="sxs-lookup"><span data-stu-id="ad0c3-167"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="ad0c3-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span><span class="sxs-lookup"><span data-stu-id="ad0c3-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="ad0c3-169">Если в форме "Поставщики" нет текущего поставщика, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-169">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad0c3-170">...</span><span class="sxs-lookup"><span data-stu-id="ad0c3-170">...</span></span></p></td>
<td><p><span data-ttu-id="ad0c3-171"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-171"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="ad0c3-172"><strong>Имя управления</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="ad0c3-172"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="ad0c3-173">Переместите фокус на управление CompanyName.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-173">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad0c3-174">...</span><span class="sxs-lookup"><span data-stu-id="ad0c3-174">...</span></span></p></td>
<td><p><span data-ttu-id="ad0c3-175"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-175"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ad0c3-176">Остановите макрос.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-176">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ad0c3-177"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-177"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="ad0c3-178"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]! [Поставщики]! [SupplierID] <strong>Режим данных:</strong> <strong>режим только чтенияWindow</strong>: <strong>обычный</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-178"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="ad0c3-179">Откройте форму "Список продуктов" и откажите продукты текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="ad0c3-179">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="ad0c3-180"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="ad0c3-180"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="ad0c3-181"><strong>Right</strong>: 0.7799 &quot; <strong>Down</strong>: 1.8&quot;</span><span class="sxs-lookup"><span data-stu-id="ad0c3-181"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="ad0c3-182">Расположить форму "Список продуктов" в правом нижнем правом месте формы "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="ad0c3-182">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

