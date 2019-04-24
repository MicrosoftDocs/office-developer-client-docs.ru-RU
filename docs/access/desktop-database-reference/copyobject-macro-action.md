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
# <a name="copyobject-macro-action"></a><span data-ttu-id="0e892-102">Макрокоманда CopyObject</span><span class="sxs-lookup"><span data-stu-id="0e892-102">CopyObject macro action</span></span>

<span data-ttu-id="0e892-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e892-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e892-104">Макрокоманда **КопироватьОбъект** позволяет скопировать указанный объект базы данных в другую базу данных Access или в ту же базу данных или проект Access под новым именем.</span><span class="sxs-lookup"><span data-stu-id="0e892-104">You can use the **CopyObject** action to copy the specified database object to a different Access database or to the same database or Access project under a new name.</span></span> <span data-ttu-id="0e892-105">Например, можно скопировать или создать резервную копию существующего объекта в другой базе данных или быстро создать похожий объект с несколькими изменениями.</span><span class="sxs-lookup"><span data-stu-id="0e892-105">For example, you can copy or back up an existing object in another database or quickly create a similar object with a few changes.</span></span>

> [!NOTE]
> <span data-ttu-id="0e892-106">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="0e892-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="0e892-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e892-107">Setting</span></span>

<span data-ttu-id="0e892-108">Макрокоманда **КопироватьОбъект** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="0e892-108">The **CopyObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e892-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="0e892-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="0e892-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0e892-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e892-111"><strong>Целевая база данных</strong></span><span class="sxs-lookup"><span data-stu-id="0e892-111"><strong>Destination Database</strong></span></span></p></td>
<td><p><span data-ttu-id="0e892-112">Допустимый путь и имя файла для целевой базы данных.</span><span class="sxs-lookup"><span data-stu-id="0e892-112">A valid path and file name for the destination database.</span></span> <span data-ttu-id="0e892-113">Введите путь и имя файла в поле <strong>конечНая база данных</strong> в разделе <strong>аргументы макрокоманды</strong> в области построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="0e892-113">Enter the path and file name in the <strong>Destination Database</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="0e892-114">Если вы хотите выбрать текущую базу данных, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="0e892-114">Leave this argument blank if you want to select the current database.</span></span></p><p><span data-ttu-id="0e892-115"><strong>Примечание</strong>: этот аргумент доступен только в среде базы данных Access.</span><span class="sxs-lookup"><span data-stu-id="0e892-115"><strong>NOTE</strong>: This argument is only available in the Access database environment.</span></span> <span data-ttu-id="0e892-116">При использовании этого действия в среде проекта Access (ADP) аргумент базы данных-получателя должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="0e892-116">When using this action in an Access project environment (.adp), the Destination Database argument must be blank.</span></span></p>
<p><span data-ttu-id="0e892-117">При запуске макроса, содержащего макрокоманду <strong>КопироватьОбъект</strong> , в библиотечной базе данных, если оставить этот аргумент пустым, Microsoft Office Access 2007 скопирует объект в библиотечную базу данных.</span><span class="sxs-lookup"><span data-stu-id="0e892-117">If you run a macro containing the <strong>CopyObject</strong> action in a library database and leave this argument blank, Microsoft Office Access 2007 will copy the object into the library database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e892-118"><strong>Новое имя</strong></span><span class="sxs-lookup"><span data-stu-id="0e892-118"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="0e892-119">Новое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="0e892-119">A new name for the object.</span></span> <span data-ttu-id="0e892-120">При копировании в другую базу данных оставьте этот аргумент пустым, чтобы сохранить то же имя.</span><span class="sxs-lookup"><span data-stu-id="0e892-120">When copying to a different database, leave this argument blank to keep the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e892-121"><strong>Тип исходного объекта</strong></span><span class="sxs-lookup"><span data-stu-id="0e892-121"><strong>Source Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="0e892-122">Тип объекта, который необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="0e892-122">The object type you want to copy.</span></span> <span data-ttu-id="0e892-123">Щелкните <strong>Таблица</strong>, <strong>запрос</strong>, <strong>форма</strong>, <strong>отчет</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>Страница доступа к данным</strong>, <strong>представление сервера</strong>, <strong>схема</strong>, <strong>хранимая процедура</strong>или <strong>функция</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e892-123">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>.</span></span> <span data-ttu-id="0e892-124">Чтобы скопировать объект, выбранный в области навигации, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="0e892-124">To copy the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e892-125"><strong>Имя исходного объекта</strong></span><span class="sxs-lookup"><span data-stu-id="0e892-125"><strong>Source Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="0e892-126">Имя копируемого объекта.</span><span class="sxs-lookup"><span data-stu-id="0e892-126">The name of the object to be copied.</span></span> <span data-ttu-id="0e892-127">В поле <strong>имя исходного объекта</strong> отображаются все объекты базы данных с типом, выбранным аргументом <strong>Тип исходного объекта</strong> .</span><span class="sxs-lookup"><span data-stu-id="0e892-127">The <strong>Source Object Name</strong> box shows all objects in the database of the type selected by the <strong>Source Object Type</strong> argument.</span></span> <span data-ttu-id="0e892-128">В поле <strong>имя исходного объекта</strong> щелкните объект, который требуется скопировать.</span><span class="sxs-lookup"><span data-stu-id="0e892-128">In the <strong>Source Object Name</strong> box, click the object to copy.</span></span> <span data-ttu-id="0e892-129">Если оставить значение аргумента <strong>Тип исходного объекта</strong> пустым, то этот аргумент также следует оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="0e892-129">If you leave the <strong>Source Object Type</strong> argument blank, leave this argument blank also.</span></span> <span data-ttu-id="0e892-130">При запуске макроса, содержащего макрокоманду <strong>КопироватьОбъект</strong> , в библиотечной базе данных Access сначала выполняет поиск объекта с этим именем в библиотечной базе данных, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="0e892-130">If you run a macro containing the <strong>CopyObject</strong> action in a library database, Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0e892-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="0e892-131">Remarks</span></span>

<span data-ttu-id="0e892-132">Необходимо ввести значение для одной или обеих **конечНых баз данных** и аргументов **нового имени** для этого действия.</span><span class="sxs-lookup"><span data-stu-id="0e892-132">You must enter a value for either one or both of the **Destination Database** and **New Name** arguments for this action.</span></span>

<span data-ttu-id="0e892-133">Если вы оставляете аргументы **Тип исходного объекта** и **имя исходного объекта** пустыми, Access копирует объект, выбранный в области навигации.</span><span class="sxs-lookup"><span data-stu-id="0e892-133">If you leave the **Source Object Type** and **Source Object Name** arguments blank, Access copies the object selected in the Navigation Pane.</span></span> <span data-ttu-id="0e892-134">Чтобы выбрать объект в области навигации, можно использовать макрокоманду **"ВыделитьОбъект"**( **ВыделитьОбъект** ) с параметром в разделе в области навигации со значением Да.</span><span class="sxs-lookup"><span data-stu-id="0e892-134">To select an object in the Navigation Pane, you can use the **SelectObject** action with the In Navigation Pane argument set to **Yes**.</span></span>

<span data-ttu-id="0e892-135">Действие **КопироватьОбъект** аналогично выполнению следующих действий вручную:</span><span class="sxs-lookup"><span data-stu-id="0e892-135">The **CopyObject** action is similar to performing the following steps manually:</span></span>

1. <span data-ttu-id="0e892-136">Выберите объект в области навигации.</span><span class="sxs-lookup"><span data-stu-id="0e892-136">Select an object in the Navigation Pane.</span></span>

2. <span data-ttu-id="0e892-137">На вкладке Главная в группе Буфер обмена щелкните Копировать.</span><span class="sxs-lookup"><span data-stu-id="0e892-137">On the Home tab, in the Clipboard group, click Copy.</span></span>

3. <span data-ttu-id="0e892-138">На той же вкладке нажмите кнопку **Вставить**. Откроется диалоговое окно **Вставка в виде** , в котором можно присвоить объекту новое имя.</span><span class="sxs-lookup"><span data-stu-id="0e892-138">On the same tab, click **Paste**.The **Paste As** dialog box appears so that you can give the object a new name.</span></span> <span data-ttu-id="0e892-139">Действие **КопироватьОбъект** выполняет все эти действия автоматически.</span><span class="sxs-lookup"><span data-stu-id="0e892-139">The **CopyObject** action performs all of these steps automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="0e892-140">При копировании страниц доступа к данным команда **КопироватьОбъект** копирует только ссылку на соответствующий htm файл, а не сам файл.</span><span class="sxs-lookup"><span data-stu-id="0e892-140">When copying data access pages, the **CopyObject** action copies only the link to the associated .htm file, not the file itself.</span></span>

<span data-ttu-id="0e892-141">Путь и имя файла целевой базы данных должны существовать перед выполнением макрокоманды **КопироватьОбъект** .</span><span class="sxs-lookup"><span data-stu-id="0e892-141">The path and file name of the destination database must exist before the macro runs the **CopyObject** action.</span></span> <span data-ttu-id="0e892-142">Если они не существуют, Access отображает сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0e892-142">If they don't exist, Access displays an error message.</span></span>

<span data-ttu-id="0e892-143">Чтобы выполнить макрокоманду **КопироватьОбъект** в модуле Visual Basic для приложений (VBA), используйте метод **КопироватьОбъект** объекта DoCmd. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="0e892-143">To run the **CopyObject** action in a Visual Basic for Applications (VBA) module, use the **CopyObject** method of the **DoCmd** object.</span></span>

<span data-ttu-id="0e892-144">Вы также можете вручную скопировать объект, выделенный в области навигации, или объект, который в данный момент открыт, щелкнув вкладку **файл** и нажав кнопку **Сохранить как**.</span><span class="sxs-lookup"><span data-stu-id="0e892-144">You can also manually copy an object selected in the Navigation Pane, or an object that is currently open, by clicking the **File** tab and then clicking **Save As**.</span></span> <span data-ttu-id="0e892-145">Эта команда создаст копию объекта только в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="0e892-145">This command will make a copy of the object in the current database only.</span></span> <span data-ttu-id="0e892-146">В диалоговом окне **Сохранить как** введите имя копии и выберите тип объекта, который необходимо сохранить как.</span><span class="sxs-lookup"><span data-stu-id="0e892-146">In the **Save As** dialog box, enter the name for the copy, and choose what type of object you want to save it as.</span></span> <span data-ttu-id="0e892-147">Если исходный объект уже был сохранен и сохранен в текущей базе данных с новым именем, исходная версия по-прежнему будет существовать со старым именем.</span><span class="sxs-lookup"><span data-stu-id="0e892-147">If the original object has already been saved and you save it in the current database with a new name, the original version still exists with its old name.</span></span>

<span data-ttu-id="0e892-148">Чтобы вручную скопировать объект в другую базу данных Access, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="0e892-148">To manually copy an object to a different Access database:</span></span>

1. <span data-ttu-id="0e892-149">На вкладке **Внешние данные** в группе **Экспорт** нажмите кнопку **Дополнительно** , а затем выберите **база данных Access**.</span><span class="sxs-lookup"><span data-stu-id="0e892-149">On the **External Data** tab, in the **Export** group, click **More** and then click **Access Database**.</span></span>

2. <span data-ttu-id="0e892-150">В диалоговом окне **Экспорт и доступ к базе данных** введите имя файла целевой базы данных. — или нажмите кнопку **Обзор** , чтобы открыть диалоговое окно **Сохранение файла** , Найдите целевую базу данных, а затем нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0e892-150">In the **Export - Access Database** dialog box, enter the file name of the destination database.-or-Click **Browse** to display the **File Save** dialog box, locate the destination database, and then click **Save**.</span></span>

3. <span data-ttu-id="0e892-151">В диалоговом окне " **Экспорт и доступ к базе данных** " нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0e892-151">In the **Export - Access Database** dialog box, click **OK**.</span></span> <span data-ttu-id="0e892-152">Откроется диалоговое окно **Экспорт** .</span><span class="sxs-lookup"><span data-stu-id="0e892-152">The **Export** dialog box appears.</span></span>

4. <span data-ttu-id="0e892-153">В диалоговом окне **Экспорт** введите имя объекта в целевую базу данных.</span><span class="sxs-lookup"><span data-stu-id="0e892-153">In the **Export** dialog box, enter a name for the object in the destination database.</span></span> <span data-ttu-id="0e892-154">Выберите необходимые параметры, такие как **Определение экспорта и данные** или **Определение только** для таблиц.</span><span class="sxs-lookup"><span data-stu-id="0e892-154">Choose any applicable options, such as **Export Definition and Data** or **Definition Only** for tables.</span></span> <span data-ttu-id="0e892-155">По завершении нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0e892-155">When you are finished, click **OK**.</span></span>

