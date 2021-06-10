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
# <a name="refreshrecord-macro-action"></a><span data-ttu-id="1c296-102">Макрокоманда RefreshRecord</span><span class="sxs-lookup"><span data-stu-id="1c296-102">RefreshRecord macro action</span></span>


<span data-ttu-id="1c296-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c296-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1c296-104">Вы можете использовать **действие RefreshRecord** для обновления источника записей для активной формы или таблицы данных для отражения изменений, внесенных в записи текущего набора.</span><span class="sxs-lookup"><span data-stu-id="1c296-104">You can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c296-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="1c296-105">Remarks</span></span>

<span data-ttu-id="1c296-106">в **действии RefreshRecord** показаны только изменения, внесенные в записи текущего набора.</span><span class="sxs-lookup"><span data-stu-id="1c296-106">the **RefreshRecord** action shows only changes made to records in the current set.</span></span> <span data-ttu-id="1c296-107">Так как действие **RefreshRecord** фактически не переописывало базу данных, текущий набор не будет включать записи, которые были добавлены или исключены записи, которые были удалены с момента последней повторной записи базы данных; Кроме того, не будут исключены записи, которые больше не соответствуют критериям запроса или фильтра.</span><span class="sxs-lookup"><span data-stu-id="1c296-107">Because the **RefreshRecord** action does not actually requery the database, the current set will not include records that have been added or exclude records that have been deleted since the database was last requeried; Nor will it exclude records that no longer satisfy the criteria of the query or filter.</span></span> <span data-ttu-id="1c296-108">Чтобы повторно запросить базу данных, используйте метод **[Requery](requery-macro-action.md)**.</span><span class="sxs-lookup"><span data-stu-id="1c296-108">To requery the database, use the **[Requery](requery-macro-action.md)** method.</span></span> <span data-ttu-id="1c296-109">При повторном запросе источника записей текущий набор записей будет точно отражать все данные в источнике записей.</span><span class="sxs-lookup"><span data-stu-id="1c296-109">When the record source for a form is requeried, the current set of records will accurately reflect all data in the record source.</span></span>

<span data-ttu-id="1c296-110">Поведение этого макроса зависит от того, вызываете ли вы его в клиентской базе данных или в веб-базе данных.</span><span class="sxs-lookup"><span data-stu-id="1c296-110">The behavior of this macro action depends on whether you are calling it in a client database or a web database.</span></span>

## <a name="client-database"></a><span data-ttu-id="1c296-111">Клиентская база данных</span><span class="sxs-lookup"><span data-stu-id="1c296-111">Client database</span></span>

<span data-ttu-id="1c296-112">В клиентской базе данных можно использовать действие **RefreshRecord** для обновления источника записи для активной формы или таблицы данных, чтобы отразить изменения, внесенные в данные текущего набора.</span><span class="sxs-lookup"><span data-stu-id="1c296-112">In a client database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the data in the current set.</span></span> <span data-ttu-id="1c296-113">Изменения включают изменения, внесенные текущим пользователем или другими пользователями в многоуровневой среде.</span><span class="sxs-lookup"><span data-stu-id="1c296-113">Changes include those made by the current user or by other users in a multiuser environment.</span></span> <span data-ttu-id="1c296-114">Это эквивалентно методу **[Обновления.](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)**</span><span class="sxs-lookup"><span data-stu-id="1c296-114">It is equivalent to the **[Refresh](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)** method.</span></span>

<span data-ttu-id="1c296-115">**Макро-действие RefreshRecord** содержит следующие действия в клиентской базе данных:</span><span class="sxs-lookup"><span data-stu-id="1c296-115">The **RefreshRecord** macro action does the following in a client database:</span></span>

1.  <span data-ttu-id="1c296-116">Обновляет источник записей для активной формы или таблицы данных, чтобы отразить изменения, внесенные в строки в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="1c296-116">Updates the record source for the active form or datasheet to reflect the changes made to rows in the current set.</span></span> <span data-ttu-id="1c296-117">Для связанных таблиц ODBC извлекает изменения в записи текущего набора из источника данных.</span><span class="sxs-lookup"><span data-stu-id="1c296-117">For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="1c296-118">Обновляет текущий набор, чтобы отразить изменения.</span><span class="sxs-lookup"><span data-stu-id="1c296-118">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="1c296-119">Если строка в источнике записи удалена, она меняется, чтобы показать \# Удаленный.</span><span class="sxs-lookup"><span data-stu-id="1c296-119">If a row in the record source has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="1c296-120">Обновляет активную или таблицу данных для отображения всех измененных записей и удаленных записей \# в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="1c296-120">Refreshes the active or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="1c296-121">Requeries any subforms and subreports on the active form or datasheet.</span><span class="sxs-lookup"><span data-stu-id="1c296-121">Requeries any subforms and subreports on the active form or datasheet.</span></span>

## <a name="web-database"></a><span data-ttu-id="1c296-122">Веб-база данных</span><span class="sxs-lookup"><span data-stu-id="1c296-122">Web database</span></span>

<span data-ttu-id="1c296-123">В веб-базе данных можно использовать действие **RefreshRecord** для обновления источника записей для активной формы или таблицы данных для отражения изменений, внесенных в записи текущего набора.</span><span class="sxs-lookup"><span data-stu-id="1c296-123">In a web database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span></span> <span data-ttu-id="1c296-124">Изменения включают изменения, внесенные текущим пользователем или другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="1c296-124">Changes include those made by the current user or other users.</span></span>

<span data-ttu-id="1c296-125">**Макро-действие RefreshRecord** содержит следующие действия в веб-базе данных:</span><span class="sxs-lookup"><span data-stu-id="1c296-125">The **RefreshRecord** macro action does the following in a web database:</span></span>

1.  <span data-ttu-id="1c296-126">Извлекает изменения с сервера для любых базовых таблиц в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="1c296-126">Retrieves changes from the server for any base tables in the current set.</span></span> <span data-ttu-id="1c296-127">Для связанных таблиц ODBC извлекает изменения в записи текущего набора из источника данных.</span><span class="sxs-lookup"><span data-stu-id="1c296-127">For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="1c296-128">Обновляет текущий набор, чтобы отразить изменения.</span><span class="sxs-lookup"><span data-stu-id="1c296-128">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="1c296-129">Если строка в текущем наборе удалена, она меняется, чтобы показать \# Удаленный.</span><span class="sxs-lookup"><span data-stu-id="1c296-129">If a row in the current set has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="1c296-130">Обновляет активную форму или таблицу данных для отображения всех измененных записей и удаленных записей \# в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="1c296-130">Refreshes the active form or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="1c296-131">Requeries any subforms and subreports on the active form or datasheet.</span><span class="sxs-lookup"><span data-stu-id="1c296-131">Requeries any subforms and subreports on the active form or datasheet.</span></span>

