---
title: Макрокоманда OpenFunction
TOCTitle: OpenFunction macro action
ms:assetid: 0446dbb9-c342-9225-27ba-b8a6892030e1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844833(v=office.15)
ms:contentKeyID: 48543005
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89179
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b13d21ef1bd8a95587eb78cd448f19f9fd0c24c0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720214"
---
# <a name="openfunction-macro-action"></a><span data-ttu-id="2e2da-102">Макрокоманда OpenFunction</span><span class="sxs-lookup"><span data-stu-id="2e2da-102">OpenFunction macro action</span></span>

<span data-ttu-id="2e2da-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2e2da-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2e2da-104">В проекте Microsoft Access можно использовать действие **ОткрытьФункцию** Открытие пользовательской функции в представлении таблицы данных, представление конструктора встроенные функции, представления SQL, текстовый редактор (для скалярные или таблице пользовательских функций), или режим предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="2e2da-104">In an Access project, you can use the **OpenFunction** action to open a user-defined function in Datasheet view, inline function Design view, SQL Text Editor view (for a scalar or table user-defined function), or Print Preview.</span></span> <span data-ttu-id="2e2da-105">Это действие выполняется пользовательской функции при открытии в представлении таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="2e2da-105">This action runs the user-defined function when opened in Datasheet view.</span></span> <span data-ttu-id="2e2da-106">Также можно выбрать режим ввода данных для пользовательских функций и ограничить записи, которые отображаются пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="2e2da-106">You can also select the data entry mode for the user-defined function and restrict the records that the user-defined function displays.</span></span>

> [!NOTE]
> <span data-ttu-id="2e2da-107">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="2e2da-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="2e2da-108">Setting</span><span class="sxs-lookup"><span data-stu-id="2e2da-108">Setting</span></span>

<span data-ttu-id="2e2da-109">Действие **ОткрытьФункцию** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="2e2da-109">The **OpenFunction** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2e2da-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="2e2da-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="2e2da-111">Описание</span><span class="sxs-lookup"><span data-stu-id="2e2da-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e2da-112"><strong>Имя функции</strong></span><span class="sxs-lookup"><span data-stu-id="2e2da-112"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="2e2da-113">Имя функции, определенной пользователем, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="2e2da-113">The name of the user-defined function to open.</span></span> <span data-ttu-id="2e2da-114">В поле <strong>Имя функции</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов показаны все пользовательские функции в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="2e2da-114">The <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all user-defined functions in the current database.</span></span> <span data-ttu-id="2e2da-115">Этот параметр является обязательным. Если макрос, содержащий действие <strong>функции</strong> в базе данных библиотеки, Microsoft Access сначала выполняет поиск функции с указанным именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="2e2da-115">This is a required argument.If you run a macro containing the <strong>Function</strong> action in a library database, Microsoft Access first looks for the function with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e2da-116"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="2e2da-116"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="2e2da-117">Представление, в котором будут открываться пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="2e2da-117">The view in which the user-defined function will open.</span></span> <span data-ttu-id="2e2da-118">Выберите <strong>таблицы</strong>, <strong>разработки</strong>, <strong>Режим предварительного просмотра</strong>, <strong>сводной таблицы</strong>или <strong>сводной диаграммы</strong> в поле <strong>View</strong> .</span><span class="sxs-lookup"><span data-stu-id="2e2da-118">Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="2e2da-119">Значение по умолчанию — <strong>таблицы данных</strong>.</span><span class="sxs-lookup"><span data-stu-id="2e2da-119">The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e2da-120"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="2e2da-120"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="2e2da-121">Режим ввода данных для пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="2e2da-121">The data entry mode for the user-defined function.</span></span> <span data-ttu-id="2e2da-122">Это относится только к пользовательских функций, открытых в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="2e2da-122">This applies only to user-defined functions opened in Datasheet view.</span></span> <span data-ttu-id="2e2da-123">Нажмите кнопку <strong>Add</strong> (пользователь может добавлять новые записи, но не могут просматривать и изменять существующие записи), <strong>Изменение</strong> (пользователь может просматривать или изменять существующие записи и добавление новых записей) или <strong>Только для чтения</strong> (пользователь может только просматривать записи).</span><span class="sxs-lookup"><span data-stu-id="2e2da-123">Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="2e2da-124">Значение по умолчанию — <strong>Изменить</strong>.</span><span class="sxs-lookup"><span data-stu-id="2e2da-124">The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2e2da-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="2e2da-125">Remarks</span></span>

<span data-ttu-id="2e2da-126">Это действие аналогично дважды щелкнув пользовательской функции в области навигации или щелкнув правой кнопкой мыши функцию на левой панели навигации и выбрав представления.</span><span class="sxs-lookup"><span data-stu-id="2e2da-126">This action is similar to double-clicking a user-defined function in the Navigation Pane, or right-clicking the function in the Navigation Pane and selecting a view.</span></span>

<span data-ttu-id="2e2da-127">Переключение в режим конструктора при открытом пользовательской функции удаляется значение аргумента **Режим данных** для пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="2e2da-127">Switching to Design view while the user-defined function is open removes the **Data Mode** argument setting for the user-defined function.</span></span> <span data-ttu-id="2e2da-128">Этот параметр не действует, даже в том случае, если пользователь возвращается в режим таблицы.</span><span class="sxs-lookup"><span data-stu-id="2e2da-128">This setting is not in effect, even if the user returns to Datasheet view.</span></span>

> [!TIP]
> - <span data-ttu-id="2e2da-129">Можно выбрать пользовательской функции в области навигации и перетащите его в строку действие в макросе.</span><span class="sxs-lookup"><span data-stu-id="2e2da-129">You can select a user-defined function in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="2e2da-130">Это автоматически создает **ОткрытьФункцию** действие, которое открывается пользовательских функций в представлении таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="2e2da-130">This automatically creates an **OpenFunction** action that opens the user-defined function in Datasheet view.</span></span>
> - <span data-ttu-id="2e2da-131">Если вы не хотите отобразить системные сообщения, которые появляются при выполнении функции, определенной пользователем (является пользовательской функции и показывают количество записей, которые будут затронуты), чтобы отключить отображение можно использовать действие **УстановитьСообщения** Эти сообщения.</span><span class="sxs-lookup"><span data-stu-id="2e2da-131">If you don't want to display the system messages that normally appear when a user-defined function is run (indicating it is a user-defined function and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="2e2da-132">Чтобы выполнить действие **ОткрытьФункцию** в Visual Basic для приложений (VBA) модуль, используйте метод **ОткрытьФункцию** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="2e2da-132">To run the **OpenFunction** action in a Visual Basic for Applications (VBA) module, use the **OpenFunction** method of the **DoCmd** object.</span></span>

