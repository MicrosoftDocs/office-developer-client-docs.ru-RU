---
title: Действия макроса эхо (Справочник по для настольных баз данных Access)
TOCTitle: Echo Macro Action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39471ea4bab2ec1bbeb8cd22ecb00aa5df3bc411
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863971"
---
# <a name="echo-macro-action"></a><span data-ttu-id="5863e-102">Действия макроса эхо</span><span class="sxs-lookup"><span data-stu-id="5863e-102">Echo Macro Action</span></span>


<span data-ttu-id="5863e-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5863e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5863e-104">Действие **эхо** можно использовать для определения, включено ли эхо.</span><span class="sxs-lookup"><span data-stu-id="5863e-104">You can use the **Echo** action to specify whether echo is turned on.</span></span> <span data-ttu-id="5863e-105">Например можно использовать это действие скрытие или отображение результатов макроса во время его выполнения.</span><span class="sxs-lookup"><span data-stu-id="5863e-105">For example, you can use this action to hide or show the results of a macro while it runs.</span></span>

## <a name="setting"></a><span data-ttu-id="5863e-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="5863e-106">Setting</span></span>


> [!NOTE]
> <span data-ttu-id="5863e-p102">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="5863e-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>



<span data-ttu-id="5863e-109">Действие **эхо** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="5863e-109">The **Echo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5863e-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="5863e-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5863e-111">Описание</span><span class="sxs-lookup"><span data-stu-id="5863e-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5863e-112"><strong>Включить вывод</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-112"><strong>Echo On</strong></span></span></p></td>
<td><p><span data-ttu-id="5863e-113">Нажмите кнопку <strong>Да</strong> (включает вывод на экран) или <strong>Нет</strong> (отключает вывод) в <strong>Эхо на</strong> поле в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="5863e-113">Click <strong>Yes</strong> (turn echo on) or <strong>No</strong> (turn echo off) in the <strong>Echo On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="5863e-114">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="5863e-114">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5863e-115"><strong>Текст в строке состояния</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-115"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="5863e-116">Текст, отображаемый в строке когда выключена эхо состояния.</span><span class="sxs-lookup"><span data-stu-id="5863e-116">The text to display in the status bar when echo is turned off.</span></span> <span data-ttu-id="5863e-117">Например, при отключении эхо в строке состояния может отображаться &quot;выполнение макроса.&quot;</span><span class="sxs-lookup"><span data-stu-id="5863e-117">For example, when echo is turned off, the status bar can display &quot;The macro is running.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5863e-118">При запуске макроса обновление часто отображаются сведения о несущественные для функционирования макрос экрана.</span><span class="sxs-lookup"><span data-stu-id="5863e-118">When runs a macro, screen updating often shows information not essential to the functioning of the macro.</span></span> <span data-ttu-id="5863e-119">Если аргумент **Эхо на** значение **No**, макрос выполняется без обновления экрана.</span><span class="sxs-lookup"><span data-stu-id="5863e-119">When you set the **Echo On** argument to **No**, the macro runs without updating the screen.</span></span> <span data-ttu-id="5863e-120">После завершения макроса доступа автоматически включает эхо и обновляет окна.</span><span class="sxs-lookup"><span data-stu-id="5863e-120">When the macro finishes, Access automatically turns echo back on and repaints the window.</span></span> <span data-ttu-id="5863e-121">**No** для аргумента **Эхо на** не влияет на функциональность макроса или его результаты.</span><span class="sxs-lookup"><span data-stu-id="5863e-121">The **No** setting for the **Echo On** argument doesn't affect the functionality of the macro or its results.</span></span>

<span data-ttu-id="5863e-122">Действие **эхо** не отображение без модальных диалоговых окон, например, сообщений об ошибках или всплывающих форм, таких как страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="5863e-122">The **Echo** action doesn't suppress the display of modal dialog boxes, such as error messages, or pop-up forms, such as property sheets.</span></span> <span data-ttu-id="5863e-123">Диалоговые окна и всплывающие формы для сбора и отображения данных, можно использовать даже в том случае, если отключено эхо.</span><span class="sxs-lookup"><span data-stu-id="5863e-123">You can use dialog boxes and pop-up forms to gather or display information, even if echo is turned off.</span></span> <span data-ttu-id="5863e-124">Чтобы запретить все сообщения и диалоговых окон за исключением окна сообщений об ошибках и диалоговых окон, которые требуют пользователю требуется ввести сведения, используйте действие **УстановитьСообщения** .</span><span class="sxs-lookup"><span data-stu-id="5863e-124">To suppress all message or dialog boxes except error message boxes and dialog boxes that require the user to enter information, use the **SetWarnings** action.</span></span>

<span data-ttu-id="5863e-125">**Эхо** действие можно выполнить более одного раза в макросе.</span><span class="sxs-lookup"><span data-stu-id="5863e-125">You can run the **Echo** action more than once in a macro.</span></span> <span data-ttu-id="5863e-126">Это позволяет изменить текст в строке состояния во время выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="5863e-126">This allows you to change the status bar text while the macro runs.</span></span>

<span data-ttu-id="5863e-127">При выключении эхо, можно использовать действие **DisplayHourglassPointer** изменение указатель мыши на значок песочными часами (или любое значок указателя мыши, заданные для «Занят») для предоставления визуальный индикатор, на котором выполняется макрос.</span><span class="sxs-lookup"><span data-stu-id="5863e-127">If you turn echo off, you can use the **DisplayHourglassPointer** action to change the mouse pointer into an hourglass icon (or whatever mouse pointer icon you've set for "Busy") to provide a visual indication that the macro is running.</span></span>

<span data-ttu-id="5863e-128">Чтобы выполнить действие **эхо** в Visual Basic для приложений (VBA) модуль, используйте метод **эхо** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="5863e-128">To run the **Echo** action in a Visual Basic for Applications (VBA) module, use the **Echo** method of the **DoCmd** object.</span></span>

## <a name="examples"></a><span data-ttu-id="5863e-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="5863e-129">Examples</span></span>

<span data-ttu-id="5863e-130">**Задайте значение элемента управления с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="5863e-130">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="5863e-131">Следующий макрос открывает форму добавления продуктов с помощью кнопки на форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="5863e-131">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="5863e-132">Демонстрируется использование **эхо**, **CloseWindow**, **ОткрытьФорму**, **SetValue**и **КЭлементуУправления** действий.</span><span class="sxs-lookup"><span data-stu-id="5863e-132">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="5863e-133">Действие **SetValue** задает код поставщика управления на форме продуктов для текущего поставщика в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="5863e-133">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="5863e-134">**Затем КЭлементуУправления** перемещает фокус в поле Идентификатор категории, где можно вводить данные для нового продукта.</span><span class="sxs-lookup"><span data-stu-id="5863e-134">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="5863e-135">Этот макрос должен быть связан с кнопкой Добавить продукты в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="5863e-135">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5863e-136">Действие</span><span class="sxs-lookup"><span data-stu-id="5863e-136">Action</span></span></p></th>
<th><p><span data-ttu-id="5863e-137">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="5863e-137">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="5863e-138">Comment</span><span class="sxs-lookup"><span data-stu-id="5863e-138">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5863e-139"><strong>Эхо</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-139"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="5863e-140"><strong>Вывод на экран</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-140"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="5863e-141">Остановите обновление экрана в процессе выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="5863e-141">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5863e-142"><strong>CloseWindow</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-142"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="5863e-143"><strong>Тип объекта</strong>: <strong>FormObject имя</strong>: продукт списка <strong>Сохранить</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-143"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="5863e-144">Закройте форму списка продуктов.</span><span class="sxs-lookup"><span data-stu-id="5863e-144">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5863e-145"><strong>ОткрытьФорму</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-145"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="5863e-146"><strong>Имя формы</strong>: продуктов <strong>представления</strong>: <strong>FormData режима</strong>: <strong>Режим AddWindow</strong>: <strong>Обычный</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-146"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="5863e-147">Откройте форму продуктов.</span><span class="sxs-lookup"><span data-stu-id="5863e-147">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5863e-148"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-148"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="5863e-149"><strong>Элемент</strong>: [формы]! [Товары]! [Код поставщика] <strong>Выражение</strong>: КодПоставщика</span><span class="sxs-lookup"><span data-stu-id="5863e-149"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="5863e-150">Значение текущего поставщика управления код поставщика в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="5863e-150">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5863e-151"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-151"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="5863e-152"><strong>Имя элемента управления</strong>: идентификатор категории</span><span class="sxs-lookup"><span data-stu-id="5863e-152"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="5863e-153">Перейдите к элементу управления идентификатор категории.</span><span class="sxs-lookup"><span data-stu-id="5863e-153">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5863e-154">**Синхронизация форм с помощью макроса (en)**</span><span class="sxs-lookup"><span data-stu-id="5863e-154">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="5863e-155">Следующий макрос открывает форму списка продуктов в правом нижнем углу формы Поставщики, отображение текущего поставщика продуктов.</span><span class="sxs-lookup"><span data-stu-id="5863e-155">The following macro opens the Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="5863e-156">Демонстрируется использование **эхо**, **MessageBox**, **КЭлементуУправления**, **ОстановитьМакрос**, **ОткрытьФорму**и **MoveAndSizeWindow** действий.</span><span class="sxs-lookup"><span data-stu-id="5863e-156">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="5863e-157">Также показано использование условного выражения с **MessageBox**, **КЭлементуУправления**« **Поставщики** ».</span><span class="sxs-lookup"><span data-stu-id="5863e-157">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="5863e-158">Этот макрос должен быть связан с кнопкой Обзор продуктов в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="5863e-158">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5863e-159">Condition</span><span class="sxs-lookup"><span data-stu-id="5863e-159">Condition</span></span></p></th>
<th><p><span data-ttu-id="5863e-160">Действие</span><span class="sxs-lookup"><span data-stu-id="5863e-160">Action</span></span></p></th>
<th><p><span data-ttu-id="5863e-161">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="5863e-161">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="5863e-162">Comment</span><span class="sxs-lookup"><span data-stu-id="5863e-162">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="5863e-163"><strong>Эхо</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-163"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="5863e-164"><strong>Вывод на экран</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-164"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="5863e-165">Остановите обновление экрана в процессе выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="5863e-165">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5863e-166">Функция IsNull ([код поставщика])</span><span class="sxs-lookup"><span data-stu-id="5863e-166">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="5863e-167"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-167"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="5863e-168"><strong>Сообщение</strong>: перемещение на запись поставщика, продукты, чтобы увидеть, затем нажмите кнопку Предварительный просмотр еще раз.</span><span class="sxs-lookup"><span data-stu-id="5863e-168"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="5863e-169"><strong>Звуковые сигналы</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Выбор поставщика</span><span class="sxs-lookup"><span data-stu-id="5863e-169"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="5863e-170">При отсутствии никто из современных поставщиков в форме Поставщики, отображается сообщение.</span><span class="sxs-lookup"><span data-stu-id="5863e-170">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5863e-171">...</span><span class="sxs-lookup"><span data-stu-id="5863e-171"></span></span></p></td>
<td><p><span data-ttu-id="5863e-172"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-172"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="5863e-173"><strong>Имя элемента управления</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="5863e-173"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="5863e-174">Перемещение фокуса на элемент управления CompanyName.</span><span class="sxs-lookup"><span data-stu-id="5863e-174">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5863e-175">...</span><span class="sxs-lookup"><span data-stu-id="5863e-175"></span></span></p></td>
<td><p><span data-ttu-id="5863e-176"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-176"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5863e-177">Остановка макроса.</span><span class="sxs-lookup"><span data-stu-id="5863e-177">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="5863e-178"><strong>ОткрытьФорму</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-178"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="5863e-179"><strong>Имя формы</strong>: список продуктов <strong>представления</strong>: <strong>Имя DatasheetFilter</strong>: <strong>условие отбора</strong>: [код поставщика] = [Forms]! [Поставщики]! [Код поставщика] <strong>Режим данных</strong>: <strong>Режим чтения OnlyWindow</strong>: <strong>Обычный</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-179"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="5863e-180">Откройте форму списка продуктов и отображение текущего поставщика продуктов.</span><span class="sxs-lookup"><span data-stu-id="5863e-180">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="5863e-181"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="5863e-181"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="5863e-182"><strong>Право</strong>: 0,7799&quot; <strong>вниз</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="5863e-182"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="5863e-183">Положение формы списка продуктов в нижней правой части формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="5863e-183">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

