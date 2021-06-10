---
title: Макрокоманда CopyObject
TOCTitle: CopyObject macro action
ms:assetid: 746f61df-d5db-284a-0897-75820c2be11f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195876(v=office.15)
ms:contentKeyID: 48545661
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12836
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2d1fb13d04691b7bf5e0aafcc484cfc4f471e1e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295494"
---
# <a name="copyobject-macro-action"></a><span data-ttu-id="937ee-102">Макрокоманда CopyObject</span><span class="sxs-lookup"><span data-stu-id="937ee-102">CopyObject macro action</span></span>

<span data-ttu-id="937ee-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="937ee-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="937ee-104">Вы можете использовать **действие CopyObject** для копирования указанного объекта базы данных в другую базу данных доступа или в ту же базу данных или проект Access под новым именем.</span><span class="sxs-lookup"><span data-stu-id="937ee-104">You can use the **CopyObject** action to copy the specified database object to a different Access database or to the same database or Access project under a new name.</span></span> <span data-ttu-id="937ee-105">Например, можно скопировать или создать копию существующего объекта в другой базе данных или быстро создать аналогичный объект с несколькими изменениями.</span><span class="sxs-lookup"><span data-stu-id="937ee-105">For example, you can copy or back up an existing object in another database or quickly create a similar object with a few changes.</span></span>

> [!NOTE]
> <span data-ttu-id="937ee-106">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="937ee-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="937ee-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="937ee-107">Setting</span></span>

<span data-ttu-id="937ee-108">Действие **CopyObject** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="937ee-108">The **CopyObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="937ee-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="937ee-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="937ee-110">Описание</span><span class="sxs-lookup"><span data-stu-id="937ee-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="937ee-111"><strong>База данных назначения</strong></span><span class="sxs-lookup"><span data-stu-id="937ee-111"><strong>Destination Database</strong></span></span></p></td>
<td><p><span data-ttu-id="937ee-112">Допустимый путь и имя файла для базы данных назначения.</span><span class="sxs-lookup"><span data-stu-id="937ee-112">A valid path and file name for the destination database.</span></span> <span data-ttu-id="937ee-113">Введите путь и имя файла в поле <strong>База</strong> данных назначения в разделе <strong>Аргументы</strong> действий в области Macro Builder.</span><span class="sxs-lookup"><span data-stu-id="937ee-113">Enter the path and file name in the <strong>Destination Database</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="937ee-114">Если вы хотите выбрать текущую базу данных, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="937ee-114">Leave this argument blank if you want to select the current database.</span></span></p><p><span data-ttu-id="937ee-115"><strong>ПРИМЕЧАНИЕ.</strong>Этот аргумент доступен только в среде базы данных Access.</span><span class="sxs-lookup"><span data-stu-id="937ee-115"><strong>NOTE</strong>: This argument is only available in the Access database environment.</span></span> <span data-ttu-id="937ee-116">При использовании этого действия в среде проекта Access (.adp) аргумент "База данных назначения" должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="937ee-116">When using this action in an Access project environment (.adp), the Destination Database argument must be blank.</span></span></p>
<p><span data-ttu-id="937ee-117">Если выполнить макрос, содержащий действие <strong>CopyObject</strong> в базе данных библиотеки и оставить этот аргумент пустым, Microsoft Office Access 2007 скопирует объект в базу данных библиотеки.</span><span class="sxs-lookup"><span data-stu-id="937ee-117">If you run a macro containing the <strong>CopyObject</strong> action in a library database and leave this argument blank, Microsoft Office Access 2007 will copy the object into the library database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="937ee-118"><strong>Новое имя</strong></span><span class="sxs-lookup"><span data-stu-id="937ee-118"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="937ee-119">Новое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="937ee-119">A new name for the object.</span></span> <span data-ttu-id="937ee-120">При копировании в другую базу данных оставьте этот аргумент пустым, чтобы сохранить одно и то же имя.</span><span class="sxs-lookup"><span data-stu-id="937ee-120">When copying to a different database, leave this argument blank to keep the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="937ee-121"><strong>Тип объекта source</strong></span><span class="sxs-lookup"><span data-stu-id="937ee-121"><strong>Source Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="937ee-122">Тип объекта, который необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="937ee-122">The object type you want to copy.</span></span> <span data-ttu-id="937ee-123">Щелкните <strong>таблицу,</strong> <strong>запрос,</strong> <strong>форма,</strong> <strong>отчет,</strong> <strong>макрос,</strong> <strong>модуль,</strong>страница доступа к <strong>данным,</strong>представление <strong>сервера,</strong> <strong>схема,</strong> <strong>сохраненная</strong>процедура или <strong>функция</strong>.</span><span class="sxs-lookup"><span data-stu-id="937ee-123">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>.</span></span> <span data-ttu-id="937ee-124">Чтобы скопировать объект, выбранный в области навигации, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="937ee-124">To copy the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="937ee-125"><strong>Имя объекта source</strong></span><span class="sxs-lookup"><span data-stu-id="937ee-125"><strong>Source Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="937ee-126">Имя объекта, который будет скопирован.</span><span class="sxs-lookup"><span data-stu-id="937ee-126">The name of the object to be copied.</span></span> <span data-ttu-id="937ee-127">Поле <strong>Source Object Name</strong> отображает все объекты в базе данных типа, выбранного аргументом Типа <strong>объекта</strong> Source.</span><span class="sxs-lookup"><span data-stu-id="937ee-127">The <strong>Source Object Name</strong> box shows all objects in the database of the type selected by the <strong>Source Object Type</strong> argument.</span></span> <span data-ttu-id="937ee-128">В поле <strong>Source Object Name</strong> щелкните объект для копирования.</span><span class="sxs-lookup"><span data-stu-id="937ee-128">In the <strong>Source Object Name</strong> box, click the object to copy.</span></span> <span data-ttu-id="937ee-129">Если вы оставите аргумент <strong>Source Object Type</strong> пустым, также оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="937ee-129">If you leave the <strong>Source Object Type</strong> argument blank, leave this argument blank also.</span></span> <span data-ttu-id="937ee-130">Если вы запустите макрос, содержащий действие <strong>CopyObject</strong> в базе данных библиотеки, Access сначала ищет объект с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="937ee-130">If you run a macro containing the <strong>CopyObject</strong> action in a library database, Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="937ee-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="937ee-131">Remarks</span></span>

<span data-ttu-id="937ee-132">Для этого действия необходимо ввести значение для  одного или обоих аргументов **базы** данных назначения и нового имени.</span><span class="sxs-lookup"><span data-stu-id="937ee-132">You must enter a value for either one or both of the **Destination Database** and **New Name** arguments for this action.</span></span>

<span data-ttu-id="937ee-133">Если аргументы **типа исходных** объектов и имени исходных объектов будут пустыми, Access копирует объект, выбранный в области навигации. </span><span class="sxs-lookup"><span data-stu-id="937ee-133">If you leave the **Source Object Type** and **Source Object Name** arguments blank, Access copies the object selected in the Navigation Pane.</span></span> <span data-ttu-id="937ee-134">Чтобы выбрать объект в области навигации, можно использовать действие **SelectObject** с аргументом В области навигации, за набором **да.**</span><span class="sxs-lookup"><span data-stu-id="937ee-134">To select an object in the Navigation Pane, you can use the **SelectObject** action with the In Navigation Pane argument set to **Yes**.</span></span>

<span data-ttu-id="937ee-135">Действие **CopyObject** аналогично выполнению следующих действий вручную:</span><span class="sxs-lookup"><span data-stu-id="937ee-135">The **CopyObject** action is similar to performing the following steps manually:</span></span>

1. <span data-ttu-id="937ee-136">Выберите объект в области навигации.</span><span class="sxs-lookup"><span data-stu-id="937ee-136">Select an object in the Navigation Pane.</span></span>

2. <span data-ttu-id="937ee-137">На вкладке Главная в группе Буфер обмена щелкните Копировать.</span><span class="sxs-lookup"><span data-stu-id="937ee-137">On the Home tab, in the Clipboard group, click Copy.</span></span>

3. <span data-ttu-id="937ee-138">На той же вкладке щелкните **вклейку**. Диалоговое **окно Paste As** отображается таким образом, чтобы можно было дать объекту новое имя.</span><span class="sxs-lookup"><span data-stu-id="937ee-138">On the same tab, click **Paste**.The **Paste As** dialog box appears so that you can give the object a new name.</span></span> <span data-ttu-id="937ee-139">Действие **CopyObject** выполняет все эти действия автоматически.</span><span class="sxs-lookup"><span data-stu-id="937ee-139">The **CopyObject** action performs all of these steps automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="937ee-140">При копировании страниц доступа к данным действие **CopyObject** копирует только ссылку на связанный файл .htm, а не сам файл.</span><span class="sxs-lookup"><span data-stu-id="937ee-140">When copying data access pages, the **CopyObject** action copies only the link to the associated .htm file, not the file itself.</span></span>

<span data-ttu-id="937ee-141">Путь и имя файла базы данных назначения должны существовать до того, как макрос запускает **действие CopyObject.**</span><span class="sxs-lookup"><span data-stu-id="937ee-141">The path and file name of the destination database must exist before the macro runs the **CopyObject** action.</span></span> <span data-ttu-id="937ee-142">Если их не существует, Access отображает сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="937ee-142">If they don't exist, Access displays an error message.</span></span>

<span data-ttu-id="937ee-143">Чтобы выполнить **действие CopyObject** в Visual Basic для приложений (VBA), используйте метод **CopyObject** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="937ee-143">To run the **CopyObject** action in a Visual Basic for Applications (VBA) module, use the **CopyObject** method of the **DoCmd** object.</span></span>

<span data-ttu-id="937ee-144">Вы также можете вручную скопировать объект, выбранный в области навигации, или объект, открытый в настоящее время, щелкнув вкладку **Файл** и нажав кнопку **Сохранить Как**.</span><span class="sxs-lookup"><span data-stu-id="937ee-144">You can also manually copy an object selected in the Navigation Pane, or an object that is currently open, by clicking the **File** tab and then clicking **Save As**.</span></span> <span data-ttu-id="937ee-145">Эта команда будет делать копию объекта только в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="937ee-145">This command will make a copy of the object in the current database only.</span></span> <span data-ttu-id="937ee-146">В **диалоговом** окне Сохранить Как введите имя копии и выберите тип объекта, который необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="937ee-146">In the **Save As** dialog box, enter the name for the copy, and choose what type of object you want to save it as.</span></span> <span data-ttu-id="937ee-147">Если исходный объект уже сохранен и вы сохраните его в текущей базе данных с новым именем, оригинальная версия по-прежнему существует со старым именем.</span><span class="sxs-lookup"><span data-stu-id="937ee-147">If the original object has already been saved and you save it in the current database with a new name, the original version still exists with its old name.</span></span>

<span data-ttu-id="937ee-148">Вручную скопировать объект в другую базу данных Access:</span><span class="sxs-lookup"><span data-stu-id="937ee-148">To manually copy an object to a different Access database:</span></span>

1. <span data-ttu-id="937ee-149">На **вкладке Внешние данные** в группе **Экспорт** нажмите кнопку **Больше,** а затем нажмите **кнопку Access Database**.</span><span class="sxs-lookup"><span data-stu-id="937ee-149">On the **External Data** tab, in the **Export** group, click **More** and then click **Access Database**.</span></span>

2. <span data-ttu-id="937ee-150">В диалоговом окне Экспорт **—** Доступ к базе данных введите имя  файла базы данных назначения.-или-Щелкните Обзор, чтобы отобразить диалоговое окно Сохранить файл, найдите базу данных назначения и нажмите кнопку **Сохранить**. </span><span class="sxs-lookup"><span data-stu-id="937ee-150">In the **Export - Access Database** dialog box, enter the file name of the destination database.-or-Click **Browse** to display the **File Save** dialog box, locate the destination database, and then click **Save**.</span></span>

3. <span data-ttu-id="937ee-151">В **диалоговом окне Экспорт — Доступ** к базе данных нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="937ee-151">In the **Export - Access Database** dialog box, click **OK**.</span></span> <span data-ttu-id="937ee-152">Отображается **диалоговое** окно Экспорт.</span><span class="sxs-lookup"><span data-stu-id="937ee-152">The **Export** dialog box appears.</span></span>

4. <span data-ttu-id="937ee-153">В **диалоговом** окне Экспорт введите имя объекта в базе данных назначения.</span><span class="sxs-lookup"><span data-stu-id="937ee-153">In the **Export** dialog box, enter a name for the object in the destination database.</span></span> <span data-ttu-id="937ee-154">Выберите все применимые параметры, такие как **экспортное определение и данные** или **определение только для** таблиц.</span><span class="sxs-lookup"><span data-stu-id="937ee-154">Choose any applicable options, such as **Export Definition and Data** or **Definition Only** for tables.</span></span> <span data-ttu-id="937ee-155">По завершении нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="937ee-155">When you are finished, click **OK**.</span></span>

