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
# <a name="repaintobject-macro-action"></a><span data-ttu-id="6e428-102">Макрокоманда RepaintObject</span><span class="sxs-lookup"><span data-stu-id="6e428-102">RepaintObject macro action</span></span>

<span data-ttu-id="6e428-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e428-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6e428-104">Вы можете использовать действие **репаинтобжект** для выполнения всех ожидающих обновлений экрана для указанного объекта базы данных или для активного объекта Database, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="6e428-104">You can use the **RepaintObject** action to complete any pending screen updates for a specified database object or for the active database object, if none is specified.</span></span> <span data-ttu-id="6e428-105">Такие обновления включают все ожидающие пересчеты для элементов управления объекта.</span><span class="sxs-lookup"><span data-stu-id="6e428-105">Such updates include any pending recalculations for the object's controls.</span></span>

## <a name="setting"></a><span data-ttu-id="6e428-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="6e428-106">Setting</span></span>

<span data-ttu-id="6e428-107">Макрокоманда **репаинтобжект** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="6e428-107">The **RepaintObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e428-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="6e428-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6e428-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6e428-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e428-110"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="6e428-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="6e428-111">Тип объекта, который необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="6e428-111">The type of object to repaint.</span></span> <span data-ttu-id="6e428-112">Щелкните <strong>Таблица</strong>, <strong>запрос</strong>, <strong>форма</strong>, <strong>отчет</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>Страница доступа к данным</strong>, <strong>представление сервера</strong>, <strong>схема</strong>, <strong>хранимая процедура</strong>или <strong>функция</strong> в <strong>типе объекта. </strong>в разделе <strong>аргументы макрокоманды</strong> в панели построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="6e428-112">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="6e428-113">Чтобы выбрать активный объект, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="6e428-113">Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e428-114"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="6e428-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="6e428-115">Имя объекта, который необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="6e428-115">The name of the object to repaint.</span></span> <span data-ttu-id="6e428-116">Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="6e428-116">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="6e428-117">Если оставить аргумент " <strong>тип объекта</strong> " пустым, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="6e428-117">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6e428-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="6e428-118">Remarks</span></span>

<span data-ttu-id="6e428-119">Microsoft Access ждет завершения отложенных обновлений экрана, пока не завершит другие задачи, ожидающие выполнения.</span><span class="sxs-lookup"><span data-stu-id="6e428-119">Microsoft Access waits to complete pending screen updates until it finishes other pending tasks.</span></span> <span data-ttu-id="6e428-120">С помощью этого действия можно принудительно выполнить немедленный перерисовку элементов управления в указанном объекте.</span><span class="sxs-lookup"><span data-stu-id="6e428-120">With this action, you can force immediate repainting of the controls in the specified object.</span></span> <span data-ttu-id="6e428-121">Вы можете использовать это действие:</span><span class="sxs-lookup"><span data-stu-id="6e428-121">You can use this action:</span></span>

- <span data-ttu-id="6e428-122">При использовании действия **SetValue** для изменения значений в нескольких элементах управления.</span><span class="sxs-lookup"><span data-stu-id="6e428-122">When you use the **SetValue** action to change values in a number of controls.</span></span> <span data-ttu-id="6e428-123">Access может не показывать изменения немедленно, особенно если другие элементы управления (например, вычисляемые элементы управления) зависят от значений в измененных элементах управления.</span><span class="sxs-lookup"><span data-stu-id="6e428-123">Access might not show the changes immediately, especially if other controls (such as calculated controls) depend on values in the changed controls.</span></span>

- <span data-ttu-id="6e428-124">Если необходимо убедиться, что просматриваемая форма отображает данные во всех элементах управления.</span><span class="sxs-lookup"><span data-stu-id="6e428-124">When you want to make sure that the form you are viewing displays data in all of its controls.</span></span> <span data-ttu-id="6e428-125">Например, элементы управления, содержащие объекты OLE, не отображают свои данные сразу после открытия формы.</span><span class="sxs-lookup"><span data-stu-id="6e428-125">For example, controls containing OLE objects don't display their data immediately after you open a form.</span></span>

> [!NOTE]
> - <span data-ttu-id="6e428-126">Это действие не приводит к повторному созданию базы данных, поэтому не отображает новые и измененные записи и не удаляет удаленные записи из базовой таблицы или запроса объекта.</span><span class="sxs-lookup"><span data-stu-id="6e428-126">This action doesn't cause a requery of the database, so it doesn't show new and changed records or remove deleted records from the object's underlying table or query.</span></span> <span data-ttu-id="6e428-127">Используйте действие **Requery** для запроса источника объекта или одного из его элементов управления.</span><span class="sxs-lookup"><span data-stu-id="6e428-127">Use the **Requery** action to requery the source of the object or one of its controls.</span></span> <span data-ttu-id="6e428-128">Используйте действие **шоваллрекордс** , чтобы отобразить последние записи и удалить все примененные фильтры.</span><span class="sxs-lookup"><span data-stu-id="6e428-128">Use the **ShowAllRecords** action to display the most recent records and remove any applied filters.</span></span>
> - <span data-ttu-id="6e428-129">Действие **репаинтобжект** не оказывает того же результата, что и нажатие кнопки **Обновить** в группе **записи** на вкладке **Главная** , в которой отображаются все изменения, внесенные вами или другими пользователями в текущие записи в формах и таблицах.</span><span class="sxs-lookup"><span data-stu-id="6e428-129">The **RepaintObject** action doesn't have the same effect as clicking **Refresh** in the **Records** group on the **Home** tab, which shows any changes you or other users have made to the currently displayed records in forms and datasheets.</span></span>

<span data-ttu-id="6e428-130">Чтобы запустить действие **репаинтобжект** в модуле Visual Basic для приложений (VBA), используйте метод **репаинтобжект** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="6e428-130">To run the **RepaintObject** action in a Visual Basic for Applications (VBA) module, use the **RepaintObject** method of the **DoCmd** object.</span></span>

