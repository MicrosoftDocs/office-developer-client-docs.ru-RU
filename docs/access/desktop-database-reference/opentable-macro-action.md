---
title: Макрокоманда OpenTable
TOCTitle: OpenTable macro action
ms:assetid: 4220ad3a-d064-0034-2806-ec1a447cebac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192909(v=office.15)
ms:contentKeyID: 48544469
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm149011
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 48a3797c2008f261eda8acc3391b39561fec05f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288296"
---
# <a name="opentable-macro-action"></a><span data-ttu-id="6341f-102">Макрокоманда OpenTable</span><span class="sxs-lookup"><span data-stu-id="6341f-102">OpenTable macro action</span></span>

<span data-ttu-id="6341f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6341f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6341f-104">Вы можете использовать **действие OpenTable** для открытия таблицы в представлении таблицы Datasheet, представлении "Дизайн" или "Предварительный просмотр печати".</span><span class="sxs-lookup"><span data-stu-id="6341f-104">You can use the **OpenTable** action to open a table in Datasheet view, Design view, or Print Preview.</span></span> <span data-ttu-id="6341f-105">Вы также можете выбрать режим ввода данных для таблицы.</span><span class="sxs-lookup"><span data-stu-id="6341f-105">You can also select a data entry mode for the table.</span></span>

## <a name="setting"></a><span data-ttu-id="6341f-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="6341f-106">Setting</span></span>

<span data-ttu-id="6341f-107">Действие **OpenTable** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="6341f-107">The **OpenTable** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6341f-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="6341f-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6341f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6341f-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6341f-110"><strong>Имя таблицы</strong></span><span class="sxs-lookup"><span data-stu-id="6341f-110"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="6341f-111">Имя открытой таблицы.</span><span class="sxs-lookup"><span data-stu-id="6341f-111">The name of the table to open.</span></span> <span data-ttu-id="6341f-112">Поле <strong>Имя таблицы</strong> в разделе <strong>Аргументы</strong> действий в области Macro Builder отображает все таблицы в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="6341f-112">The <strong>Table Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all tables in the current database.</span></span> <span data-ttu-id="6341f-113">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="6341f-113">This is a required argument.</span></span> <span data-ttu-id="6341f-114">Если вы запустите макрос, содержащий действие <strong>OpenTable</strong> в базе данных библиотеки, Microsoft Microsoft Access сначала ищет таблицу с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="6341f-114">If you run a macro containing the <strong>OpenTable</strong> action in a library database, Microsoft Microsoft Access looks for the table with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6341f-115"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="6341f-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="6341f-116">Представление, в котором откроется таблица.</span><span class="sxs-lookup"><span data-stu-id="6341f-116">The view in which the table will open.</span></span> <span data-ttu-id="6341f-117">Щелкните <strong>таблицу</strong>данных, <strong>дизайн,</strong> <strong>предварительный</strong>просмотр печати, <strong>pivotTable</strong>или сводная диаграмма в <strong>поле Просмотр.</strong> <strong></strong></span><span class="sxs-lookup"><span data-stu-id="6341f-117">Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="6341f-118">По умолчанию — <strong>таблица данных.</strong></span><span class="sxs-lookup"><span data-stu-id="6341f-118">The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6341f-119"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="6341f-119"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="6341f-120">Режим ввода данных для таблицы.</span><span class="sxs-lookup"><span data-stu-id="6341f-120">The data entry mode for the table.</span></span> <span data-ttu-id="6341f-121">Это касается только таблиц, открытых в представлении Datasheet.</span><span class="sxs-lookup"><span data-stu-id="6341f-121">This applies only to tables opened in Datasheet view.</span></span> <span data-ttu-id="6341f-122">Щелкните <strong>Добавить</strong> (пользователь может добавлять новые записи, но не может изменять существующие записи), <strong></strong> изменить (пользователь может изменять существующие записи и добавлять новые записи) или <strong>Только</strong> для чтения (пользователь может просматривать только записи).</span><span class="sxs-lookup"><span data-stu-id="6341f-122">Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="6341f-123">По умолчанию <strong>изменить</strong>.</span><span class="sxs-lookup"><span data-stu-id="6341f-123">The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="6341f-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="6341f-124">Remarks</span></span>

<span data-ttu-id="6341f-125">Это действие аналогично дважды щелкнув таблицу в области навигации или щелкнув правой кнопкой мыши таблицу в области навигации и выбрав представление.</span><span class="sxs-lookup"><span data-stu-id="6341f-125">This action is similar to double-clicking the table in the Navigation Pane, or right-clicking the table in the Navigation Pane and selecting a view.</span></span>

> [!TIP]
> <span data-ttu-id="6341f-126">Таблицу можно перетаскивать из области навигации в строку действий макроса.</span><span class="sxs-lookup"><span data-stu-id="6341f-126">You can drag a table from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="6341f-127">Это автоматически создает действие **OpenTable,** которое открывает таблицу в представлении Datasheet.</span><span class="sxs-lookup"><span data-stu-id="6341f-127">This automatically creates an **OpenTable** action that opens the table in Datasheet view.</span></span>

<span data-ttu-id="6341f-128">Для запуска **действия OpenTable** в Visual Basic для приложений (VBA) используйте метод **OpenTable** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="6341f-128">To run the **OpenTable** action in a Visual Basic for Applications (VBA) module, use the **OpenTable** method of the **DoCmd** object.</span></span>

