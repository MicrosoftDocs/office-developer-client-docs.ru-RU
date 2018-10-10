---
title: GoToRecord Macro Action
TOCTitle: GoToRecord Macro Action
ms:assetid: 76f936de-739b-63be-9b28-5b0e111408e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196037(v=office.15)
ms:contentKeyID: 48545712
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm58124
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f7094d95053e97180526523fd41862dfeb100c86
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482375"
---
# <a name="gotorecord-macro-action"></a><span data-ttu-id="dadf9-102">GoToRecord Macro Action</span><span class="sxs-lookup"><span data-stu-id="dadf9-102">GoToRecord Macro Action</span></span>


<span data-ttu-id="dadf9-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dadf9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dadf9-104">Можно использовать действие **НаЗапись** чтобы сделать указанной записи текущей открытой таблицы, формы или набора результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="dadf9-104">You can use the **GoToRecord** action to make the specified record the current record in an open table, form, or query result set.</span></span>

## <a name="setting"></a><span data-ttu-id="dadf9-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="dadf9-105">Setting</span></span>

<span data-ttu-id="dadf9-106">Действие **НаЗапись** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="dadf9-106">The **GoToRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dadf9-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="dadf9-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="dadf9-108">Описание</span><span class="sxs-lookup"><span data-stu-id="dadf9-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dadf9-109"><strong>Тип объекта</strong></span><span class="sxs-lookup"><span data-stu-id="dadf9-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="dadf9-110">Тип объекта, который содержит запись, которую следует сделать текущей.</span><span class="sxs-lookup"><span data-stu-id="dadf9-110">The type of object that contains the record you want to make current.</span></span> <span data-ttu-id="dadf9-111">Выберите <strong>таблицы</strong>, <strong>запроса</strong>, <strong>формы</strong>, <strong>Представление</strong>, <strong>Хранимую процедуру</strong>или <strong>функцию</strong> в поле <strong>Тип объекта</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="dadf9-111">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="dadf9-112">Оставьте данный аргумент пустым, чтобы выбрать активный объект.</span><span class="sxs-lookup"><span data-stu-id="dadf9-112">Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dadf9-113"><strong>Имя объекта</strong></span><span class="sxs-lookup"><span data-stu-id="dadf9-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="dadf9-114">Имя объекта, содержащую запись, который требуется сделать текущей записи.</span><span class="sxs-lookup"><span data-stu-id="dadf9-114">The name of the object that contains the record you want to make the current record.</span></span> <span data-ttu-id="dadf9-115">В поле <strong>Имя объекта</strong> содержит все объекты базы данных, указанному в аргументе <strong>Тип объекта</strong> типа.</span><span class="sxs-lookup"><span data-stu-id="dadf9-115">The <strong>Object Name</strong> box shows all objects in the current database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="dadf9-116">Если <strong>Тип объекта</strong> аргумента оставлено пустым, оставьте аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="dadf9-116">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dadf9-117"><strong>Запись</strong></span><span class="sxs-lookup"><span data-stu-id="dadf9-117"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="dadf9-118">Сделать текущей запись.</span><span class="sxs-lookup"><span data-stu-id="dadf9-118">The record to make the current record.</span></span> <span data-ttu-id="dadf9-119">Нажмите кнопку <strong>Назад</strong>, <strong>Далее</strong>, <strong>первый</strong>, <strong>последний</strong>, <strong>Перейдите к</strong>или <strong>Создать</strong> в поле <strong>записи</strong> .</span><span class="sxs-lookup"><span data-stu-id="dadf9-119">Click <strong>Previous</strong>, <strong>Next</strong>, <strong>First</strong>, <strong>Last</strong>, <strong>Go To</strong>, or <strong>New</strong> in the <strong>Record</strong> box.</span></span> <span data-ttu-id="dadf9-120">Значение по умолчанию — <strong>Далее</strong>.</span><span class="sxs-lookup"><span data-stu-id="dadf9-120">The default is <strong>Next</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dadf9-121"><strong>Смещение</strong></span><span class="sxs-lookup"><span data-stu-id="dadf9-121"><strong>Offset</strong></span></span></p></td>
<td><p><span data-ttu-id="dadf9-122">Целое число или выражение, которое оценивается как целое число.</span><span class="sxs-lookup"><span data-stu-id="dadf9-122">An integer or expression that evaluates to an integer.</span></span> <span data-ttu-id="dadf9-123">Выражение должно предшествовать знак равенства (<strong>=</strong>).</span><span class="sxs-lookup"><span data-stu-id="dadf9-123">An expression must be preceded by an equal sign (<strong>=</strong>).</span></span> <span data-ttu-id="dadf9-124">Этот аргумент определяет записи, чтобы сделать текущей.</span><span class="sxs-lookup"><span data-stu-id="dadf9-124">This argument specifies the record to make the current record.</span></span> <span data-ttu-id="dadf9-125">Аргумент <strong>смещение</strong> можно использовать двумя способами:</span><span class="sxs-lookup"><span data-stu-id="dadf9-125">You can use the <strong>Offset</strong> argument in two ways:</span></span></p>
<ul>
<li><p><span data-ttu-id="dadf9-126">Если аргумент <strong>запись</strong> <strong>следующий</strong> или <strong>Предыдущий</strong>, Microsoft Office Access 2007 перемещает число записей вперед или назад, указанный в аргументе <strong>смещение</strong> .</span><span class="sxs-lookup"><span data-stu-id="dadf9-126">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="dadf9-127">При <strong>записи</strong> аргумент <strong>Перейти к</strong>Access перемещает записи с номером равен <strong>смещение</strong> .</span><span class="sxs-lookup"><span data-stu-id="dadf9-127">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument.</span></span> <span data-ttu-id="dadf9-128">Номер записи отображается в поле номер записи в нижней части окна.</span><span class="sxs-lookup"><span data-stu-id="dadf9-128">The record number is shown in the record number box at the bottom of the window.</span></span></p></li>
</ul>

> [!NOTE]
> <P><span data-ttu-id="dadf9-129">Если используется параметр <STRONG>первого</STRONG>, <STRONG>последнего</STRONG>или <STRONG>Создать</STRONG> <STRONG>запись</STRONG> аргумента <STRONG>смещение</STRONG> игнорируется.</span><span class="sxs-lookup"><span data-stu-id="dadf9-129">If you use the <STRONG>First</STRONG>, <STRONG>Last</STRONG>, or <STRONG>New</STRONG> setting for the <STRONG>Record</STRONG> argument, Access ignores the <STRONG>Offset</STRONG> argument.</span></span> <span data-ttu-id="dadf9-130">Если аргумент <STRONG>смещение</STRONG> слишком большого размера, Access отображает сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="dadf9-130">If you enter an <STRONG>Offset</STRONG> argument that is too large, Access displays an error message.</span></span> <span data-ttu-id="dadf9-131">Нельзя вводить отрицательные числа для аргумента <STRONG>смещение</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="dadf9-131">You can't enter negative numbers for the <STRONG>Offset</STRONG> argument.</span></span></P>


<p></p>
<ul>
<li><p><span data-ttu-id="dadf9-132">Если аргумент <strong>запись</strong> <strong>следующий</strong> или <strong>Предыдущий</strong>, Microsoft Office Access 2007 перемещает число записей вперед или назад, указанный в аргументе <strong>смещение</strong> .</span><span class="sxs-lookup"><span data-stu-id="dadf9-132">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="dadf9-133">При <strong>записи</strong> аргумент <strong>Перейти к</strong>Access перемещает записи с номером равен <strong>смещение</strong> .</span><span class="sxs-lookup"><span data-stu-id="dadf9-133">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument.</span></span> <span data-ttu-id="dadf9-134">Номер записи отображается в поле номер записи в нижней части окна.</span><span class="sxs-lookup"><span data-stu-id="dadf9-134">The record number is shown in the record number box at the bottom of the window.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="dadf9-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="dadf9-135">Remarks</span></span>

<span data-ttu-id="dadf9-136">Если фокус находится в конкретный элемент управления в запись, это действие оставляет его в тот же элемент управления для новой записи.</span><span class="sxs-lookup"><span data-stu-id="dadf9-136">If the focus is in a particular control in a record, this action leaves it in the same control for the new record.</span></span>

<span data-ttu-id="dadf9-137">Параметр **Создать** **запись** для перемещения в пустую запись в конце формы или таблицы, которые можно ввести новые данные.</span><span class="sxs-lookup"><span data-stu-id="dadf9-137">You can use the **New** setting for the **Record** argument to move to the blank record at the end of a form or table so you can enter new data.</span></span>

<span data-ttu-id="dadf9-138">Это действие аналогично щелкнув стрелку под кнопкой **Найти** на вкладке **Главная** и затем нажав кнопку **Перейти**.</span><span class="sxs-lookup"><span data-stu-id="dadf9-138">This action is similar to clicking the arrow below the **Find** button on the **Home** tab and then clicking **Go To**.</span></span> <span data-ttu-id="dadf9-139">**Первый**, **последний**, **Далее**, **Назад**и команд **Новую запись** команды **Перейти к** имеют такой же эффект на выбранный объект, как **первый**, **последний**, **Далее**, **Назад** **Создать** параметры и **запись** .</span><span class="sxs-lookup"><span data-stu-id="dadf9-139">The **First**, **Last**, **Next**, **Previous**, and **New Record** subcommands of the **Go To** command have the same effect on the selected object as the **First**, **Last**, **Next**, **Previous**, and **New** settings for the **Record** argument.</span></span> <span data-ttu-id="dadf9-140">Вы также можете переместить в записи с помощью кнопок перехода в нижней части окна.</span><span class="sxs-lookup"><span data-stu-id="dadf9-140">You can also move to records by using the navigation buttons at the bottom of the window.</span></span>

<span data-ttu-id="dadf9-141">Можно использовать **НаЗапись** , чтобы сделать запись в скрытой форме текущей записи при указании скрытые формы в аргументах **Тип** и **Имя объекта** .</span><span class="sxs-lookup"><span data-stu-id="dadf9-141">You can use the **GoToRecord** action to make a record on a hidden form the current record if you specify the hidden form in the **Object Type** and **Object Name** arguments.</span></span>

<span data-ttu-id="dadf9-142">Чтобы запустить **НаЗапись** в Visual Basic для приложений (VBA) модуль, используйте метод **НаЗапись** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="dadf9-142">To run the **GoToRecord** action in a Visual Basic for Applications (VBA) module, use the **GoToRecord** method of the **DoCmd** object.</span></span>

