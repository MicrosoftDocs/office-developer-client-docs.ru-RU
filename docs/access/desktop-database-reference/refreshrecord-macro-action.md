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
ms.openlocfilehash: 5e842ed4898f98f0d3c51955c3fb66010ef02853
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026199"
---
# <a name="refreshrecord-macro-action"></a><span data-ttu-id="5d1a9-102">Макрокоманда RefreshRecord</span><span class="sxs-lookup"><span data-stu-id="5d1a9-102">RefreshRecord macro action</span></span>


<span data-ttu-id="5d1a9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d1a9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d1a9-104">Действие **RefreshRecord** можно использовать для обновления базового источника данных для активной формы или таблицы для отражения изменений, внесенных в записи в текущий набор.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-104">You can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d1a9-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="5d1a9-105">Remarks</span></span>

<span data-ttu-id="5d1a9-106">Действие **RefreshRecord** показывает только изменения, внесенные в записи в текущий набор.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-106">the **RefreshRecord** action shows only changes made to records in the current set.</span></span> <span data-ttu-id="5d1a9-107">Поскольку действие **RefreshRecord** фактически не запрашивать базу, текущий набор не будет включать записи, которые были добавлены или исключения записей, которые были удалены с момента базы данных последнего опросить; И не будет исключать записям, которые больше не отвечают условию запроса или фильтра.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-107">Because the **RefreshRecord** action does not actually requery the database, the current set will not include records that have been added or exclude records that have been deleted since the database was last requeried; Nor will it exclude records that no longer satisfy the criteria of the query or filter.</span></span> <span data-ttu-id="5d1a9-108">Чтобы запросить базу данных, используйте метод **[повторный запрос](requery-macro-action.md)** .</span><span class="sxs-lookup"><span data-stu-id="5d1a9-108">To requery the database, use the **[Requery](requery-macro-action.md)** method.</span></span> <span data-ttu-id="5d1a9-109">Если обновляется источника записей для формы, текущего набора записей будет точно отражают все данные из источника данных.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-109">When the record source for a form is requeried, the current set of records will accurately reflect all data in the record source.</span></span>

<span data-ttu-id="5d1a9-110">Это действие макроса зависит ли вы вызываете его в базу данных клиента или веб-база данных.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-110">The behavior of this macro action depends on whether you are calling it in a client database or a web database.</span></span>

## <a name="client-database"></a><span data-ttu-id="5d1a9-111">База данных клиента</span><span class="sxs-lookup"><span data-stu-id="5d1a9-111">Client database</span></span>

<span data-ttu-id="5d1a9-112">В базе данных клиента можно использовать действие **RefreshRecord** обновление базового источника данных для активной формы или таблицы для отражения изменений, внесенных в данные в текущий набор.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-112">In a client database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the data in the current set.</span></span> <span data-ttu-id="5d1a9-113">Изменения включают указанные текущим пользователем или другими пользователями в многопользовательской среде.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-113">Changes include those made by the current user or by other users in a multiuser environment.</span></span> <span data-ttu-id="5d1a9-114">Это эквивалентно метод **[Refresh](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)** .</span><span class="sxs-lookup"><span data-stu-id="5d1a9-114">It is equivalent to the **[Refresh](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)** method.</span></span>

<span data-ttu-id="5d1a9-115">Действия макроса **RefreshRecord** производит следующие действия в базе данных клиента:</span><span class="sxs-lookup"><span data-stu-id="5d1a9-115">The **RefreshRecord** macro action does the following in a client database:</span></span>

1.  <span data-ttu-id="5d1a9-116">Обновляет источник записей для активной формы или таблицы для отражения изменений, внесенных в строки в текущий набор.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-116">Updates the record source for the active form or datasheet to reflect the changes made to rows in the current set.</span></span> <span data-ttu-id="5d1a9-117">Для ODBC связанные таблицы, извлекает изменения в записи в текущий набор из источника данных.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-117">For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="5d1a9-118">Обновляет текущий набор в соответствии с изменениями.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-118">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="5d1a9-119">Если была удалена строка в источнике записей, он изменяется для отображения \#удалено.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-119">If a row in the record source has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="5d1a9-120">Обновляет активный или таблицы для отображения какие-либо изменения записей и какие-либо \#удаленных записей в текущий набор.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-120">Refreshes the active or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="5d1a9-121">Вызывает повторный запрос все подчиненные формы и отчеты на активную форму или таблицы.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-121">Requeries any subforms and subreports on the active form or datasheet.</span></span>

## <a name="web-database"></a><span data-ttu-id="5d1a9-122">Веб-база данных</span><span class="sxs-lookup"><span data-stu-id="5d1a9-122">Web database</span></span>

<span data-ttu-id="5d1a9-123">В веб-база данных можно использовать действие **RefreshRecord** обновление базового источника данных для активной формы или таблицы для отражения изменений, внесенных в записи в текущий набор.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-123">In a web database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span></span> <span data-ttu-id="5d1a9-124">Изменения включают сделанные текущего пользователя и других пользователей.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-124">Changes include those made by the current user or other users.</span></span>

<span data-ttu-id="5d1a9-125">Действия макроса **RefreshRecord** выполняет следующие действия в веб-база данных:</span><span class="sxs-lookup"><span data-stu-id="5d1a9-125">The **RefreshRecord** macro action does the following in a web database:</span></span>

1.  <span data-ttu-id="5d1a9-126">Извлекает изменяется с сервера для любого базовые таблицы в текущий набор.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-126">Retrieves changes from the server for any base tables in the current set.</span></span> <span data-ttu-id="5d1a9-127">Для ODBC связанные таблицы, извлекает изменения в записи в текущий набор из источника данных.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-127">For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="5d1a9-128">Обновляет текущий набор в соответствии с изменениями.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-128">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="5d1a9-129">Если строка в текущий набор был удален, он изменяется для отображения \#удалено.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-129">If a row in the current set has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="5d1a9-130">Обновляет активной формы или таблицы для отображения какие-либо изменения записей и какие-либо \#удаленных записей в текущий набор.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-130">Refreshes the active form or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="5d1a9-131">Вызывает повторный запрос все подчиненные формы и отчеты на активную форму или таблицы.</span><span class="sxs-lookup"><span data-stu-id="5d1a9-131">Requeries any subforms and subreports on the active form or datasheet.</span></span>

