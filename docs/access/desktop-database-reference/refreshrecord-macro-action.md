---
title: Макрокоманда RefreshRecord
TOCTitle: RefreshRecord macro action
ms:assetid: 68c90d7d-f59c-9e83-bc30-8f37cf5a3696
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195261(v=office.15)
ms:contentKeyID: 48545396
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62122
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d8682c19686650ab193536658c6b56961f289174
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307086"
---
# <a name="refreshrecord-macro-action"></a><span data-ttu-id="d8d5a-102">Макрокоманда RefreshRecord</span><span class="sxs-lookup"><span data-stu-id="d8d5a-102">RefreshRecord macro action</span></span>


<span data-ttu-id="d8d5a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8d5a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d8d5a-104">С помощью действия **RefreshRecord** вы можете обновить источник записей для активной формы или таблицы, чтобы отразить изменения, внесенные в записи в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-104">You can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8d5a-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="d8d5a-105">Remarks</span></span>

<span data-ttu-id="d8d5a-106">Действие **RefreshRecord** отображает только изменения, внесенные в записи в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-106">the **RefreshRecord** action shows only changes made to records in the current set.</span></span> <span data-ttu-id="d8d5a-107">Так как действие **RefreshRecord** фактически не повторно затребовывало базу данных, текущий набор не будет включать в себя записи, которые были добавлены или исключены из нее с момента последнего повторного взвода базы данных; Также не будут исключены записи, которые больше не удовлетворяют условиям запроса или фильтра.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-107">Because the **RefreshRecord** action does not actually requery the database, the current set will not include records that have been added or exclude records that have been deleted since the database was last requeried; Nor will it exclude records that no longer satisfy the criteria of the query or filter.</span></span> <span data-ttu-id="d8d5a-108">Чтобы повторно запросить базу данных, используйте метод **[Requery](requery-macro-action.md)**.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-108">To requery the database, use the **[Requery](requery-macro-action.md)** method.</span></span> <span data-ttu-id="d8d5a-109">При повторном запросе источника записей текущий набор записей будет точно отражать все данные в источнике записей.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-109">When the record source for a form is requeried, the current set of records will accurately reflect all data in the record source.</span></span>

<span data-ttu-id="d8d5a-110">Поведение этого макроса зависит от того, вызывается ли оно в клиентской или веб-базе данных.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-110">The behavior of this macro action depends on whether you are calling it in a client database or a web database.</span></span>

## <a name="client-database"></a><span data-ttu-id="d8d5a-111">База данных клиента</span><span class="sxs-lookup"><span data-stu-id="d8d5a-111">Client database</span></span>

<span data-ttu-id="d8d5a-112">В клиентской базе данных можно использовать действие **RefreshRecord,** чтобы обновить исходный источник записей для активной формы или таблицы данных, чтобы отразить изменения, внесенные в данные в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-112">In a client database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the data in the current set.</span></span> <span data-ttu-id="d8d5a-113">Изменения включают изменения, внесенные текущим пользователем или другими пользователями в среде с несколькими пользователями.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-113">Changes include those made by the current user or by other users in a multiuser environment.</span></span> <span data-ttu-id="d8d5a-114">Эквивалентно методу **[Refresh.](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)**</span><span class="sxs-lookup"><span data-stu-id="d8d5a-114">It is equivalent to the **[Refresh](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)** method.</span></span>

<span data-ttu-id="d8d5a-115">**Макрокод RefreshRecord** в клиентской базе данных делает следующее:</span><span class="sxs-lookup"><span data-stu-id="d8d5a-115">The **RefreshRecord** macro action does the following in a client database:</span></span>

1.  <span data-ttu-id="d8d5a-116">Обновляет источник записей для активной формы или таблицы данных, чтобы отразить изменения, внесенные в строки в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-116">Updates the record source for the active form or datasheet to reflect the changes made to rows in the current set.</span></span> <span data-ttu-id="d8d5a-117">Для связанных таблиц ODBC извлекает изменения записей в текущем наборе из источника данных.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-117">For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="d8d5a-118">Обновляет текущий набор, чтобы отразить изменения.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-118">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="d8d5a-119">Если строка в источнике записей была удалена, она меняется на \# "Удалено".</span><span class="sxs-lookup"><span data-stu-id="d8d5a-119">If a row in the record source has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="d8d5a-120">Обновляет активную или таблицу данных для отображения всех измененных и удаленных записей \# в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-120">Refreshes the active or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="d8d5a-121">Повторно затребовывать все в подчиненные формы и в подрепорты в активной форме или таблице данных.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-121">Requeries any subforms and subreports on the active form or datasheet.</span></span>

## <a name="web-database"></a><span data-ttu-id="d8d5a-122">Веб-база данных</span><span class="sxs-lookup"><span data-stu-id="d8d5a-122">Web database</span></span>

<span data-ttu-id="d8d5a-123">В веб-базе данных можно использовать действие **RefreshRecord** для обновления источника баз данных для активной формы или таблицы данных в соответствии с изменениями, внесенными в записи в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-123">In a web database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span></span> <span data-ttu-id="d8d5a-124">Изменения включают изменения, внесенные текущим пользователем или другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-124">Changes include those made by the current user or other users.</span></span>

<span data-ttu-id="d8d5a-125">**Макрокод RefreshRecord** в веб-базе данных делает следующее:</span><span class="sxs-lookup"><span data-stu-id="d8d5a-125">The **RefreshRecord** macro action does the following in a web database:</span></span>

1.  <span data-ttu-id="d8d5a-126">Извлекает изменения с сервера для всех базовых таблиц в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-126">Retrieves changes from the server for any base tables in the current set.</span></span> <span data-ttu-id="d8d5a-127">Для связанных таблиц ODBC извлекает изменения записей в текущем наборе из источника данных.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-127">For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="d8d5a-128">Обновляет текущий набор, чтобы отразить изменения.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-128">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="d8d5a-129">Если строка в текущем наборе удалена, она меняется на \# "Удалено".</span><span class="sxs-lookup"><span data-stu-id="d8d5a-129">If a row in the current set has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="d8d5a-130">Обновляет активную форму или таблицу данных для отображения всех измененных и удаленных записей \# в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-130">Refreshes the active form or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="d8d5a-131">Повторно затребовывать все в подчиненные формы и в подрепорты в активной форме или таблице данных.</span><span class="sxs-lookup"><span data-stu-id="d8d5a-131">Requeries any subforms and subreports on the active form or datasheet.</span></span>

