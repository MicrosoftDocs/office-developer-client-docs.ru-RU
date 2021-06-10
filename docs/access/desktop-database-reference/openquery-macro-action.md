---
title: Макрокоманда OpenQuery
TOCTitle: OpenQuery macro action
ms:assetid: 64bfce73-aeaf-9a78-895c-492e5da43ded
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195094(v=office.15)
ms:contentKeyID: 48545298
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89069
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3294efe5ea1ab0f82be19f5c64a51287cc4df9b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288345"
---
# <a name="openquery-macro-action"></a><span data-ttu-id="9aac2-102">Макрокоманда OpenQuery</span><span class="sxs-lookup"><span data-stu-id="9aac2-102">OpenQuery macro action</span></span>

<span data-ttu-id="9aac2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9aac2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9aac2-104">Вы можете использовать **действие OpenQuery** для открытия выбора или перекрестного запроса в представлении Datasheet, Представлении дизайна или Предварительном просмотре печати.</span><span class="sxs-lookup"><span data-stu-id="9aac2-104">You can use the **OpenQuery** action to open a select or crosstab query in Datasheet view, Design view, or Print Preview.</span></span> <span data-ttu-id="9aac2-105">Это действие выполняет запрос действий.</span><span class="sxs-lookup"><span data-stu-id="9aac2-105">This action runs an action query.</span></span> <span data-ttu-id="9aac2-106">Вы также можете выбрать режим ввода данных для запроса.</span><span class="sxs-lookup"><span data-stu-id="9aac2-106">You can also select a data entry mode for the query.</span></span>

> [!NOTE]
> <span data-ttu-id="9aac2-107">Это действие доступно только в среде базы данных Access (.mdb или .accdb).</span><span class="sxs-lookup"><span data-stu-id="9aac2-107">This action is only available in the Access database environment (.mdb or .accdb).</span></span> <span data-ttu-id="9aac2-108">См. **действия OpenView,** **OpenStoredProcedure** или **OpenFunction,** если вы используете среду проекта Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="9aac2-108">See the **OpenView**, **OpenStoredProcedure**, or **OpenFunction** actions if you are using the Access project environment (.adp).</span></span>

## <a name="setting"></a><span data-ttu-id="9aac2-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="9aac2-109">Setting</span></span>

<span data-ttu-id="9aac2-110">Действие **OpenQuery** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="9aac2-110">The **OpenQuery** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9aac2-111">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="9aac2-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="9aac2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9aac2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9aac2-113"><strong>Название запроса</strong></span><span class="sxs-lookup"><span data-stu-id="9aac2-113"><strong>Query Name</strong></span></span></p></td>
<td><p><span data-ttu-id="9aac2-114">Имя открываемого запроса.</span><span class="sxs-lookup"><span data-stu-id="9aac2-114">The name of the query to open.</span></span> <span data-ttu-id="9aac2-115">Поле <strong>Имя запроса</strong> в разделе <strong>Аргументы</strong> действий в области Macro Builder отображает все запросы в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="9aac2-115">The <strong>Query Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all queries in the current database.</span></span> <span data-ttu-id="9aac2-116">Это необходимый аргумент. Если вы запустите макрос, содержащий действие <strong>OpenQuery</strong> в базе данных библиотеки, Microsoft Access сначала ищет запрос с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="9aac2-116">This is a required argument.If you run a macro containing the <strong>OpenQuery</strong> action in a library database, Microsoft Access first looks for the query with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aac2-117"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="9aac2-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="9aac2-118">Представление, в котором откроется запрос.</span><span class="sxs-lookup"><span data-stu-id="9aac2-118">The view in which the query will open.</span></span> <span data-ttu-id="9aac2-119">Щелкните <strong>таблицу</strong>данных, <strong>дизайн,</strong> <strong>предварительный</strong>просмотр печати, <strong>pivotTable</strong>или сводная диаграмма в <strong>поле Просмотр.</strong> <strong></strong></span><span class="sxs-lookup"><span data-stu-id="9aac2-119">Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="9aac2-120">По умолчанию — <strong>таблица данных.</strong></span><span class="sxs-lookup"><span data-stu-id="9aac2-120">The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aac2-121"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="9aac2-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="9aac2-122">Режим ввода данных для запроса.</span><span class="sxs-lookup"><span data-stu-id="9aac2-122">The data entry mode for the query.</span></span> <span data-ttu-id="9aac2-123">Это касается только запросов, открытых в представлении Datasheet.</span><span class="sxs-lookup"><span data-stu-id="9aac2-123">This applies only to queries opened in Datasheet view.</span></span> <span data-ttu-id="9aac2-124">Щелкните <strong>Добавить</strong> (пользователь может добавлять новые записи, но не может изменять существующие записи), <strong></strong> изменить (пользователь может изменять существующие записи и добавлять новые записи) или <strong>Только</strong> для чтения (пользователь может просматривать только записи).</span><span class="sxs-lookup"><span data-stu-id="9aac2-124">Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="9aac2-125">По умолчанию <strong>изменить</strong>.</span><span class="sxs-lookup"><span data-stu-id="9aac2-125">The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9aac2-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="9aac2-126">Remarks</span></span>

<span data-ttu-id="9aac2-127">Если вы  используете таблицу данных для аргумента **Просмотр,** Access отображает набор результатов, если запрос является выбором, перекрестием, союзом или сквозным запросом, свойство **ReturnsRecords** которого задалось **да;** и выполняет запрос, если это действие, определение данных или сквозной запрос, свойство **ReturnsRecords** которого задано **No**.</span><span class="sxs-lookup"><span data-stu-id="9aac2-127">If you use **Datasheet** for the **View** argument, Access displays the result set if the query is a select, crosstab, union, or pass-through query whose **ReturnsRecords** property is set to **Yes**; and it runs the query if it is an action, data-definition, or pass-through query whose **ReturnsRecords** property is set to **No**.</span></span>

<span data-ttu-id="9aac2-128">Действие **OpenQuery** аналогично двойному нажатию запроса в области навигации или правой щелкнуть запрос в области навигации и выбрать представление.</span><span class="sxs-lookup"><span data-stu-id="9aac2-128">The **OpenQuery** action is similar to double-clicking the query in the Navigation Pane, or right-clicking the query in the Navigation Pane and selecting a view.</span></span> <span data-ttu-id="9aac2-129">С помощью этого действия можно выбрать дополнительные параметры.</span><span class="sxs-lookup"><span data-stu-id="9aac2-129">With this action you can select additional options.</span></span>

> [!TIP]
> - <span data-ttu-id="9aac2-130">Запрос можно перетаскивать из области навигации в строку действий макроса.</span><span class="sxs-lookup"><span data-stu-id="9aac2-130">You can drag a query from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="9aac2-131">Это автоматически создает действие **OpenQuery,** которое открывает запрос в представлении Datasheet.</span><span class="sxs-lookup"><span data-stu-id="9aac2-131">This automatically creates an **OpenQuery** action that opens the query in Datasheet view.</span></span> <span data-ttu-id="9aac2-132">Переход к представлению Design во время открытия запроса удаляет параметр **аргумента "Режим** данных" для запроса.</span><span class="sxs-lookup"><span data-stu-id="9aac2-132">Switching to Design view while the query is open removes the **Data Mode** argument setting for the query.</span></span> <span data-ttu-id="9aac2-133">Этот параметр не действует, даже если пользователь возвращается в представление Datasheet.</span><span class="sxs-lookup"><span data-stu-id="9aac2-133">This setting isn't in effect even if the user returns to Datasheet view.</span></span>
> - <span data-ttu-id="9aac2-134">Если вы не хотите отображать системные сообщения, которые обычно отображаются при запуске запроса действий (указывающее, что это запрос действия и показывая, сколько записей будет затронуто), вы можете использовать действие **SetWarnings** для подавления отображения этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="9aac2-134">If you don't want to display the system messages that normally appear when an action query is run (indicating it is an action query and showing how many records will be affected), you can use the **SetWarnings** action to suppress the display of these messages.</span></span>

<span data-ttu-id="9aac2-135">Чтобы выполнить **действие OpenQuery** в Visual Basic для приложений (VBA), используйте метод **OpenQuery** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="9aac2-135">To run the **OpenQuery** action in a Visual Basic for Applications (VBA) module, use the **OpenQuery** method of the **DoCmd** object.</span></span>

