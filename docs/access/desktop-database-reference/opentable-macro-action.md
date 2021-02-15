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
# <a name="opentable-macro-action"></a><span data-ttu-id="bf53a-102">Макрокоманда OpenTable</span><span class="sxs-lookup"><span data-stu-id="bf53a-102">OpenTable macro action</span></span>

<span data-ttu-id="bf53a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf53a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bf53a-104">Действие **OpenTable** можно использовать для открытия таблицы в представлении таблицы, представлении конструктора или предварительном просмотре печати.</span><span class="sxs-lookup"><span data-stu-id="bf53a-104">You can use the **OpenTable** action to open a table in Datasheet view, Design view, or Print Preview.</span></span> <span data-ttu-id="bf53a-105">Можно также выбрать режим ввода данных для таблицы.</span><span class="sxs-lookup"><span data-stu-id="bf53a-105">You can also select a data entry mode for the table.</span></span>

## <a name="setting"></a><span data-ttu-id="bf53a-106">Setting</span><span class="sxs-lookup"><span data-stu-id="bf53a-106">Setting</span></span>

<span data-ttu-id="bf53a-107">Действие **OpenTable** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="bf53a-107">The **OpenTable** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf53a-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="bf53a-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="bf53a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="bf53a-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf53a-110"><strong>Имя таблицы</strong></span><span class="sxs-lookup"><span data-stu-id="bf53a-110"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="bf53a-111">Имя открытой таблицы.</span><span class="sxs-lookup"><span data-stu-id="bf53a-111">The name of the table to open.</span></span> <span data-ttu-id="bf53a-112">В <strong>поле "Имя таблицы"</strong> в разделе <strong>"Аргументы</strong> действий" области построитель макроса показаны все таблицы в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="bf53a-112">The <strong>Table Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all tables in the current database.</span></span> <span data-ttu-id="bf53a-113">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="bf53a-113">This is a required argument.</span></span> <span data-ttu-id="bf53a-114">При запуске макроса, содержащего действие <strong>OpenTable</strong> в базе данных библиотеки, Microsoft Access сначала ищет таблицу с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="bf53a-114">If you run a macro containing the <strong>OpenTable</strong> action in a library database, Microsoft Microsoft Access looks for the table with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf53a-115"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="bf53a-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="bf53a-116">Представление, в котором откроется таблица.</span><span class="sxs-lookup"><span data-stu-id="bf53a-116">The view in which the table will open.</span></span> <span data-ttu-id="bf53a-117">Щелкните <strong></strong> <strong>"Таблица</strong> <strong>данных", "Конструктор",</strong>"Предварительный <strong>просмотр",</strong> <strong>"Сводная диаграмма</strong> в поле <strong>"Вид".</strong></span><span class="sxs-lookup"><span data-stu-id="bf53a-117">Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="bf53a-118">Значение по умолчанию <strong>— Таблица.</strong></span><span class="sxs-lookup"><span data-stu-id="bf53a-118">The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf53a-119"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="bf53a-119"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="bf53a-120">Режим ввода данных для таблицы.</span><span class="sxs-lookup"><span data-stu-id="bf53a-120">The data entry mode for the table.</span></span> <span data-ttu-id="bf53a-121">Это относится только к таблицам, открытым в представлении таблиц.</span><span class="sxs-lookup"><span data-stu-id="bf53a-121">This applies only to tables opened in Datasheet view.</span></span> <span data-ttu-id="bf53a-122">Нажмите <strong></strong> кнопку "Добавить" (пользователь может добавлять новые записи, но не может редактировать существующие <strong>записи),</strong> изменить (пользователь может редактировать существующие записи и добавлять новые) или "Только чтение" <strong>(пользователь</strong> может просматривать только записи).</span><span class="sxs-lookup"><span data-stu-id="bf53a-122">Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="bf53a-123">Значение по умолчанию — <strong>Edit</strong>.</span><span class="sxs-lookup"><span data-stu-id="bf53a-123">The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="bf53a-124">Заметки</span><span class="sxs-lookup"><span data-stu-id="bf53a-124">Remarks</span></span>

<span data-ttu-id="bf53a-125">Это действие аналогично двойному щелчку таблицы в области навигации или щелчку правой кнопкой мыши таблицы в области навигации и выбору представления.</span><span class="sxs-lookup"><span data-stu-id="bf53a-125">This action is similar to double-clicking the table in the Navigation Pane, or right-clicking the table in the Navigation Pane and selecting a view.</span></span>

> [!TIP]
> <span data-ttu-id="bf53a-126">Можно перетащить таблицу из области навигации в строку макроса.</span><span class="sxs-lookup"><span data-stu-id="bf53a-126">You can drag a table from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="bf53a-127">При этом автоматически создается действие **OpenTable,** которое открывает таблицу в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="bf53a-127">This automatically creates an **OpenTable** action that opens the table in Datasheet view.</span></span>

<span data-ttu-id="bf53a-128">Чтобы запустить действие **OpenTable** в модуле Visual Basic для приложений (VBA), используйте метод **OpenTable** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="bf53a-128">To run the **OpenTable** action in a Visual Basic for Applications (VBA) module, use the **OpenTable** method of the **DoCmd** object.</span></span>

