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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288310"
---
# <a name="openstoredprocedure-macro-action"></a><span data-ttu-id="b1783-102">Макрокоманда OpenStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="b1783-102">OpenStoredProcedure macro action</span></span>

<span data-ttu-id="b1783-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1783-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b1783-104">В проекте Access можно использовать действие **OpenStoredProcedure,** чтобы открыть хранимую процедуру в представлении таблицы, представлении конструктора хранимой процедуры или предварительного просмотра печати.</span><span class="sxs-lookup"><span data-stu-id="b1783-104">In an Access project, you can use the **OpenStoredProcedure** action to open a stored procedure in Datasheet view, stored procedure Design view, or Print Preview.</span></span> <span data-ttu-id="b1783-105">Это действие выполняет именоваемую хранимую процедуру при запуске в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="b1783-105">This action runs the named stored procedure when opened in Datasheet view.</span></span> <span data-ttu-id="b1783-106">Можно выбрать режим ввода данных для хранимой процедуры и ограничить отображаемую запись.</span><span class="sxs-lookup"><span data-stu-id="b1783-106">You can select the data entry mode for the stored procedure and restrict the records that the stored procedure displays.</span></span>

> [!NOTE]
> <span data-ttu-id="b1783-107">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="b1783-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="b1783-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="b1783-108">Setting</span></span>

<span data-ttu-id="b1783-109">Действие **OpenStoredProcedure** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="b1783-109">The **OpenStoredProcedure** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1783-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="b1783-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b1783-111">Описание</span><span class="sxs-lookup"><span data-stu-id="b1783-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1783-112"><strong>Имя процедуры</strong></span><span class="sxs-lookup"><span data-stu-id="b1783-112"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b1783-113">Имя хранимой процедуры для открытия.</span><span class="sxs-lookup"><span data-stu-id="b1783-113">The name of the stored procedure to open.</span></span> <span data-ttu-id="b1783-114">В <strong>поле "Имя процедуры"</strong> в разделе <strong>"Аргументы</strong> действий" области построитель макроса показаны все хранимые процедуры в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="b1783-114">The <strong>Procedure Name box</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all stored procedures in the current database.</span></span> <span data-ttu-id="b1783-115">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="b1783-115">This is a required argument.</span></span> <span data-ttu-id="b1783-116">При запуске макроса, содержащего действие <strong>OpenStoredProcedure</strong> в базе данных библиотеки, Microsoft Access сначала ищет хранимую процедуру с этим именем сначала в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="b1783-116">If you run a macro containing the <strong>OpenStoredProcedure</strong> action in a library database, Microsoft Access first looks for the stored procedure with this name first in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1783-117"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="b1783-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="b1783-118">Представление, в котором откроется хранимая процедура.</span><span class="sxs-lookup"><span data-stu-id="b1783-118">The view in which the stored procedure will open.</span></span> <span data-ttu-id="b1783-119">Щелкните <strong></strong> <strong>"Таблица</strong> <strong>данных", "Конструктор",</strong>"Предварительный <strong>просмотр",</strong> <strong>"Сводная диаграмма</strong> в поле <strong>"Вид".</strong></span><span class="sxs-lookup"><span data-stu-id="b1783-119">Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="b1783-120">Значение по умолчанию <strong>— Таблица.</strong></span><span class="sxs-lookup"><span data-stu-id="b1783-120">The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1783-121"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="b1783-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="b1783-122">Режим ввода данных для хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="b1783-122">The data entry mode for the stored procedure.</span></span> <span data-ttu-id="b1783-123">Это относится только к хранимой процедуре, открытой в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="b1783-123">This applies only to stored procedures opened in Datasheet view.</span></span> <span data-ttu-id="b1783-124">Нажмите <strong></strong> кнопку "Добавить" (пользователь может добавлять новые записи, но не может просматривать или редактировать существующие <strong>записи),</strong> изменять (пользователь может просматривать или редактировать существующие записи и добавлять новые записи) или только для чтения <strong>(пользователь</strong> может просматривать только записи).</span><span class="sxs-lookup"><span data-stu-id="b1783-124">Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="b1783-125">Значение по умолчанию <strong>— Edit</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1783-125">The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="b1783-126">Заметки</span><span class="sxs-lookup"><span data-stu-id="b1783-126">Remarks</span></span>

<span data-ttu-id="b1783-127">Это действие аналогично двойному щелчку хранимой процедуры в области навигации или щелчку правой кнопкой мыши хранимой процедуры в области навигации и выбору нужной команды.</span><span class="sxs-lookup"><span data-stu-id="b1783-127">This action is similar to double-clicking the stored procedure in the Navigation Pane, or right-clicking the stored procedure in the Navigation Pane and selecting the command you want.</span></span>

<span data-ttu-id="b1783-128">При переключении в режим конструктора во время  открытия хранимой процедуры удаляется параметр аргумента режима данных для хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="b1783-128">Switching to Design view while the stored procedure is open removes the **Data Mode** argument setting for the stored procedure.</span></span> <span data-ttu-id="b1783-129">Этот параметр не действует, даже если пользователь возвращается в представление таблицы.</span><span class="sxs-lookup"><span data-stu-id="b1783-129">This setting is not in effect, even if the user returns to Datasheet view.</span></span>

> [!TIP]
> - <span data-ttu-id="b1783-130">Вы можете перетащить хранимую процедуру из области навигации в строку макроса.</span><span class="sxs-lookup"><span data-stu-id="b1783-130">You can drag a stored procedure from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="b1783-131">При этом автоматически создается действие **OpenStoredProcedure,** которое открывает хранимую процедуру в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="b1783-131">This automatically creates an **OpenStoredProcedure** action that opens the stored procedure in Datasheet view.</span></span>
> - <span data-ttu-id="b1783-132">Если вы не хотите отображать системные сообщения, которые обычно отображаются при запуске хранимой процедуры (указывая, что это хранимая процедура и показывает, сколько записей будет затронуто), можно использовать действие **SetWarning,** чтобы запретить отображение этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="b1783-132">If you do not want to display the system messages that normally appear when a stored procedure is run (indicating it is a stored procedure and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="b1783-133">Чтобы запустить действие **OpenStoredProcedure** в модуле Visual Basic для приложений (VBA), используйте метод **OpenStoredProcedure** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="b1783-133">To run the **OpenStoredProcedure** action in a Visual Basic for Applications (VBA) module, use the **OpenStoredProcedure** method of the **DoCmd** object.</span></span>

