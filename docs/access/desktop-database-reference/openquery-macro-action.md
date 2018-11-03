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
ms.openlocfilehash: 1e5e031b0dc89626a40934cb42f8f54a0eb8d057
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928112"
---
# <a name="openquery-macro-action"></a><span data-ttu-id="1024b-102">Макрокоманда OpenQuery</span><span class="sxs-lookup"><span data-stu-id="1024b-102">OpenQuery macro action</span></span>


<span data-ttu-id="1024b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1024b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1024b-104">Можно использовать **ОткрытьЗапрос** Открытие запроса выборку в режиме таблицы, конструктора или просмотра.</span><span class="sxs-lookup"><span data-stu-id="1024b-104">You can use the **OpenQuery** action to open a select or crosstab query in Datasheet view, Design view, or Print Preview.</span></span> <span data-ttu-id="1024b-105">Это действие Запуск запроса.</span><span class="sxs-lookup"><span data-stu-id="1024b-105">This action runs an action query.</span></span> <span data-ttu-id="1024b-106">Также можно выбрать режим ввода данных для запроса.</span><span class="sxs-lookup"><span data-stu-id="1024b-106">You can also select a data entry mode for the query.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1024b-107">Это действие доступно только в среде базы данных Access (MDB- или .accdb).</span><span class="sxs-lookup"><span data-stu-id="1024b-107">This action is only available in the Access database environment (.mdb or .accdb).</span></span> <span data-ttu-id="1024b-108">Посмотреть <STRONG>OpenView</STRONG>, <STRONG>ОткрытьСохраненнуюПроцедуру</STRONG>или <STRONG>ОткрытьФункцию</STRONG> действия при использовании среды проекта Microsoft Access (файлы с расширением ADP).</span><span class="sxs-lookup"><span data-stu-id="1024b-108">See the <STRONG>OpenView</STRONG>, <STRONG>OpenStoredProcedure</STRONG>, or <STRONG>OpenFunction</STRONG> actions if you are using the Access project environment (.adp).</span></span></P>



## <a name="setting"></a><span data-ttu-id="1024b-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="1024b-109">Setting</span></span>

<span data-ttu-id="1024b-110">**ОткрытьЗапрос** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="1024b-110">The **OpenQuery** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1024b-111">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="1024b-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="1024b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="1024b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1024b-113"><strong>Имя запроса</strong></span><span class="sxs-lookup"><span data-stu-id="1024b-113"><strong>Query Name</strong></span></span></p></td>
<td><p><span data-ttu-id="1024b-114">Имя запроса, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="1024b-114">The name of the query to open.</span></span> <span data-ttu-id="1024b-115">В поле <strong>Имя запроса</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов содержит все запросы текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="1024b-115">The <strong>Query Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all queries in the current database.</span></span> <span data-ttu-id="1024b-116">Этот параметр является обязательным. Если макрос, содержащий <strong>ОткрытьЗапрос в базе данных библиотеки</strong> , Microsoft Access сначала выполняет поиск запроса с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="1024b-116">This is a required argument.If you run a macro containing the <strong>OpenQuery</strong> action in a library database, Microsoft Access first looks for the query with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1024b-117"><strong>Просмотр</strong></span><span class="sxs-lookup"><span data-stu-id="1024b-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="1024b-118">Представление, в котором будут открываться запроса.</span><span class="sxs-lookup"><span data-stu-id="1024b-118">The view in which the query will open.</span></span> <span data-ttu-id="1024b-119">Выберите <strong>таблицы</strong>, <strong>разработки</strong>, <strong>Режим предварительного просмотра</strong>, <strong>сводной таблицы</strong>или <strong>сводной диаграммы</strong> в поле <strong>View</strong> .</span><span class="sxs-lookup"><span data-stu-id="1024b-119">Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="1024b-120">Значение по умолчанию — <strong>таблицы данных</strong>.</span><span class="sxs-lookup"><span data-stu-id="1024b-120">The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1024b-121"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="1024b-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="1024b-122">Режим ввода данных для запроса.</span><span class="sxs-lookup"><span data-stu-id="1024b-122">The data entry mode for the query.</span></span> <span data-ttu-id="1024b-123">Применяется только к запросам, открываемым в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="1024b-123">This applies only to queries opened in Datasheet view.</span></span> <span data-ttu-id="1024b-124">Нажмите кнопку <strong>Add</strong> (пользователь может добавлять новые записи, но не могут изменять существующие записи), <strong>Изменение</strong> (пользователь может изменять существующие записи и добавление новых записей), или <strong>Только для чтения</strong> (пользователь может только просматривать записи).</span><span class="sxs-lookup"><span data-stu-id="1024b-124">Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="1024b-125">Значение по умолчанию — <strong>Изменить</strong>.</span><span class="sxs-lookup"><span data-stu-id="1024b-125">The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1024b-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="1024b-126">Remarks</span></span>

<span data-ttu-id="1024b-127">При использовании для аргумента **представления** **таблицы данных** Access отображает набор результатов, если запрос будет выбрать, перекрестного объединения, или запроса к серверу, свойство **ReturnsRecords** установлен в значение **Yes**; и выполняет запрос, если это действие, определение данных или запроса к серверу, свойство **ReturnsRecords** задано значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="1024b-127">If you use **Datasheet** for the **View** argument, Access displays the result set if the query is a select, crosstab, union, or pass-through query whose **ReturnsRecords** property is set to **Yes**; and it runs the query if it is an action, data-definition, or pass-through query whose **ReturnsRecords** property is set to **No**.</span></span>

<span data-ttu-id="1024b-128">**ОткрытьЗапрос** аналогично дважды щелкнув запросов на левой панели навигации или щелкнув правой кнопкой мыши запрос на левой панели навигации и выбрав представления.</span><span class="sxs-lookup"><span data-stu-id="1024b-128">The **OpenQuery** action is similar to double-clicking the query in the Navigation Pane, or right-clicking the query in the Navigation Pane and selecting a view.</span></span> <span data-ttu-id="1024b-129">С помощью этого действия можно выбрать дополнительные параметры.</span><span class="sxs-lookup"><span data-stu-id="1024b-129">With this action you can select additional options.</span></span>

<span data-ttu-id="1024b-130">\*\*Советы \*\*</span><span class="sxs-lookup"><span data-stu-id="1024b-130">**Tips**</span></span>

  - <span data-ttu-id="1024b-131">Можно перетащить запрос из области переходов в строку действие в макросе.</span><span class="sxs-lookup"><span data-stu-id="1024b-131">You can drag a query from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="1024b-132">Это автоматически создает **OpenQuery** действие, которое открывается, в представлении таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="1024b-132">This automatically creates an **OpenQuery** action that opens the query in Datasheet view.</span></span> <span data-ttu-id="1024b-133">Переключиться в режим разработки, когда запрос открыт удаляется значение аргумента **Режим данных** для запроса.</span><span class="sxs-lookup"><span data-stu-id="1024b-133">Switching to Design view while the query is open removes the **Data Mode** argument setting for the query.</span></span> <span data-ttu-id="1024b-134">Этот параметр не действует даже в том случае, если пользователь возвращается в режим таблицы.</span><span class="sxs-lookup"><span data-stu-id="1024b-134">This setting isn't in effect even if the user returns to Datasheet view.</span></span>

  - <span data-ttu-id="1024b-135">Если не хотите отобразить системные сообщения, которые появляются при выполнении запроса (это запроса и показывают количество записей затрагиваются), можно использовать действие **УстановитьСообщения** отображение этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="1024b-135">If you don't want to display the system messages that normally appear when an action query is run (indicating it is an action query and showing how many records will be affected), you can use the **SetWarnings** action to suppress the display of these messages.</span></span>

<span data-ttu-id="1024b-136">Чтобы запустить **ОткрытьЗапрос** в Visual Basic для приложений (VBA) модуль, используйте метод **OpenQuery** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="1024b-136">To run the **OpenQuery** action in a Visual Basic for Applications (VBA) module, use the **OpenQuery** method of the **DoCmd** object.</span></span>

