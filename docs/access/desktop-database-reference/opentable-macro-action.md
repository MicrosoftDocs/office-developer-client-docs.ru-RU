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
# <a name="opentable-macro-action"></a><span data-ttu-id="1b6e6-102">Макрокоманда OpenTable</span><span class="sxs-lookup"><span data-stu-id="1b6e6-102">OpenTable macro action</span></span>

<span data-ttu-id="1b6e6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b6e6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1b6e6-104">Вы можете использовать действие **опентабле** для открытия таблицы в режиме таблицы, конструктора или предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="1b6e6-104">You can use the **OpenTable** action to open a table in Datasheet view, Design view, or Print Preview.</span></span> <span data-ttu-id="1b6e6-105">Вы также можете выбрать режим ввода данных для таблицы.</span><span class="sxs-lookup"><span data-stu-id="1b6e6-105">You can also select a data entry mode for the table.</span></span>

## <a name="setting"></a><span data-ttu-id="1b6e6-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="1b6e6-106">Setting</span></span>

<span data-ttu-id="1b6e6-107">Макрокоманда **опентабле** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="1b6e6-107">The **OpenTable** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1b6e6-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="1b6e6-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="1b6e6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1b6e6-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b6e6-110"><strong>Имя таблицы</strong></span><span class="sxs-lookup"><span data-stu-id="1b6e6-110"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="1b6e6-111">Имя открываемой таблицы.</span><span class="sxs-lookup"><span data-stu-id="1b6e6-111">The name of the table to open.</span></span> <span data-ttu-id="1b6e6-112">В поле <strong>имя таблицы</strong> в разделе <strong>аргументы макрокоманды</strong> области построителя макросов отображаются все таблицы текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="1b6e6-112">The <strong>Table Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all tables in the current database.</span></span> <span data-ttu-id="1b6e6-113">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="1b6e6-113">This is a required argument.</span></span> <span data-ttu-id="1b6e6-114">При запуске макроса, содержащего действие <strong>опентабле</strong> , в библиотечной базе данных Microsoft Access сначала ищет таблицу с этим именем в библиотечной базе данных, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="1b6e6-114">If you run a macro containing the <strong>OpenTable</strong> action in a library database, Microsoft Microsoft Access looks for the table with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b6e6-115"><strong>Просмотр</strong></span><span class="sxs-lookup"><span data-stu-id="1b6e6-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="1b6e6-116">Представление, в котором будет открыта таблица.</span><span class="sxs-lookup"><span data-stu-id="1b6e6-116">The view in which the table will open.</span></span> <span data-ttu-id="1b6e6-117">В поле <strong>вид</strong> щелкните <strong>Таблица</strong>, <strong>Макет</strong>, <strong>Предварительный просмотр</strong>, <strong>Сводная таблица</strong>или <strong>Сводная диаграмма</strong> .</span><span class="sxs-lookup"><span data-stu-id="1b6e6-117">Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="1b6e6-118">Значение по умолчанию — <strong>Таблица</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b6e6-118">The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b6e6-119"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="1b6e6-119"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="1b6e6-120">Режим ввода данных для таблицы.</span><span class="sxs-lookup"><span data-stu-id="1b6e6-120">The data entry mode for the table.</span></span> <span data-ttu-id="1b6e6-121">Это применимо только к таблицам, открываемым в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="1b6e6-121">This applies only to tables opened in Datasheet view.</span></span> <span data-ttu-id="1b6e6-122">Нажмите кнопку <strong>Добавить</strong> (пользователь может добавлять новые записи, но не может изменять существующие), <strong>изменять</strong> (пользователь может изменять существующие записи и добавлять новые записи) или <strong>только для чтения</strong> (пользователи могут только просматривать записи).</span><span class="sxs-lookup"><span data-stu-id="1b6e6-122">Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="1b6e6-123">Значение по умолчанию — <strong>Edit</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b6e6-123">The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="1b6e6-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="1b6e6-124">Remarks</span></span>

<span data-ttu-id="1b6e6-125">Это действие аналогично двойному щелчку таблицы в области навигации или щелчке правой кнопкой мыши таблицы в области навигации и выбора представления.</span><span class="sxs-lookup"><span data-stu-id="1b6e6-125">This action is similar to double-clicking the table in the Navigation Pane, or right-clicking the table in the Navigation Pane and selecting a view.</span></span>

> [!TIP]
> <span data-ttu-id="1b6e6-126">Вы можете перетащить таблицу из области навигации в строку макрокоманды.</span><span class="sxs-lookup"><span data-stu-id="1b6e6-126">You can drag a table from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="1b6e6-127">При этом автоматически создается действие **опентабле** , которое открывает таблицу в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="1b6e6-127">This automatically creates an **OpenTable** action that opens the table in Datasheet view.</span></span>

<span data-ttu-id="1b6e6-128">Чтобы запустить действие **опентабле** в модуле Visual Basic для приложений (VBA), используйте метод **опентабле** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="1b6e6-128">To run the **OpenTable** action in a Visual Basic for Applications (VBA) module, use the **OpenTable** method of the **DoCmd** object.</span></span>

