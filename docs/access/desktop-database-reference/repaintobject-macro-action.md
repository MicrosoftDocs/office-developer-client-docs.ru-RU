---
title: Макрокоманда RepaintObject
TOCTitle: RepaintObject macro action
ms:assetid: e8fa7d0b-578c-5071-2bd5-b772b48637a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836055(v=office.15)
ms:contentKeyID: 48548431
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm195788
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2ef6c5f38064ae3253cd7e0e58732f63294ceb3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722832"
---
# <a name="repaintobject-macro-action"></a><span data-ttu-id="ce7b5-102">Макрокоманда RepaintObject</span><span class="sxs-lookup"><span data-stu-id="ce7b5-102">RepaintObject macro action</span></span>

<span data-ttu-id="ce7b5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce7b5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ce7b5-104">**ОбновитьОбъект** можно использовать для выполнения все ожидающие обновления экрана для указанного объекта или для активного объекта базы данных, если он не задан.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-104">You can use the **RepaintObject** action to complete any pending screen updates for a specified database object or for the active database object, if none is specified.</span></span> <span data-ttu-id="ce7b5-105">Такие обновления включают все ожидающие пересчета для элементов управления объекта.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-105">Such updates include any pending recalculations for the object's controls.</span></span>

## <a name="setting"></a><span data-ttu-id="ce7b5-106">Setting</span><span class="sxs-lookup"><span data-stu-id="ce7b5-106">Setting</span></span>

<span data-ttu-id="ce7b5-107">**ОбновитьОбъект** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-107">The **RepaintObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ce7b5-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="ce7b5-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ce7b5-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ce7b5-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce7b5-110"><strong>Тип объекта</strong></span><span class="sxs-lookup"><span data-stu-id="ce7b5-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="ce7b5-111">Тип объекта, который следует обновить.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-111">The type of object to repaint.</span></span> <span data-ttu-id="ce7b5-112">Выберите <strong>таблицы</strong>, <strong>запроса</strong>, <strong>формы</strong>, <strong>отчета</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>страницы доступа к данным</strong>, <strong>представление</strong>, <strong>Схема</strong>, <strong>хранимая процедура</strong>или <strong>функции</strong> в тип объекта <strong> </strong>флажок в разделе <strong>Действие аргументы</strong> области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-112">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="ce7b5-113">Оставьте данный аргумент пустым, чтобы выбрать активный объект.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-113">Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce7b5-114"><strong>Имя объекта</strong></span><span class="sxs-lookup"><span data-stu-id="ce7b5-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ce7b5-115">Имя обновляемого объекта.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-115">The name of the object to repaint.</span></span> <span data-ttu-id="ce7b5-116">В поле <strong>Имя объекта</strong> содержит все объекты базы данных, указанному в аргументе <strong>Тип объекта</strong> типа.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-116">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="ce7b5-117">Если <strong>Тип объекта</strong> аргумента оставлено пустым, оставьте аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-117">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ce7b5-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="ce7b5-118">Remarks</span></span>

<span data-ttu-id="ce7b5-119">Microsoft Access будет ожидать завершения ожидающие обновления экрана до завершения другие ожидающие задачи.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-119">Microsoft Access waits to complete pending screen updates until it finishes other pending tasks.</span></span> <span data-ttu-id="ce7b5-120">С помощью этого действия можно принудительно немедленное обновление элементов управления в указанном объекте.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-120">With this action, you can force immediate repainting of the controls in the specified object.</span></span> <span data-ttu-id="ce7b5-121">Это действие можно использовать:</span><span class="sxs-lookup"><span data-stu-id="ce7b5-121">You can use this action:</span></span>

- <span data-ttu-id="ce7b5-122">При использовании **ЗадатьЗначение** изменение значений нескольких элементов управления.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-122">When you use the **SetValue** action to change values in a number of controls.</span></span> <span data-ttu-id="ce7b5-123">Не обязательно будут отражены изменения немедленно, особенно в том случае, если другие элементы управления (например, вычисляемые элементы управления) зависят от значений измененных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-123">Access might not show the changes immediately, especially if other controls (such as calculated controls) depend on values in the changed controls.</span></span>

- <span data-ttu-id="ce7b5-124">При необходимости убедитесь в том, что форма отображается отображает данные в всех элементов управления.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-124">When you want to make sure that the form you are viewing displays data in all of its controls.</span></span> <span data-ttu-id="ce7b5-125">Например элементы управления, содержащий объекты OLE не отображать свои данные сразу же после открытия формы.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-125">For example, controls containing OLE objects don't display their data immediately after you open a form.</span></span>

> [!NOTE]
> - <span data-ttu-id="ce7b5-126">Это действие не вызывает обновление базы данных, поэтому она не показывает новые, измененные или удаления записи из объекта базовой таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-126">This action doesn't cause a requery of the database, so it doesn't show new and changed records or remove deleted records from the object's underlying table or query.</span></span> <span data-ttu-id="ce7b5-127">Действие **повторный запрос** используется при обновлении объекта или один из его элементов.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-127">Use the **Requery** action to requery the source of the object or one of its controls.</span></span> <span data-ttu-id="ce7b5-128">Используйте **ПоказатьВсеЗаписи** для отображения последних записей и удалить все примененные фильтры.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-128">Use the **ShowAllRecords** action to display the most recent records and remove any applied filters.</span></span>
> - <span data-ttu-id="ce7b5-129">**ОбновитьОбъект** не имеет тот же эффект, как **Обновить** в группе **записей** на вкладке **Главная** , где отображаются все изменения, что вы или другие пользователи были внесены в текущей отображаемой страницы записи в формах и технические описания.</span><span class="sxs-lookup"><span data-stu-id="ce7b5-129">The **RepaintObject** action doesn't have the same effect as clicking **Refresh** in the **Records** group on the **Home** tab, which shows any changes you or other users have made to the currently displayed records in forms and datasheets.</span></span>

<span data-ttu-id="ce7b5-130">Чтобы запустить **ОбновитьОбъект** в Visual Basic для приложений (VBA) модуль, используйте метод **ОбновитьОбъект** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="ce7b5-130">To run the **RepaintObject** action in a Visual Basic for Applications (VBA) module, use the **RepaintObject** method of the **DoCmd** object.</span></span>

