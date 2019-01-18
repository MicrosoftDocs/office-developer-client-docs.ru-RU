---
title: Макрокоманда OpenStoredProcedure
TOCTitle: OpenStoredProcedure macro action
ms:assetid: b14dbb82-7c8a-0ace-e251-46599551a490
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822003(v=office.15)
ms:contentKeyID: 48547142
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm187628
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b972174e4fe7f3c0384b7483e17eb5ceb9e8bc15
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698773"
---
# <a name="openstoredprocedure-macro-action"></a><span data-ttu-id="c4feb-102">Макрокоманда OpenStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="c4feb-102">OpenStoredProcedure macro action</span></span>

<span data-ttu-id="c4feb-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4feb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c4feb-104">В проекте Microsoft Access можно использовать действие **ОткрытьСохраненнуюПроцедуру** для открытия хранимую процедуру в режиме таблицы данных, представление конструирования хранимую процедуру или режим предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="c4feb-104">In an Access project, you can use the **OpenStoredProcedure** action to open a stored procedure in Datasheet view, stored procedure Design view, or Print Preview.</span></span> <span data-ttu-id="c4feb-105">Это действие выполняется именованные хранимую процедуру при открытии в представлении таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="c4feb-105">This action runs the named stored procedure when opened in Datasheet view.</span></span> <span data-ttu-id="c4feb-106">Можно выбрать режим ввода данных для хранимые процедуры и ограничить записи, которые отображаются хранимую процедуру.</span><span class="sxs-lookup"><span data-stu-id="c4feb-106">You can select the data entry mode for the stored procedure and restrict the records that the stored procedure displays.</span></span>

> [!NOTE]
> <span data-ttu-id="c4feb-107">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="c4feb-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="c4feb-108">Setting</span><span class="sxs-lookup"><span data-stu-id="c4feb-108">Setting</span></span>

<span data-ttu-id="c4feb-109">Действие **ОткрытьСохраненнуюПроцедуру** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="c4feb-109">The **OpenStoredProcedure** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4feb-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="c4feb-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="c4feb-111">Описание</span><span class="sxs-lookup"><span data-stu-id="c4feb-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4feb-112"><strong>Имя процедуры</strong></span><span class="sxs-lookup"><span data-stu-id="c4feb-112"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="c4feb-113">Имя процедуры, которую следует открыть.</span><span class="sxs-lookup"><span data-stu-id="c4feb-113">The name of the stored procedure to open.</span></span> <span data-ttu-id="c4feb-114">Поле <strong>имя процедуры</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов содержит все хранимые процедуры в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="c4feb-114">The <strong>Procedure Name box</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all stored procedures in the current database.</span></span> <span data-ttu-id="c4feb-115">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="c4feb-115">This is a required argument.</span></span> <span data-ttu-id="c4feb-116">Если макрос, содержащий <strong>ОткрытьСохраненнуюПроцедуру</strong> действие в базе данных библиотеки, Microsoft Access сначала выполняет поиск хранимую процедуру с этим именем сначала в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="c4feb-116">If you run a macro containing the <strong>OpenStoredProcedure</strong> action in a library database, Microsoft Access first looks for the stored procedure with this name first in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4feb-117"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="c4feb-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="c4feb-118">Представление, в котором будут открываться хранимую процедуру.</span><span class="sxs-lookup"><span data-stu-id="c4feb-118">The view in which the stored procedure will open.</span></span> <span data-ttu-id="c4feb-119">Выберите <strong>таблицы</strong>, <strong>разработки</strong>, <strong>Режим предварительного просмотра</strong>, <strong>сводной таблицы</strong>или <strong>сводной диаграммы</strong> в поле <strong>View</strong> .</span><span class="sxs-lookup"><span data-stu-id="c4feb-119">Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="c4feb-120">Значение по умолчанию — <strong>таблицы данных</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4feb-120">The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4feb-121"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="c4feb-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="c4feb-122">Режим ввода данных для хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="c4feb-122">The data entry mode for the stored procedure.</span></span> <span data-ttu-id="c4feb-123">Это относится только к хранимых процедур, открытых в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="c4feb-123">This applies only to stored procedures opened in Datasheet view.</span></span> <span data-ttu-id="c4feb-124">Нажмите кнопку <strong>Add</strong> (пользователь может добавлять новые записи, но не могут просматривать и изменять существующие записи), <strong>Изменение</strong> (пользователь может просматривать или изменять существующие записи и добавление новых записей) или <strong>Только для чтения</strong> (пользователь может только просматривать записи).</span><span class="sxs-lookup"><span data-stu-id="c4feb-124">Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="c4feb-125">Значение по умолчанию — <strong>Изменить</strong>.</span><span class="sxs-lookup"><span data-stu-id="c4feb-125">The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="c4feb-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="c4feb-126">Remarks</span></span>

<span data-ttu-id="c4feb-127">Это действие аналогично дважды щелкнув хранимую процедуру на левой панели навигации или щелкнув правой кнопкой мыши хранимую процедуру на левой панели навигации и выбрав команду.</span><span class="sxs-lookup"><span data-stu-id="c4feb-127">This action is similar to double-clicking the stored procedure in the Navigation Pane, or right-clicking the stored procedure in the Navigation Pane and selecting the command you want.</span></span>

<span data-ttu-id="c4feb-128">Переключение в режим конструктора при открытом хранимую процедуру удаляется значение аргумента **Режим данных** для хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="c4feb-128">Switching to Design view while the stored procedure is open removes the **Data Mode** argument setting for the stored procedure.</span></span> <span data-ttu-id="c4feb-129">Этот параметр не действует, даже в том случае, если пользователь возвращается в режим таблицы.</span><span class="sxs-lookup"><span data-stu-id="c4feb-129">This setting is not in effect, even if the user returns to Datasheet view.</span></span>

> [!TIP]
> - <span data-ttu-id="c4feb-130">Хранимую процедуру можно перетаскивать из области переходов в строку действие в макросе.</span><span class="sxs-lookup"><span data-stu-id="c4feb-130">You can drag a stored procedure from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="c4feb-131">Это автоматически создает **ОткрытьСохраненнуюПроцедуру** действие, которое будет открыта хранимую процедуру в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="c4feb-131">This automatically creates an **OpenStoredProcedure** action that opens the stored procedure in Datasheet view.</span></span>
> - <span data-ttu-id="c4feb-132">Если вы не хотите вывод системных сообщений, которые появляются при запуске хранимую процедуру (это хранимые процедуры и показывают количество записей затрагиваются), можно использовать действие **УстановитьСообщения** для отмены вывода на отображение сообщения.</span><span class="sxs-lookup"><span data-stu-id="c4feb-132">If you do not want to display the system messages that normally appear when a stored procedure is run (indicating it is a stored procedure and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="c4feb-133">Чтобы выполнить действие **ОткрытьСохраненнуюПроцедуру** в Visual Basic для приложений (VBA) модуль, используйте метод **ОткрытьСохраненнуюПроцедуру** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="c4feb-133">To run the **OpenStoredProcedure** action in a Visual Basic for Applications (VBA) module, use the **OpenStoredProcedure** method of the **DoCmd** object.</span></span>

