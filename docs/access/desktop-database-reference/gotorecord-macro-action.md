---
title: Макрокоманда GoToRecord
TOCTitle: GoToRecord macro action
ms:assetid: 76f936de-739b-63be-9b28-5b0e111408e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196037(v=office.15)
ms:contentKeyID: 48545712
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm58124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7534ae84b57d14450009865ea330a4c54d4cfb44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292141"
---
# <a name="gotorecord-macro-action"></a><span data-ttu-id="b4d3d-102">Макрокоманда GoToRecord</span><span class="sxs-lookup"><span data-stu-id="b4d3d-102">GoToRecord macro action</span></span>


<span data-ttu-id="b4d3d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4d3d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4d3d-104">Вы можете использовать **действие GoToRecord,** чтобы фиксировать текущую запись в наборе результатов открытой таблицы, формы или запроса.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-104">You can use the **GoToRecord** action to make the specified record the current record in an open table, form, or query result set.</span></span>

## <a name="setting"></a><span data-ttu-id="b4d3d-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="b4d3d-105">Setting</span></span>

<span data-ttu-id="b4d3d-106">Действие **GoToRecord имеет** следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-106">The **GoToRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4d3d-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="b4d3d-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b4d3d-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b4d3d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4d3d-109"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="b4d3d-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="b4d3d-110">Тип объекта, который содержит запись, которую необходимо сделать текущим.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-110">The type of object that contains the record you want to make current.</span></span> <span data-ttu-id="b4d3d-111">Щелкните таблицу, <strong></strong> <strong>запрос,</strong> <strong>форму,</strong>представление <strong></strong> <strong>сервера,</strong>сохраненную процедуру <strong></strong> <strong>или</strong>функцию в поле Тип объекта в разделе Аргументы действий области Macro Builder. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="b4d3d-111">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="b4d3d-112">Оставьте этот аргумент пустым, чтобы выбрать активный объект.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-112">Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4d3d-113"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="b4d3d-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b4d3d-114">Имя объекта, который содержит запись, которую необходимо сделать текущей записью.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-114">The name of the object that contains the record you want to make the current record.</span></span> <span data-ttu-id="b4d3d-115">Поле <strong>Имя объекта</strong> отображает все объекты текущей базы данных типа, выбранного <strong>аргументом Object Type.</strong></span><span class="sxs-lookup"><span data-stu-id="b4d3d-115">The <strong>Object Name</strong> box shows all objects in the current database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="b4d3d-116">Если оставить аргумент <strong>Object Type</strong> пустым, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-116">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4d3d-117"><strong>Record</strong></span><span class="sxs-lookup"><span data-stu-id="b4d3d-117"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="b4d3d-118">Запись, чтобы сделать текущую запись.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-118">The record to make the current record.</span></span> <span data-ttu-id="b4d3d-119">Нажмите <strong>кнопку</strong>Предыдущий , <strong>Далее</strong>, <strong>Первый</strong>, <strong>Последний</strong>, <strong>Перейти к</strong>, или <strong>Новый</strong> в <strong>поле Запись.</strong></span><span class="sxs-lookup"><span data-stu-id="b4d3d-119">Click <strong>Previous</strong>, <strong>Next</strong>, <strong>First</strong>, <strong>Last</strong>, <strong>Go To</strong>, or <strong>New</strong> in the <strong>Record</strong> box.</span></span> <span data-ttu-id="b4d3d-120">По умолчанию <strong>далее</strong>.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-120">The default is <strong>Next</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4d3d-121"><strong>Offset</strong></span><span class="sxs-lookup"><span data-stu-id="b4d3d-121"><strong>Offset</strong></span></span></p></td>
<td><p><span data-ttu-id="b4d3d-122">Integer или выражение, которое оценивается для integer.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-122">An integer or expression that evaluates to an integer.</span></span> <span data-ttu-id="b4d3d-123">Выражению должно предшествовать равный знак ( <strong>=</strong> ).</span><span class="sxs-lookup"><span data-stu-id="b4d3d-123">An expression must be preceded by an equal sign (<strong>=</strong>).</span></span> <span data-ttu-id="b4d3d-124">Этот аргумент указывает запись, чтобы сделать текущую запись.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-124">This argument specifies the record to make the current record.</span></span> <span data-ttu-id="b4d3d-125">Аргумент Offset можно <strong>использовать</strong> двумя способами:</span><span class="sxs-lookup"><span data-stu-id="b4d3d-125">You can use the <strong>Offset</strong> argument in two ways:</span></span></p>
<ul>
<li><p><span data-ttu-id="b4d3d-126">Когда аргумент <strong>Записи</strong> <strong>следующий</strong> или предыдущий, <strong></strong>Microsoft Office Access 2007 перемещает количество записей вперед или назад, указанное в <strong>аргументе Смещение.</strong></span><span class="sxs-lookup"><span data-stu-id="b4d3d-126">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="b4d3d-127">Когда аргумент <strong>Записи</strong> <strong>перейдите к</strong>записи, доступ перемещается к записи с номером, равным <strong>аргументу Смещение.</strong></span><span class="sxs-lookup"><span data-stu-id="b4d3d-127">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument.</span></span> <span data-ttu-id="b4d3d-128">Номер записи отображается в поле записи в нижней части окна.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-128">The record number is shown in the record number box at the bottom of the window.</span></span></p>
<p><span data-ttu-id="b4d3d-129"><strong>ПРИМЕЧАНИЕ.</strong>Если вы используете <strong>первый,</strong> <strong>последний</strong>или новый параметр для аргумента <strong>Запись,</strong> Access игнорирует аргумент <strong>Смещение.</strong> <strong></strong></span><span class="sxs-lookup"><span data-stu-id="b4d3d-129"><strong>NOTE</strong>: If you use the <strong>First</strong>, <strong>Last</strong>, or <strong>New</strong> setting for the <strong>Record</strong> argument, Access ignores the <strong>Offset</strong> argument.</span></span> <span data-ttu-id="b4d3d-130">Если вы вводите слишком большой аргумент <strong>Смещения,</strong> Access отображает сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-130">If you enter an <strong>Offset</strong> argument that is too large, Access displays an error message.</span></span> <span data-ttu-id="b4d3d-131">Для аргумента Смещение нельзя вводить отрицательные <strong>номера.</strong></span><span class="sxs-lookup"><span data-stu-id="b4d3d-131">You can't enter negative numbers for the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="b4d3d-132">Когда аргумент <strong>Записи</strong> <strong>следующий</strong> или предыдущий, <strong></strong>Microsoft Office Access 2007 перемещает количество записей вперед или назад, указанное в <strong>аргументе Смещение.</strong></span><span class="sxs-lookup"><span data-stu-id="b4d3d-132">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="b4d3d-133">Когда аргумент <strong>Записи</strong> <strong>перейдите к</strong>записи, доступ перемещается к записи с номером, равным <strong>аргументу Смещение.</strong></span><span class="sxs-lookup"><span data-stu-id="b4d3d-133">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument.</span></span> <span data-ttu-id="b4d3d-134">Номер записи отображается в поле записи в нижней части окна.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-134">The record number is shown in the record number box at the bottom of the window.</span></span></p></li>
</ul>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b4d3d-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4d3d-135">Remarks</span></span>

<span data-ttu-id="b4d3d-136">Если фокус находится в определенном контроле в записи, это действие оставляет его в том же контроле для новой записи.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-136">If the focus is in a particular control in a record, this action leaves it in the same control for the new record.</span></span>

<span data-ttu-id="b4d3d-137">Вы можете использовать параметр **New** для аргумента **Запись** для перемещения на пустую запись в конце формы или таблицы, чтобы можно было ввести новые данные.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-137">You can use the **New** setting for the **Record** argument to move to the blank record at the end of a form or table so you can enter new data.</span></span>

<span data-ttu-id="b4d3d-138">Это действие аналогично нажатию стрелки ниже кнопки **Найти** на вкладке **Главная,** а затем нажать **кнопку Перейти к**.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-138">This action is similar to clicking the arrow below the **Find** button on the **Home** tab and then clicking **Go To**.</span></span> <span data-ttu-id="b4d3d-139">**Первые,** последние, **последующие,**  предыдущие и новые подкомитеты записи команды **Go To** имеют такое же влияние на  выбранный объект, как **первый,** **последний,** **следующий,** предыдущий и новые параметры для аргумента **Запись.** </span><span class="sxs-lookup"><span data-stu-id="b4d3d-139">The **First**, **Last**, **Next**, **Previous**, and **New Record** subcommands of the **Go To** command have the same effect on the selected object as the **First**, **Last**, **Next**, **Previous**, and **New** settings for the **Record** argument.</span></span> <span data-ttu-id="b4d3d-140">Вы также можете перейти к записям с помощью кнопок навигации в нижней части окна.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-140">You can also move to records by using the navigation buttons at the bottom of the window.</span></span>

<span data-ttu-id="b4d3d-141">Вы можете использовать **действие GoToRecord** для записи в скрытой форме текущей записи,  если указать скрытую форму в аргументах **Типа** объекта и имени объектов.</span><span class="sxs-lookup"><span data-stu-id="b4d3d-141">You can use the **GoToRecord** action to make a record on a hidden form the current record if you specify the hidden form in the **Object Type** and **Object Name** arguments.</span></span>

<span data-ttu-id="b4d3d-142">Чтобы выполнить **действие GoToRecord** в модуле Visual Basic для приложений (VBA), используйте метод **GoToRecord** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="b4d3d-142">To run the **GoToRecord** action in a Visual Basic for Applications (VBA) module, use the **GoToRecord** method of the **DoCmd** object.</span></span>

