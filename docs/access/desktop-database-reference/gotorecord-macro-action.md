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
# <a name="gotorecord-macro-action"></a><span data-ttu-id="fc8a2-102">Макрокоманда GoToRecord</span><span class="sxs-lookup"><span data-stu-id="fc8a2-102">GoToRecord macro action</span></span>


<span data-ttu-id="fc8a2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc8a2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fc8a2-104">Вы можете использовать макрокоманду **GoToRecord (GoToRecord** ), чтобы сделать указанную запись текущей записью в открытой таблице, форме или наборе результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-104">You can use the **GoToRecord** action to make the specified record the current record in an open table, form, or query result set.</span></span>

## <a name="setting"></a><span data-ttu-id="fc8a2-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="fc8a2-105">Setting</span></span>

<span data-ttu-id="fc8a2-106">Макрокоманда **GoToRecord** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-106">The **GoToRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc8a2-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="fc8a2-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="fc8a2-108">Описание</span><span class="sxs-lookup"><span data-stu-id="fc8a2-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc8a2-109"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="fc8a2-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="fc8a2-110">Тип объекта, который содержит запись, которую необходимо сделать текущей.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-110">The type of object that contains the record you want to make current.</span></span> <span data-ttu-id="fc8a2-111">Щелкните <strong>Таблица</strong>, <strong>запрос</strong>, <strong>форма</strong>, <strong>серверное представление</strong>, <strong>хранимая процедура</strong>или <strong>функция</strong> в поле <strong>тип объекта</strong> в разделе <strong>аргументы макрокоманды</strong> в области построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-111">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="fc8a2-112">Чтобы выбрать активный объект, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-112">Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc8a2-113"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="fc8a2-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="fc8a2-114">Имя объекта, содержащего запись, которую необходимо сделать текущей.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-114">The name of the object that contains the record you want to make the current record.</span></span> <span data-ttu-id="fc8a2-115">В поле <strong>имя объекта</strong> отображаются все объекты текущей базы данных с типом, выбранным аргументом <strong>тип объекта</strong> .</span><span class="sxs-lookup"><span data-stu-id="fc8a2-115">The <strong>Object Name</strong> box shows all objects in the current database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="fc8a2-116">Если оставить аргумент " <strong>тип объекта</strong> " пустым, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-116">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc8a2-117"><strong>Record</strong></span><span class="sxs-lookup"><span data-stu-id="fc8a2-117"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="fc8a2-118">Запись для создания текущей записи.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-118">The record to make the current record.</span></span> <span data-ttu-id="fc8a2-119">В поле <strong>запись</strong> выберите <strong>предыдущий</strong>, <strong>следующий</strong>, <strong>первый</strong>, <strong>последний</strong>, или <strong>Новый</strong> . <strong></strong></span><span class="sxs-lookup"><span data-stu-id="fc8a2-119">Click <strong>Previous</strong>, <strong>Next</strong>, <strong>First</strong>, <strong>Last</strong>, <strong>Go To</strong>, or <strong>New</strong> in the <strong>Record</strong> box.</span></span> <span data-ttu-id="fc8a2-120">Значение по умолчанию — <strong>Next (далее</strong>).</span><span class="sxs-lookup"><span data-stu-id="fc8a2-120">The default is <strong>Next</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc8a2-121"><strong>Offset</strong></span><span class="sxs-lookup"><span data-stu-id="fc8a2-121"><strong>Offset</strong></span></span></p></td>
<td><p><span data-ttu-id="fc8a2-122">Целое число или выражение, которое вычисляется как целое число.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-122">An integer or expression that evaluates to an integer.</span></span> <span data-ttu-id="fc8a2-123">Перед выражением должен стоять знак равенства (<strong>=</strong>).</span><span class="sxs-lookup"><span data-stu-id="fc8a2-123">An expression must be preceded by an equal sign (<strong>=</strong>).</span></span> <span data-ttu-id="fc8a2-124">Этот аргумент указывает запись для создания текущей записи.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-124">This argument specifies the record to make the current record.</span></span> <span data-ttu-id="fc8a2-125">Аргумент <strong>СМЕЩ</strong> можно использовать двумя способами:</span><span class="sxs-lookup"><span data-stu-id="fc8a2-125">You can use the <strong>Offset</strong> argument in two ways:</span></span></p>
<ul>
<li><p><span data-ttu-id="fc8a2-126">Если аргумент <strong>Record</strong> находится в <strong>следующей</strong> или <strong>предыдущей</strong>версии, Microsoft Office Access 2007 перемещает число записей, указанных в аргументе <strong>СМЕЩ</strong> , вперед или назад.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-126">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="fc8a2-127">Когда используется аргумент <strong>Record</strong> , <strong></strong>Access перемещается к записи с номером, равным значению аргумента <strong>offset</strong> .</span><span class="sxs-lookup"><span data-stu-id="fc8a2-127">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument.</span></span> <span data-ttu-id="fc8a2-128">Номер записи отображается в поле номера записи в нижней части окна.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-128">The record number is shown in the record number box at the bottom of the window.</span></span></p>
<p><span data-ttu-id="fc8a2-129"><strong>Note</strong>: Если вы используете <strong>первый</strong>, <strong>последний</strong>или <strong>Новый</strong> параметр в аргументе <strong>Record</strong> , Access игнорирует аргумент <strong>СМЕЩ</strong> .</span><span class="sxs-lookup"><span data-stu-id="fc8a2-129"><strong>NOTE</strong>: If you use the <strong>First</strong>, <strong>Last</strong>, or <strong>New</strong> setting for the <strong>Record</strong> argument, Access ignores the <strong>Offset</strong> argument.</span></span> <span data-ttu-id="fc8a2-130">Если ввести слишком большой аргумент <strong>смещения</strong> , Access выведет сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-130">If you enter an <strong>Offset</strong> argument that is too large, Access displays an error message.</span></span> <span data-ttu-id="fc8a2-131">Вы не можете вводить отрицательные числа для аргумента <strong>СМЕЩ</strong> .</span><span class="sxs-lookup"><span data-stu-id="fc8a2-131">You can't enter negative numbers for the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="fc8a2-132">Если аргумент <strong>Record</strong> находится в <strong>следующей</strong> или <strong>предыдущей</strong>версии, Microsoft Office Access 2007 перемещает число записей, указанных в аргументе <strong>СМЕЩ</strong> , вперед или назад.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-132">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="fc8a2-133">Когда используется аргумент <strong>Record</strong> , <strong></strong>Access перемещается к записи с номером, равным значению аргумента <strong>offset</strong> .</span><span class="sxs-lookup"><span data-stu-id="fc8a2-133">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument.</span></span> <span data-ttu-id="fc8a2-134">Номер записи отображается в поле номера записи в нижней части окна.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-134">The record number is shown in the record number box at the bottom of the window.</span></span></p></li>
</ul>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fc8a2-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="fc8a2-135">Remarks</span></span>

<span data-ttu-id="fc8a2-136">Если фокус находится в определенном элементе управления в записи, это действие оставляет его в том же элементе управления для новой записи.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-136">If the focus is in a particular control in a record, this action leaves it in the same control for the new record.</span></span>

<span data-ttu-id="fc8a2-137">Вы можете использовать параметр **New** для аргумента **Record** , чтобы переместиться на пустую запись в конце формы или таблицы, чтобы можно было вводить новые данные.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-137">You can use the **New** setting for the **Record** argument to move to the blank record at the end of a form or table so you can enter new data.</span></span>

<span data-ttu-id="fc8a2-138">Это действие аналогично щелчку стрелки под кнопкой **найти** на вкладке **Главная** и нажатием кнопки **Перейти**.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-138">This action is similar to clicking the arrow below the **Find** button on the **Home** tab and then clicking **Go To**.</span></span> <span data-ttu-id="fc8a2-139">**Первый**, **последний**, **следующий**, **предыдущий**и **Новый** подкоманды команды **Перейти** к выбранному объекту будут иметь одинаковое значение в **первом**, **последнем**, **следующем**, **предыдущем**, и **новые** параметры для аргумента **Record** .</span><span class="sxs-lookup"><span data-stu-id="fc8a2-139">The **First**, **Last**, **Next**, **Previous**, and **New Record** subcommands of the **Go To** command have the same effect on the selected object as the **First**, **Last**, **Next**, **Previous**, and **New** settings for the **Record** argument.</span></span> <span data-ttu-id="fc8a2-140">Кроме того, можно перейти к записям с помощью кнопок навигации в нижней части окна.</span><span class="sxs-lookup"><span data-stu-id="fc8a2-140">You can also move to records by using the navigation buttons at the bottom of the window.</span></span>

<span data-ttu-id="fc8a2-141">Вы можете использовать макрокоманду **GoToRecord (GoToRecord** ), чтобы сделать запись в скрытой форме текущей записью, если указать скрытую форму в аргументах **тип объекта** и **имя объекта** .</span><span class="sxs-lookup"><span data-stu-id="fc8a2-141">You can use the **GoToRecord** action to make a record on a hidden form the current record if you specify the hidden form in the **Object Type** and **Object Name** arguments.</span></span>

<span data-ttu-id="fc8a2-142">Чтобы выполнить макрокоманду **GoToRecord** в модуле Visual Basic для приложений (VBA), используйте метод **GoToRecord** объекта DoCmd. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="fc8a2-142">To run the **GoToRecord** action in a Visual Basic for Applications (VBA) module, use the **GoToRecord** method of the **DoCmd** object.</span></span>

