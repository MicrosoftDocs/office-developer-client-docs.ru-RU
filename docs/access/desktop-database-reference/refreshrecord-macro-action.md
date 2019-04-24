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
# <a name="refreshrecord-macro-action"></a><span data-ttu-id="d5ee6-102">Макрокоманда RefreshRecord</span><span class="sxs-lookup"><span data-stu-id="d5ee6-102">RefreshRecord macro action</span></span>


<span data-ttu-id="d5ee6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d5ee6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d5ee6-104">Вы можете использовать действие **рефрешрекорд** , чтобы обновить базовый источник записей для активной формы или таблицы, чтобы отразить изменения, внесенные в записи в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-104">You can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5ee6-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="d5ee6-105">Remarks</span></span>

<span data-ttu-id="d5ee6-106">в действии **рефрешрекорд** отображаются только изменения, внесенные в записи в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-106">the **RefreshRecord** action shows only changes made to records in the current set.</span></span> <span data-ttu-id="d5ee6-107">Так как действие **рефрешрекорд** фактически не отправляет запрос в базу данных, текущий набор не включает записи, которые были удалены с момента последнего повторного запроса базы данных; Кроме того, он не будет исключать записи, которые больше не удовлетворяют критериям запроса или фильтра.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-107">Because the **RefreshRecord** action does not actually requery the database, the current set will not include records that have been added or exclude records that have been deleted since the database was last requeried; Nor will it exclude records that no longer satisfy the criteria of the query or filter.</span></span> <span data-ttu-id="d5ee6-108">Чтобы повторно запросить базу данных, используйте метод **[Requery](requery-macro-action.md)**.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-108">To requery the database, use the **[Requery](requery-macro-action.md)** method.</span></span> <span data-ttu-id="d5ee6-109">При повторном запросе источника записей текущий набор записей будет точно отражать все данные в источнике записей.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-109">When the record source for a form is requeried, the current set of records will accurately reflect all data in the record source.</span></span>

<span data-ttu-id="d5ee6-110">Поведение этого макроса зависит от того, вызывается ли он в клиентской базе данных или в веб-базе данных.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-110">The behavior of this macro action depends on whether you are calling it in a client database or a web database.</span></span>

## <a name="client-database"></a><span data-ttu-id="d5ee6-111">Клиентская база данных</span><span class="sxs-lookup"><span data-stu-id="d5ee6-111">Client database</span></span>

<span data-ttu-id="d5ee6-112">В клиентской базе данных можно использовать действие **рефрешрекорд** для обновления базового источника записей для активной формы или таблицы, чтобы отразить изменения данных в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-112">In a client database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the data in the current set.</span></span> <span data-ttu-id="d5ee6-113">Изменения включают изменения, внесенные текущим пользователем или другими пользователями в многопользовательской среде.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-113">Changes include those made by the current user or by other users in a multiuser environment.</span></span> <span data-ttu-id="d5ee6-114">Эквивалентен методу **[Refresh](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)** .</span><span class="sxs-lookup"><span data-stu-id="d5ee6-114">It is equivalent to the **[Refresh](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)** method.</span></span>

<span data-ttu-id="d5ee6-115">Макрокоманда **рефрешрекорд** выполняет следующие действия в клиентской базе данных:</span><span class="sxs-lookup"><span data-stu-id="d5ee6-115">The **RefreshRecord** macro action does the following in a client database:</span></span>

1.  <span data-ttu-id="d5ee6-116">Обновляет источник записи для активной формы или таблицы в соответствии с изменениями, внесенными в строки в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-116">Updates the record source for the active form or datasheet to reflect the changes made to rows in the current set.</span></span> <span data-ttu-id="d5ee6-117">Для связанных таблиц ODBC получает изменения записей в текущем наборе из источника данных.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-117">For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="d5ee6-118">Обновляет текущий набор, чтобы отразить изменения.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-118">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="d5ee6-119">Если строка в источнике записей была удалена, она будет изменена на Показать \#удалено.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-119">If a row in the record source has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="d5ee6-120">Обновление активной или текущей таблицы для отображения измененных записей и всех \#удаленных записей в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-120">Refreshes the active or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="d5ee6-121">Повторно запрашивает все подчиненные формы и подчиненные отчеты в активной форме или таблице.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-121">Requeries any subforms and subreports on the active form or datasheet.</span></span>

## <a name="web-database"></a><span data-ttu-id="d5ee6-122">Веб-база данных</span><span class="sxs-lookup"><span data-stu-id="d5ee6-122">Web database</span></span>

<span data-ttu-id="d5ee6-123">В веб-базе данных вы можете использовать действие **рефрешрекорд** , чтобы обновить базовый источник записей для активной формы или таблицы, чтобы отразить изменения, внесенные в записи в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-123">In a web database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span></span> <span data-ttu-id="d5ee6-124">Изменения включают изменения, внесенные текущим пользователем или другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-124">Changes include those made by the current user or other users.</span></span>

<span data-ttu-id="d5ee6-125">Макрокоманда **рефрешрекорд** выполняет следующие действия в веб-базе данных:</span><span class="sxs-lookup"><span data-stu-id="d5ee6-125">The **RefreshRecord** macro action does the following in a web database:</span></span>

1.  <span data-ttu-id="d5ee6-126">Извлекает изменения с сервера для всех базовых таблиц в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-126">Retrieves changes from the server for any base tables in the current set.</span></span> <span data-ttu-id="d5ee6-127">Для связанных таблиц ODBC получает изменения записей в текущем наборе из источника данных.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-127">For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="d5ee6-128">Обновляет текущий набор, чтобы отразить изменения.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-128">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="d5ee6-129">Если строка в текущем наборе была удалена, она будет изменена на Показать \#удалено.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-129">If a row in the current set has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="d5ee6-130">Обновление активной формы или таблицы для отображения измененных записей и всех \#удаленных записей в текущем наборе.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-130">Refreshes the active form or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="d5ee6-131">Повторно запрашивает все подчиненные формы и подчиненные отчеты в активной форме или таблице.</span><span class="sxs-lookup"><span data-stu-id="d5ee6-131">Requeries any subforms and subreports on the active form or datasheet.</span></span>

