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
ms.openlocfilehash: d80065c976a014ccf379bdc2016b0324cb02b269
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998149"
---
# <a name="opentable-macro-action"></a><span data-ttu-id="a1c0a-102">Макрокоманда OpenTable</span><span class="sxs-lookup"><span data-stu-id="a1c0a-102">OpenTable macro action</span></span>

<span data-ttu-id="a1c0a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1c0a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1c0a-104">Чтобы открыть таблицу в режиме таблицы, конструктора или просмотра можно использовать **ОткрытьТаблицу** .</span><span class="sxs-lookup"><span data-stu-id="a1c0a-104">You can use the **OpenTable** action to open a table in Datasheet view, Design view, or Print Preview.</span></span> <span data-ttu-id="a1c0a-105">Также можно выбрать режим ввода данных для таблицы.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-105">You can also select a data entry mode for the table.</span></span>

## <a name="setting"></a><span data-ttu-id="a1c0a-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="a1c0a-106">Setting</span></span>

<span data-ttu-id="a1c0a-107">**ОткрытьТаблицу** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-107">The **OpenTable** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1c0a-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="a1c0a-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a1c0a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a1c0a-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1c0a-110"><strong>Имя таблицы</strong></span><span class="sxs-lookup"><span data-stu-id="a1c0a-110"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="a1c0a-111">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-111">The name of the table to open.</span></span> <span data-ttu-id="a1c0a-112">В поле <strong>Имя таблицы</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов содержит все таблицы в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-112">The <strong>Table Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all tables in the current database.</span></span> <span data-ttu-id="a1c0a-113">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-113">This is a required argument.</span></span> <span data-ttu-id="a1c0a-114">Если макрос, содержащий <strong>ОткрытьТаблицу в базе данных библиотеки</strong> , Microsoft Microsoft Access выполняет поиск таблицы с указанным именем сначала в библиотеке базы данных, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-114">If you run a macro containing the <strong>OpenTable</strong> action in a library database, Microsoft Microsoft Access looks for the table with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1c0a-115"><strong>Просмотр</strong></span><span class="sxs-lookup"><span data-stu-id="a1c0a-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="a1c0a-116">Представление, в котором будут открываться в таблице.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-116">The view in which the table will open.</span></span> <span data-ttu-id="a1c0a-117">Выберите <strong>таблицы</strong>, <strong>разработки</strong>, <strong>Режим предварительного просмотра</strong>, <strong>сводной таблицы</strong>или <strong>сводной диаграммы</strong> в поле <strong>View</strong> .</span><span class="sxs-lookup"><span data-stu-id="a1c0a-117">Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="a1c0a-118">Значение по умолчанию — <strong>таблицы данных</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-118">The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1c0a-119"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="a1c0a-119"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="a1c0a-120">Режим ввода данных для таблицы.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-120">The data entry mode for the table.</span></span> <span data-ttu-id="a1c0a-121">Это относится только к таблиц, открытых в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-121">This applies only to tables opened in Datasheet view.</span></span> <span data-ttu-id="a1c0a-122">Нажмите кнопку <strong>Add</strong> (пользователь может добавлять новые записи, но не могут изменять существующие записи), <strong>Изменение</strong> (пользователь может изменять существующие записи и добавление новых записей), или <strong>Только для чтения</strong> (пользователь может только просматривать записи).</span><span class="sxs-lookup"><span data-stu-id="a1c0a-122">Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="a1c0a-123">Значение по умолчанию — <strong>Изменить</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-123">The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="a1c0a-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="a1c0a-124">Remarks</span></span>

<span data-ttu-id="a1c0a-125">Это действие аналогична таблице на левой панели навигации, дважды щелкнув или щелкнув правой кнопкой мыши таблицу в области навигации и выбрав представления.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-125">This action is similar to double-clicking the table in the Navigation Pane, or right-clicking the table in the Navigation Pane and selecting a view.</span></span>

> [!TIP]
> <span data-ttu-id="a1c0a-126">Таблица можно перетаскивать из области переходов в строку действие в макросе.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-126">You can drag a table from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="a1c0a-127">Это автоматически создает **ОткрытьТаблицу** действие, которое открывается таблицы в представлении таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-127">This automatically creates an **OpenTable** action that opens the table in Datasheet view.</span></span>

<span data-ttu-id="a1c0a-128">Чтобы запустить **ОткрытьТаблицу** в Visual Basic для приложений (VBA) модуль, используйте метод **ОткрытьТаблицу** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="a1c0a-128">To run the **OpenTable** action in a Visual Basic for Applications (VBA) module, use the **OpenTable** method of the **DoCmd** object.</span></span>

