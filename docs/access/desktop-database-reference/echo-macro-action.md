---
title: Макрокоманда Echo макрос (Справочник по базам данных Access на компьютере)
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
# <a name="echo-macro-action"></a><span data-ttu-id="f95e7-102">Макрокоманда Echo</span><span class="sxs-lookup"><span data-stu-id="f95e7-102">Echo macro action</span></span>

<span data-ttu-id="f95e7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f95e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f95e7-104">Вы можете использовать макрокоманду **echo (Echo** ), чтобы указать, включена ли функция Echo.</span><span class="sxs-lookup"><span data-stu-id="f95e7-104">You can use the **Echo** action to specify whether echo is turned on.</span></span> <span data-ttu-id="f95e7-105">Например, это действие можно использовать для скрытия или отображения результатов макроса во время его выполнения.</span><span class="sxs-lookup"><span data-stu-id="f95e7-105">For example, you can use this action to hide or show the results of a macro while it runs.</span></span>

## <a name="setting"></a><span data-ttu-id="f95e7-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="f95e7-106">Setting</span></span>

> [!NOTE]
> <span data-ttu-id="f95e7-107">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="f95e7-107">This action will not be allowed if the database is not trusted.</span></span>

<span data-ttu-id="f95e7-108">Макрокоманда **echo** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="f95e7-108">The **Echo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f95e7-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="f95e7-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f95e7-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f95e7-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f95e7-111"><strong>Включить эхо</strong></span><span class="sxs-lookup"><span data-stu-id="f95e7-111"><strong>Echo On</strong></span></span></p></td>
<td><p><span data-ttu-id="f95e7-112">Выберите <strong>Да</strong> (включить эхо) или <strong>нет</strong> (отключить эхо) в поле <strong>echo вкл</strong> в разделе <strong>аргументы макрокоманды</strong> в области построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="f95e7-112">Click <strong>Yes</strong> (turn echo on) or <strong>No</strong> (turn echo off) in the <strong>Echo On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="f95e7-113">Значение по умолчанию — <strong>Yes</strong>.</span><span class="sxs-lookup"><span data-stu-id="f95e7-113">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f95e7-114"><strong>Текст в строке состояния</strong></span><span class="sxs-lookup"><span data-stu-id="f95e7-114"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="f95e7-115">Текст, отображаемый в строке состояния, когда режим Echo отключен.</span><span class="sxs-lookup"><span data-stu-id="f95e7-115">The text to display in the status bar when echo is turned off.</span></span> <span data-ttu-id="f95e7-116">Например, если функция Echo отключена, в строке состояния может отображаться &quot;макрос работает.&quot;</span><span class="sxs-lookup"><span data-stu-id="f95e7-116">For example, when echo is turned off, the status bar can display &quot;The macro is running.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f95e7-117">При запуске макроса часто отображает сведения, не необходимые для работы макроса.</span><span class="sxs-lookup"><span data-stu-id="f95e7-117">When a macro runs, screen updating often shows information not essential to the functioning of the macro.</span></span> <span data-ttu-id="f95e7-118">Если для аргумента **echo on** задано значение **нет**, макрос запускается без обновления экрана.</span><span class="sxs-lookup"><span data-stu-id="f95e7-118">When you set the **Echo On** argument to **No**, the macro runs without updating the screen.</span></span> <span data-ttu-id="f95e7-119">Когда макрос закончится, Access автоматически включит Echo обратно и перерисовывает окно.</span><span class="sxs-lookup"><span data-stu-id="f95e7-119">When the macro finishes, Access automatically turns echo back on and repaints the window.</span></span> <span data-ttu-id="f95e7-120">Параметр **No** для аргумента **echo on** не влияет на функциональность макроса или его результаты.</span><span class="sxs-lookup"><span data-stu-id="f95e7-120">The **No** setting for the **Echo On** argument doesn't affect the functionality of the macro or its results.</span></span>

<span data-ttu-id="f95e7-121">Действие **echo** не отключает отображение модальных диалоговых окон, например сообщений об ошибках или всплывающих форм, таких как страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="f95e7-121">The **Echo** action doesn't suppress the display of modal dialog boxes, such as error messages, or pop-up forms, such as property sheets.</span></span> <span data-ttu-id="f95e7-122">Вы можете использовать диалоговые окна и всплывающие формы для сбора и отображения данных, даже если режим эхо отключен.</span><span class="sxs-lookup"><span data-stu-id="f95e7-122">You can use dialog boxes and pop-up forms to gather or display information, even if echo is turned off.</span></span> <span data-ttu-id="f95e7-123">Чтобы отключить все сообщения и диалоговые окна, за исключением окон сообщений об ошибках и диалоговых окон, в которых пользователь должен ввести сведения, используйте действие **сетварнингс** .</span><span class="sxs-lookup"><span data-stu-id="f95e7-123">To suppress all message or dialog boxes except error message boxes and dialog boxes that require the user to enter information, use the **SetWarnings** action.</span></span>

<span data-ttu-id="f95e7-124">В макросе можно выполнить макрокоманду **echo** несколько раз.</span><span class="sxs-lookup"><span data-stu-id="f95e7-124">You can run the **Echo** action more than once in a macro.</span></span> <span data-ttu-id="f95e7-125">Это позволяет изменить текст строки состояния во время выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="f95e7-125">This allows you to change the status bar text while the macro runs.</span></span>

<span data-ttu-id="f95e7-126">Если отключить режим Echo, вы можете использовать действие **дисплайхаургласспоинтер** , чтобы изменить указатель мыши на значок песочных часов (или любой значок указателя мыши, заданный для "занято"), чтобы предоставить визуальную индикацию запуска макроса.</span><span class="sxs-lookup"><span data-stu-id="f95e7-126">If you turn echo off, you can use the **DisplayHourglassPointer** action to change the mouse pointer into an hourglass icon (or whatever mouse pointer icon you've set for "Busy") to provide a visual indication that the macro is running.</span></span>

<span data-ttu-id="f95e7-127">Чтобы выполнить макрокоманду **echo** в модуле Visual Basic для приложений (VBA), используйте метод **echo** объекта DoCmd. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f95e7-127">To run the **Echo** action in a Visual Basic for Applications (VBA) module, use the **Echo** method of the **DoCmd** object.</span></span>

## <a name="examples"></a><span data-ttu-id="f95e7-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="f95e7-128">Examples</span></span>

### <a name="set-the-value-of-a-control-by-using-a-macro"></a><span data-ttu-id="f95e7-129">Задание значения элемента управления с помощью макроса</span><span class="sxs-lookup"><span data-stu-id="f95e7-129">Set the value of a control by using a macro</span></span>

<span data-ttu-id="f95e7-130">Следующий макрос открывает форму "Добавление продуктов" на кнопке в форме "поставщики".</span><span class="sxs-lookup"><span data-stu-id="f95e7-130">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="f95e7-131">В нем показано использование действий **echo**, **клосевиндов**, **OpenForm**, **SetValue**и **КЭлементуУправления** .</span><span class="sxs-lookup"><span data-stu-id="f95e7-131">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="f95e7-132">Действие **SetValue** устанавливает для элемента управления "идентификатор поставщика" в форме "продукты" текущего поставщика в форме "поставщики".</span><span class="sxs-lookup"><span data-stu-id="f95e7-132">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="f95e7-133">После этого действие " **КЭлементуУправления** " переместит фокус на поле "идентификатор категории", в котором можно начать ввод данных для нового продукта.</span><span class="sxs-lookup"><span data-stu-id="f95e7-133">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="f95e7-134">Этот макрос должен быть присоединен к кнопке "добавить продукты" в форме "поставщики".</span><span class="sxs-lookup"><span data-stu-id="f95e7-134">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f95e7-135">Действие</span><span class="sxs-lookup"><span data-stu-id="f95e7-135">Action</span></span></p></th>
<th><p><span data-ttu-id="f95e7-136">Аргументы: Настройка</span><span class="sxs-lookup"><span data-stu-id="f95e7-136">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="f95e7-137">Комментарий</span><span class="sxs-lookup"><span data-stu-id="f95e7-137">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f95e7-138"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="f95e7-138"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="f95e7-139"><strong>Echo on</strong>: <strong>нет</strong></span><span class="sxs-lookup"><span data-stu-id="f95e7-139"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="f95e7-140">Остановить обновление экрана во время выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="f95e7-140">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f95e7-141"><strong>Клосевиндов</strong></span><span class="sxs-lookup"><span data-stu-id="f95e7-141"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="f95e7-142"><strong>Тип объекта</strong>: <strong>Формобжект Name</strong>: List Product <strong>Save</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="f95e7-142"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="f95e7-143">Закройте форму "список товаров".</span><span class="sxs-lookup"><span data-stu-id="f95e7-143">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f95e7-144"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="f95e7-144"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="f95e7-145"><strong>Имя формы</strong>: " <strong>Просмотр</strong>продуктов: <strong>режим формдата</strong>: режим <strong>аддвиндов</strong>: <strong>обычный</strong> "</span><span class="sxs-lookup"><span data-stu-id="f95e7-145"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="f95e7-146">Откройте форму продукты.</span><span class="sxs-lookup"><span data-stu-id="f95e7-146">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f95e7-147"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="f95e7-147"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="f95e7-148"><strong>Элемент</strong>: [Forms]! [Products]! Ключев <strong>Выражение</strong>: КодПоставщика</span><span class="sxs-lookup"><span data-stu-id="f95e7-148"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="f95e7-149">В форме Поставщики задайте для элемента управления "идентификатор поставщика" текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="f95e7-149">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f95e7-150"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="f95e7-150"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="f95e7-151"><strong>Имя элемента управления</strong>: КодТипа</span><span class="sxs-lookup"><span data-stu-id="f95e7-151"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="f95e7-152">Перейдите к элементу управления ИДЕНТИФИКАТОРом категории.</span><span class="sxs-lookup"><span data-stu-id="f95e7-152">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a><span data-ttu-id="f95e7-153">Синхронизация форм с помощью макроса</span><span class="sxs-lookup"><span data-stu-id="f95e7-153">Synchronize forms by using a macro</span></span>

<span data-ttu-id="f95e7-154">Следующий макрос открывает форму списка товаров в правом нижнем углу формы поставщики, в которой отображаются продукты текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="f95e7-154">The following macro opens the Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="f95e7-155">В нем показано использование действий **echo**, **MessageBox**, **КЭлементуУправления**, **Макрокоманда StopMacro**, **OpenForm**и **мовеандсизевиндов** .</span><span class="sxs-lookup"><span data-stu-id="f95e7-155">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="f95e7-156">В нем также показано использование условного выражения с действиями **MessageBox**, **КЭлементуУправления**и **Макрокоманда StopMacro** .</span><span class="sxs-lookup"><span data-stu-id="f95e7-156">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="f95e7-157">Этот макрос необходимо прикрепить к кнопке "проверить продукты" в форме "поставщики".</span><span class="sxs-lookup"><span data-stu-id="f95e7-157">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f95e7-158">Условие</span><span class="sxs-lookup"><span data-stu-id="f95e7-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="f95e7-159">Действие</span><span class="sxs-lookup"><span data-stu-id="f95e7-159">Action</span></span></p></th>
<th><p><span data-ttu-id="f95e7-160">Аргументы: Настройка</span><span class="sxs-lookup"><span data-stu-id="f95e7-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="f95e7-161">Комментарий</span><span class="sxs-lookup"><span data-stu-id="f95e7-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="f95e7-162"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="f95e7-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="f95e7-163"><strong>Echo on</strong>: <strong>нет</strong></span><span class="sxs-lookup"><span data-stu-id="f95e7-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="f95e7-164">Остановить обновление экрана во время выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="f95e7-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f95e7-165">IsNull ([идентификатор поставщика])</span><span class="sxs-lookup"><span data-stu-id="f95e7-165">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="f95e7-166"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="f95e7-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="f95e7-167"><strong>Сообщение</strong>: перейдите к записи поставщика, продукты которой вы хотите просмотреть, а затем снова нажмите кнопку Просмотр продуктов.</span><span class="sxs-lookup"><span data-stu-id="f95e7-167"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="f95e7-168"><strong>Beep</strong>: <strong>естипе</strong>: <strong>нонетитле</strong>: выберите поставщика</span><span class="sxs-lookup"><span data-stu-id="f95e7-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="f95e7-169">Если в форме Поставщики нет текущего поставщика, отобразите сообщение.</span><span class="sxs-lookup"><span data-stu-id="f95e7-169">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f95e7-170">...</span><span class="sxs-lookup"><span data-stu-id="f95e7-170"></span></span></p></td>
<td><p><span data-ttu-id="f95e7-171"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="f95e7-171"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="f95e7-172"><strong>Имя элемента управления</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="f95e7-172"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="f95e7-173">Перемещение фокуса на элемент управления CompanyName.</span><span class="sxs-lookup"><span data-stu-id="f95e7-173">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f95e7-174">...</span><span class="sxs-lookup"><span data-stu-id="f95e7-174"></span></span></p></td>
<td><p><span data-ttu-id="f95e7-175"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="f95e7-175"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="f95e7-176">Остановка макроса.</span><span class="sxs-lookup"><span data-stu-id="f95e7-176">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="f95e7-177"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="f95e7-177"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="f95e7-178"><strong>Имя формы</strong>: <strong>представление</strong>списка продуктов: <strong>даташитфилтер Name</strong>: <strong>WHERE Condition</strong>: [ID поставщика] = [Forms]! [Поставщики]! Ключев <strong>Режим данных</strong>: <strong>режим чтения онливиндов</strong>: <strong>обычный</strong></span><span class="sxs-lookup"><span data-stu-id="f95e7-178"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="f95e7-179">Откройте форму Список продуктов и отобразите текущие продукты поставщика.</span><span class="sxs-lookup"><span data-stu-id="f95e7-179">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="f95e7-180"><strong>Мовеандсизевиндов</strong></span><span class="sxs-lookup"><span data-stu-id="f95e7-180"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="f95e7-181"><strong>Right</strong>: 0,7799&quot; <strong>вниз</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="f95e7-181"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="f95e7-182">РасПоложите форму списка товаров в правом нижнем углу формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="f95e7-182">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

