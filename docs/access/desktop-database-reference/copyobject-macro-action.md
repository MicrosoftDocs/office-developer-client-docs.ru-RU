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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715888"
---
# <a name="copyobject-macro-action"></a><span data-ttu-id="d7234-102">Макрокоманда CopyObject</span><span class="sxs-lookup"><span data-stu-id="d7234-102">CopyObject macro action</span></span>

<span data-ttu-id="d7234-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7234-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7234-104">**КопироватьОбъект** можно использовать для копирования указанного объекта в другую базу данных Access или одной базы данных или проекта Access под новым именем.</span><span class="sxs-lookup"><span data-stu-id="d7234-104">You can use the **CopyObject** action to copy the specified database object to a different Access database or to the same database or Access project under a new name.</span></span> <span data-ttu-id="d7234-105">Например можно скопировать или резервное копирование существующего объекта в другую базу данных или быстро создать объект аналогичные с несколько изменений.</span><span class="sxs-lookup"><span data-stu-id="d7234-105">For example, you can copy or back up an existing object in another database or quickly create a similar object with a few changes.</span></span>

> [!NOTE]
> <span data-ttu-id="d7234-106">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="d7234-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="d7234-107">Setting</span><span class="sxs-lookup"><span data-stu-id="d7234-107">Setting</span></span>

<span data-ttu-id="d7234-108">**КопироватьОбъект** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="d7234-108">The **CopyObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d7234-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="d7234-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d7234-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d7234-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7234-111"><strong>Конечная база данных</strong></span><span class="sxs-lookup"><span data-stu-id="d7234-111"><strong>Destination Database</strong></span></span></p></td>
<td><p><span data-ttu-id="d7234-112">Допустимый путь и имя конечной базы данных.</span><span class="sxs-lookup"><span data-stu-id="d7234-112">A valid path and file name for the destination database.</span></span> <span data-ttu-id="d7234-113">Введите путь и имя файла в поле <strong>Конечной базы данных</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="d7234-113">Enter the path and file name in the <strong>Destination Database</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="d7234-114">Этот аргумент оставьте поле пустым, чтобы выбрать текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="d7234-114">Leave this argument blank if you want to select the current database.</span></span></p><p><span data-ttu-id="d7234-115"><strong>Примечание</strong>: этот аргумент доступен только в среде базы данных Access.</span><span class="sxs-lookup"><span data-stu-id="d7234-115"><strong>NOTE</strong>: This argument is only available in the Access database environment.</span></span> <span data-ttu-id="d7234-116">При использовании этого действия в среде проекта Access (файлы с расширением ADP), аргумент конечной базы данных должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="d7234-116">When using this action in an Access project environment (.adp), the Destination Database argument must be blank.</span></span></p>
<p><span data-ttu-id="d7234-117">Если макрос, содержащий <strong>КопироватьОбъект в базе данных библиотеки</strong> и оставить данный аргумент пустым, Microsoft Office Access 2007 копирует объект в базе данных библиотеки.</span><span class="sxs-lookup"><span data-stu-id="d7234-117">If you run a macro containing the <strong>CopyObject</strong> action in a library database and leave this argument blank, Microsoft Office Access 2007 will copy the object into the library database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7234-118"><strong>Новое имя</strong></span><span class="sxs-lookup"><span data-stu-id="d7234-118"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d7234-119">Новое имя для объекта.</span><span class="sxs-lookup"><span data-stu-id="d7234-119">A new name for the object.</span></span> <span data-ttu-id="d7234-120">При копировании в другую базу данных, этот аргумент оставьте поле пустым таким же именем.</span><span class="sxs-lookup"><span data-stu-id="d7234-120">When copying to a different database, leave this argument blank to keep the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7234-121"><strong>Тип объекта</strong></span><span class="sxs-lookup"><span data-stu-id="d7234-121"><strong>Source Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="d7234-122">Тип объекта, который необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="d7234-122">The object type you want to copy.</span></span> <span data-ttu-id="d7234-123">Выберите <strong>таблицы</strong>, <strong>запроса</strong>, <strong>формы</strong>, <strong>отчета</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>страницы доступа к данным</strong>, <strong>представление</strong>, <strong>Схема</strong>, <strong>хранимая процедура</strong>или <strong>функция</strong>.</span><span class="sxs-lookup"><span data-stu-id="d7234-123">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>.</span></span> <span data-ttu-id="d7234-124">Чтобы скопировать объект, выделенный в области навигации, оставьте данный аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="d7234-124">To copy the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7234-125"><strong>Имя исходного объекта</strong></span><span class="sxs-lookup"><span data-stu-id="d7234-125"><strong>Source Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d7234-126">Имя объекта для копирования.</span><span class="sxs-lookup"><span data-stu-id="d7234-126">The name of the object to be copied.</span></span> <span data-ttu-id="d7234-127">В поле <strong>Имя исходного объекта</strong> содержит все объекты базы данных, указанному в аргументе <strong>Тип объекта</strong> типа.</span><span class="sxs-lookup"><span data-stu-id="d7234-127">The <strong>Source Object Name</strong> box shows all objects in the database of the type selected by the <strong>Source Object Type</strong> argument.</span></span> <span data-ttu-id="d7234-128">В поле <strong>Имя объекта</strong> выберите объект для копирования.</span><span class="sxs-lookup"><span data-stu-id="d7234-128">In the <strong>Source Object Name</strong> box, click the object to copy.</span></span> <span data-ttu-id="d7234-129">Если <strong>Тип объекта</strong> аргумента оставлено пустым, оставьте аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="d7234-129">If you leave the <strong>Source Object Type</strong> argument blank, leave this argument blank also.</span></span> <span data-ttu-id="d7234-130">Если макрос, содержащий <strong>КопироватьОбъект в базе данных библиотеки</strong> , сначала поиск объекта с указанным именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="d7234-130">If you run a macro containing the <strong>CopyObject</strong> action in a library database, Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d7234-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="d7234-131">Remarks</span></span>

<span data-ttu-id="d7234-132">Необходимо ввести значение для одного или обоих аргументов **Конечной базы данных** и **Новое имя** для этого действия.</span><span class="sxs-lookup"><span data-stu-id="d7234-132">You must enter a value for either one or both of the **Destination Database** and **New Name** arguments for this action.</span></span>

<span data-ttu-id="d7234-133">Если оставить **Тип объекта** и **Имя исходного объекта** аргументов, Access копирует объекта, выбранного в области навигации.</span><span class="sxs-lookup"><span data-stu-id="d7234-133">If you leave the **Source Object Type** and **Source Object Name** arguments blank, Access copies the object selected in the Navigation Pane.</span></span> <span data-ttu-id="d7234-134">Для выбора объекта в области навигации, можно использовать **ВыделитьОбъект** с аргументом в области переходов, значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="d7234-134">To select an object in the Navigation Pane, you can use the **SelectObject** action with the In Navigation Pane argument set to **Yes**.</span></span>

<span data-ttu-id="d7234-135">**КопироватьОбъект** будет вручную для выполнения следующих действий:</span><span class="sxs-lookup"><span data-stu-id="d7234-135">The **CopyObject** action is similar to performing the following steps manually:</span></span>

1. <span data-ttu-id="d7234-136">Выберите объект в области навигации.</span><span class="sxs-lookup"><span data-stu-id="d7234-136">Select an object in the Navigation Pane.</span></span>

2. <span data-ttu-id="d7234-137">
    На вкладке Главная в группе Буфер обмена щелкните Копировать.
  </span><span class="sxs-lookup"><span data-stu-id="d7234-137">On the Home tab, in the Clipboard group, click Copy.</span></span>

3. <span data-ttu-id="d7234-138">На этой же вкладке нажмите кнопку **Вставить**. Откроется диалоговое окно **Вставка** , чтобы назначить объект новое имя.</span><span class="sxs-lookup"><span data-stu-id="d7234-138">On the same tab, click **Paste**.The **Paste As** dialog box appears so that you can give the object a new name.</span></span> <span data-ttu-id="d7234-139">**КопироватьОбъект** автоматически выполняет все эти действия.</span><span class="sxs-lookup"><span data-stu-id="d7234-139">The **CopyObject** action performs all of these steps automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="d7234-140">При копировании страницы доступа к данным, **КопироватьОбъект** копирует только связи со связанными .htm файлами, не файл.</span><span class="sxs-lookup"><span data-stu-id="d7234-140">When copying data access pages, the **CopyObject** action copies only the link to the associated .htm file, not the file itself.</span></span>

<span data-ttu-id="d7234-141">Путь и имя конечной базы данных должен существовать до выполнения макроса **КопироватьОбъект** .</span><span class="sxs-lookup"><span data-stu-id="d7234-141">The path and file name of the destination database must exist before the macro runs the **CopyObject** action.</span></span> <span data-ttu-id="d7234-142">Если они не существуют, Access отображает сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d7234-142">If they don't exist, Access displays an error message.</span></span>

<span data-ttu-id="d7234-143">Чтобы запустить **КопироватьОбъект** в Visual Basic для приложений (VBA) модуль, используйте метод **КопироватьОбъект** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="d7234-143">To run the **CopyObject** action in a Visual Basic for Applications (VBA) module, use the **CopyObject** method of the **DoCmd** object.</span></span>

<span data-ttu-id="d7234-144">Можно также вручную скопировать объекта, выбранного в области навигации, или откройте объект, который в данный момент, нажав кнопку на вкладку **файл** и нажмите кнопку **Сохранить как**.</span><span class="sxs-lookup"><span data-stu-id="d7234-144">You can also manually copy an object selected in the Navigation Pane, or an object that is currently open, by clicking the **File** tab and then clicking **Save As**.</span></span> <span data-ttu-id="d7234-145">Эта команда будет создать копию объекта только текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="d7234-145">This command will make a copy of the object in the current database only.</span></span> <span data-ttu-id="d7234-146">В диалоговом окне **Сохранить как** введите имя для копии и выберите тип объекта, вы хотите сохранить как.</span><span class="sxs-lookup"><span data-stu-id="d7234-146">In the **Save As** dialog box, enter the name for the copy, and choose what type of object you want to save it as.</span></span> <span data-ttu-id="d7234-147">Если исходный объект уже был сохранен и сохраните его в текущей базе данных с новым именем, с его старое имя по-прежнему существует исходной версии.</span><span class="sxs-lookup"><span data-stu-id="d7234-147">If the original object has already been saved and you save it in the current database with a new name, the original version still exists with its old name.</span></span>

<span data-ttu-id="d7234-148">Чтобы вручную скопировать объект в другую базу данных Access:</span><span class="sxs-lookup"><span data-stu-id="d7234-148">To manually copy an object to a different Access database:</span></span>

1. <span data-ttu-id="d7234-149">На вкладке **Внешние данные** в группе **экспорта** нажмите кнопку **Дополнительно** и нажмите кнопку **Базы данных Access**.</span><span class="sxs-lookup"><span data-stu-id="d7234-149">On the **External Data** tab, in the **Export** group, click **More** and then click **Access Database**.</span></span>

2. <span data-ttu-id="d7234-150">В диалоговом окне **Экспорт - базы данных Access** , введите имя файла из целевой базы данных.- или -нажмите кнопку **Обзор** для отображения диалогового окна **Сохранение файла** , найдите в целевую базу данных и нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d7234-150">In the **Export - Access Database** dialog box, enter the file name of the destination database.-or-Click **Browse** to display the **File Save** dialog box, locate the destination database, and then click **Save**.</span></span>

3. <span data-ttu-id="d7234-151">В диалоговом окне **Экспорт - базы данных Access** нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="d7234-151">In the **Export - Access Database** dialog box, click **OK**.</span></span> <span data-ttu-id="d7234-152">Откроется диалоговое окно **Экспорт** .</span><span class="sxs-lookup"><span data-stu-id="d7234-152">The **Export** dialog box appears.</span></span>

4. <span data-ttu-id="d7234-153">В диалоговом окне **Экспорт** введите имя для объекта в целевой базы данных.</span><span class="sxs-lookup"><span data-stu-id="d7234-153">In the **Export** dialog box, enter a name for the object in the destination database.</span></span> <span data-ttu-id="d7234-154">Выберите любое применение параметров, таких как **Экспорт определения и данных** или **Определение только** для таблиц.</span><span class="sxs-lookup"><span data-stu-id="d7234-154">Choose any applicable options, such as **Export Definition and Data** or **Definition Only** for tables.</span></span> <span data-ttu-id="d7234-155">Завершив настройку, нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="d7234-155">When you are finished, click **OK**.</span></span>

