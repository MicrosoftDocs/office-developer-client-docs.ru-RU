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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306687"
---
# <a name="repaintobject-macro-action"></a><span data-ttu-id="3a66a-102">Макрокоманда RepaintObject</span><span class="sxs-lookup"><span data-stu-id="3a66a-102">RepaintObject macro action</span></span>

<span data-ttu-id="3a66a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a66a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a66a-104">Вы можете использовать **действие RepaintObject** для завершения любых ожидающих обновлений экрана для указанного объекта базы данных или для объекта активной базы данных, если их нет.</span><span class="sxs-lookup"><span data-stu-id="3a66a-104">You can use the **RepaintObject** action to complete any pending screen updates for a specified database object or for the active database object, if none is specified.</span></span> <span data-ttu-id="3a66a-105">Такие обновления включают любые ожидающих пересчетов для элементов управления объектом.</span><span class="sxs-lookup"><span data-stu-id="3a66a-105">Such updates include any pending recalculations for the object's controls.</span></span>

## <a name="setting"></a><span data-ttu-id="3a66a-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="3a66a-106">Setting</span></span>

<span data-ttu-id="3a66a-107">Действие **RepaintObject** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="3a66a-107">The **RepaintObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a66a-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="3a66a-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3a66a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3a66a-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a66a-110"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="3a66a-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="3a66a-111">Тип объекта, который необходимо перекрасить.</span><span class="sxs-lookup"><span data-stu-id="3a66a-111">The type of object to repaint.</span></span> <span data-ttu-id="3a66a-112"><strong>Щелкните</strong> <strong>таблицу,</strong> <strong>запрос,</strong>форма, отчет, макрос, модуль, <strong></strong> <strong></strong>страница доступа <strong></strong> к данным, представление сервера, схема, сохраненная процедура или функция в поле Тип объекта в разделе Аргументы действий области Macro Builder. <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong></span><span class="sxs-lookup"><span data-stu-id="3a66a-112">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="3a66a-113">Оставьте этот аргумент пустым, чтобы выбрать активный объект.</span><span class="sxs-lookup"><span data-stu-id="3a66a-113">Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a66a-114"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="3a66a-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="3a66a-115">Имя объекта для переклинации.</span><span class="sxs-lookup"><span data-stu-id="3a66a-115">The name of the object to repaint.</span></span> <span data-ttu-id="3a66a-116">Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a66a-116">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="3a66a-117">Если оставить аргумент <strong>Object Type</strong> пустым, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="3a66a-117">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3a66a-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="3a66a-118">Remarks</span></span>

<span data-ttu-id="3a66a-119">Microsoft Access ожидает завершения ожидающих обновлений экрана, пока не завершит выполнение других ожидающих задач.</span><span class="sxs-lookup"><span data-stu-id="3a66a-119">Microsoft Access waits to complete pending screen updates until it finishes other pending tasks.</span></span> <span data-ttu-id="3a66a-120">С помощью этого действия можно принудить к немедленному перекрасу элементов управления в указанном объекте.</span><span class="sxs-lookup"><span data-stu-id="3a66a-120">With this action, you can force immediate repainting of the controls in the specified object.</span></span> <span data-ttu-id="3a66a-121">Вы можете использовать это действие:</span><span class="sxs-lookup"><span data-stu-id="3a66a-121">You can use this action:</span></span>

- <span data-ttu-id="3a66a-122">При использовании **действия SetValue** для изменения значений в ряде элементов управления.</span><span class="sxs-lookup"><span data-stu-id="3a66a-122">When you use the **SetValue** action to change values in a number of controls.</span></span> <span data-ttu-id="3a66a-123">Доступ может не показывать изменения сразу, особенно если другие элементы управления (например, рассчитанные элементы управления) зависят от значений в измененных средствах управления.</span><span class="sxs-lookup"><span data-stu-id="3a66a-123">Access might not show the changes immediately, especially if other controls (such as calculated controls) depend on values in the changed controls.</span></span>

- <span data-ttu-id="3a66a-124">Если необходимо убедиться, что просматриваемая форма отображает данные во всех средствах управления.</span><span class="sxs-lookup"><span data-stu-id="3a66a-124">When you want to make sure that the form you are viewing displays data in all of its controls.</span></span> <span data-ttu-id="3a66a-125">Например, элементы управления, содержащие объекты OLE, не отображают их данные сразу после открытия формы.</span><span class="sxs-lookup"><span data-stu-id="3a66a-125">For example, controls containing OLE objects don't display their data immediately after you open a form.</span></span>

> [!NOTE]
> - <span data-ttu-id="3a66a-126">Это действие не вызывает повторного выполнения базы данных, поэтому она не показывает новые и не изменяла записи или не удаляет удаленные записи из основной таблицы или запроса объекта.</span><span class="sxs-lookup"><span data-stu-id="3a66a-126">This action doesn't cause a requery of the database, so it doesn't show new and changed records or remove deleted records from the object's underlying table or query.</span></span> <span data-ttu-id="3a66a-127">Используйте **действие Requery,** чтобы переокупить источник объекта или один из его элементов управления.</span><span class="sxs-lookup"><span data-stu-id="3a66a-127">Use the **Requery** action to requery the source of the object or one of its controls.</span></span> <span data-ttu-id="3a66a-128">Используйте действие **ShowAllRecords** для отображения последних записей и удаления примененных фильтров.</span><span class="sxs-lookup"><span data-stu-id="3a66a-128">Use the **ShowAllRecords** action to display the most recent records and remove any applied filters.</span></span>
> - <span data-ttu-id="3a66a-129">Действие **RepaintObject** не имеет того же эффекта, что и нажатие обновления в группе **Records** на вкладке **Home,** в которой показаны изменения, внесенные вами или другими пользователями к отображаемой в настоящее время записи в формах и таблицах данных. </span><span class="sxs-lookup"><span data-stu-id="3a66a-129">The **RepaintObject** action doesn't have the same effect as clicking **Refresh** in the **Records** group on the **Home** tab, which shows any changes you or other users have made to the currently displayed records in forms and datasheets.</span></span>

<span data-ttu-id="3a66a-130">Чтобы выполнить действие **RepaintObject** в Visual Basic для приложений (VBA), используйте метод **RepaintObject** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="3a66a-130">To run the **RepaintObject** action in a Visual Basic for Applications (VBA) module, use the **RepaintObject** method of the **DoCmd** object.</span></span>

