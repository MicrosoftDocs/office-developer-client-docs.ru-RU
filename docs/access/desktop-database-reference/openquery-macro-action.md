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
# <a name="openquery-macro-action"></a><span data-ttu-id="6ab15-102">Макрокоманда OpenQuery</span><span class="sxs-lookup"><span data-stu-id="6ab15-102">OpenQuery macro action</span></span>

<span data-ttu-id="6ab15-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ab15-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6ab15-104">С помощью действия **OPENQUERY** можно открыть запрос на выборку или перекрестный запрос в режиме таблицы, конструктора или в режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="6ab15-104">You can use the **OpenQuery** action to open a select or crosstab query in Datasheet view, Design view, or Print Preview.</span></span> <span data-ttu-id="6ab15-105">Это действие выполняет запрос на изменение.</span><span class="sxs-lookup"><span data-stu-id="6ab15-105">This action runs an action query.</span></span> <span data-ttu-id="6ab15-106">Вы также можете выбрать режим ввода данных для запроса.</span><span class="sxs-lookup"><span data-stu-id="6ab15-106">You can also select a data entry mode for the query.</span></span>

> [!NOTE]
> <span data-ttu-id="6ab15-107">Это действие доступно только в среде базы данных Access (MDB или ACCDB).</span><span class="sxs-lookup"><span data-stu-id="6ab15-107">This action is only available in the Access database environment (.mdb or .accdb).</span></span> <span data-ttu-id="6ab15-108">Ознакомьтесь с действиями **опенвиев**, **опенсторедпроцедуре**или **опенфунктион** , если вы используете среду проекта Access (ADP).</span><span class="sxs-lookup"><span data-stu-id="6ab15-108">See the **OpenView**, **OpenStoredProcedure**, or **OpenFunction** actions if you are using the Access project environment (.adp).</span></span>

## <a name="setting"></a><span data-ttu-id="6ab15-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="6ab15-109">Setting</span></span>

<span data-ttu-id="6ab15-110">Действие **OPENQUERY** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="6ab15-110">The **OpenQuery** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6ab15-111">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="6ab15-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6ab15-112">Описание</span><span class="sxs-lookup"><span data-stu-id="6ab15-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ab15-113"><strong>Название запроса</strong></span><span class="sxs-lookup"><span data-stu-id="6ab15-113"><strong>Query Name</strong></span></span></p></td>
<td><p><span data-ttu-id="6ab15-114">Имя запроса, который требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="6ab15-114">The name of the query to open.</span></span> <span data-ttu-id="6ab15-115">В поле <strong>имя запроса</strong> в разделе <strong>аргументы макрокоманды</strong> области построителя макросов отображаются все запросы в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="6ab15-115">The <strong>Query Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all queries in the current database.</span></span> <span data-ttu-id="6ab15-116">Это обязательный аргумент. При запуске макроса, содержащего действие <strong>OPENQUERY</strong> , в библиотечной базе данных Microsoft Access сначала ищет запрос с этим именем в библиотечной базе данных, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="6ab15-116">This is a required argument.If you run a macro containing the <strong>OpenQuery</strong> action in a library database, Microsoft Access first looks for the query with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ab15-117"><strong>Просмотр</strong></span><span class="sxs-lookup"><span data-stu-id="6ab15-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="6ab15-118">Представление, в котором будет открыт запрос.</span><span class="sxs-lookup"><span data-stu-id="6ab15-118">The view in which the query will open.</span></span> <span data-ttu-id="6ab15-119">В поле <strong>вид</strong> щелкните <strong>Таблица</strong>, <strong>Макет</strong>, <strong>Предварительный просмотр</strong>, <strong>Сводная таблица</strong>или <strong>Сводная диаграмма</strong> .</span><span class="sxs-lookup"><span data-stu-id="6ab15-119">Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="6ab15-120">Значение по умолчанию — <strong>Таблица</strong>.</span><span class="sxs-lookup"><span data-stu-id="6ab15-120">The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ab15-121"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="6ab15-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="6ab15-122">Режим ввода данных для запроса.</span><span class="sxs-lookup"><span data-stu-id="6ab15-122">The data entry mode for the query.</span></span> <span data-ttu-id="6ab15-123">Это относится только к запросам, открываемым в представлении таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="6ab15-123">This applies only to queries opened in Datasheet view.</span></span> <span data-ttu-id="6ab15-124">Нажмите кнопку <strong>Добавить</strong> (пользователь может добавлять новые записи, но не может изменять существующие), <strong>изменять</strong> (пользователь может изменять существующие записи и добавлять новые записи) или <strong>только для чтения</strong> (пользователи могут только просматривать записи).</span><span class="sxs-lookup"><span data-stu-id="6ab15-124">Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="6ab15-125">Значение по умолчанию — <strong>Edit</strong>.</span><span class="sxs-lookup"><span data-stu-id="6ab15-125">The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6ab15-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="6ab15-126">Remarks</span></span>

<span data-ttu-id="6ab15-127">Если для аргумента **View** используется **Таблица** , Access отображает набор результатов, если запрос является запросом на выборку, перекрестный запрос, объединение или запрос к серверу, для свойства **ReturnsRecords** которого задано значение **"Да"**. и выполняет запрос, если он является действием, определением данных или запросом к серверу, свойство **ReturnsRecords** которого имеет значение " **нет**".</span><span class="sxs-lookup"><span data-stu-id="6ab15-127">If you use **Datasheet** for the **View** argument, Access displays the result set if the query is a select, crosstab, union, or pass-through query whose **ReturnsRecords** property is set to **Yes**; and it runs the query if it is an action, data-definition, or pass-through query whose **ReturnsRecords** property is set to **No**.</span></span>

<span data-ttu-id="6ab15-128">Действие **OPENQUERY** аналогично двойному щелчку запроса в области навигации или щелчку правой кнопкой мыши запроса в области навигации и выбора представления.</span><span class="sxs-lookup"><span data-stu-id="6ab15-128">The **OpenQuery** action is similar to double-clicking the query in the Navigation Pane, or right-clicking the query in the Navigation Pane and selecting a view.</span></span> <span data-ttu-id="6ab15-129">С помощью этого действия можно выбрать дополнительные параметры.</span><span class="sxs-lookup"><span data-stu-id="6ab15-129">With this action you can select additional options.</span></span>

> [!TIP]
> - <span data-ttu-id="6ab15-130">Вы можете перетащить запрос из области навигации в строку макрокоманды.</span><span class="sxs-lookup"><span data-stu-id="6ab15-130">You can drag a query from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="6ab15-131">При этом автоматически создается действие **OPENQUERY** , которое открывает запрос в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="6ab15-131">This automatically creates an **OpenQuery** action that opens the query in Datasheet view.</span></span> <span data-ttu-id="6ab15-132">При переходе в режим конструктора, пока запрос открыт, удаляет значение аргумента **режим данных** для запроса.</span><span class="sxs-lookup"><span data-stu-id="6ab15-132">Switching to Design view while the query is open removes the **Data Mode** argument setting for the query.</span></span> <span data-ttu-id="6ab15-133">Этот параметр не действует, даже если пользователь возвращается в режим таблицы.</span><span class="sxs-lookup"><span data-stu-id="6ab15-133">This setting isn't in effect even if the user returns to Datasheet view.</span></span>
> - <span data-ttu-id="6ab15-134">Если вы не хотите отображать системные сообщения, которые обычно отображаются при выполнении запроса на изменение (указывает, что это запрос на изменение, в котором отображается количество затронутых записей), можно использовать действие **сетварнингс** , чтобы отключить отображение этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="6ab15-134">If you don't want to display the system messages that normally appear when an action query is run (indicating it is an action query and showing how many records will be affected), you can use the **SetWarnings** action to suppress the display of these messages.</span></span>

<span data-ttu-id="6ab15-135">Чтобы выполнить действие **OPENQUERY** в модуле Visual Basic для приложений (VBA), используйте метод **OPENQUERY** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="6ab15-135">To run the **OpenQuery** action in a Visual Basic for Applications (VBA) module, use the **OpenQuery** method of the **DoCmd** object.</span></span>

