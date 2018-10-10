---
title: RefreshRecord Macro Action
TOCTitle: RefreshRecord Macro Action
ms:assetid: 68c90d7d-f59c-9e83-bc30-8f37cf5a3696
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195261(v=office.15)
ms:contentKeyID: 48545396
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62122
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 91c49ca4d453418a02d55163a023e853fadd5773
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481247"
---
# <a name="refreshrecord-macro-action"></a><span data-ttu-id="8fbd6-102">RefreshRecord Macro Action</span><span class="sxs-lookup"><span data-stu-id="8fbd6-102">RefreshRecord Macro Action</span></span>


<span data-ttu-id="8fbd6-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8fbd6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8fbd6-104">Действие **RefreshRecord** можно использовать для обновления базового источника данных для активной формы или таблицы для отражения изменений, внесенных в записи в текущий набор.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-104">You can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fbd6-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="8fbd6-105">Remarks</span></span>

<span data-ttu-id="8fbd6-106">Действие **RefreshRecord** показывает только изменения, внесенные в записи в текущий набор.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-106">the **RefreshRecord** action shows only changes made to records in the current set.</span></span> <span data-ttu-id="8fbd6-107">Поскольку действие **RefreshRecord** фактически не запрашивать базу, текущий набор не будет включать записи, которые были добавлены или исключения записей, которые были удалены с момента базы данных последнего опросить; И не будет исключать записям, которые больше не отвечают условию запроса или фильтра.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-107">Because the **RefreshRecord** action does not actually requery the database, the current set will not include records that have been added or exclude records that have been deleted since the database was last requeried; Nor will it exclude records that no longer satisfy the criteria of the query or filter.</span></span> <span data-ttu-id="8fbd6-108">Чтобы запросить базу данных, используйте метод **[повторный запрос](requery-macro-action.md)** .</span><span class="sxs-lookup"><span data-stu-id="8fbd6-108">To requery the database, use the **[Requery](requery-macro-action.md)** method.</span></span> <span data-ttu-id="8fbd6-109">Если обновляется источника записей для формы, текущего набора записей будет точно отражают все данные из источника данных.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-109">When the record source for a form is requeried, the current set of records will accurately reflect all data in the record source.</span></span>

<span data-ttu-id="8fbd6-110">Это действие макроса зависит ли вы вызываете его в базу данных клиента или веб-база данных.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-110">The behavior of this macro action depends on whether you are calling it in a client database or a web database.</span></span>

## <a name="client-database"></a><span data-ttu-id="8fbd6-111">База данных клиента</span><span class="sxs-lookup"><span data-stu-id="8fbd6-111">Client database</span></span>

<span data-ttu-id="8fbd6-112">В базе данных клиента можно использовать действие **RefreshRecord** обновление базового источника данных для активной формы или таблицы для отражения изменений, внесенных в данные в текущий набор.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-112">In a client database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the data in the current set.</span></span> <span data-ttu-id="8fbd6-113">Изменения включают указанные текущим пользователем или другими пользователями в многопользовательской среде.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-113">Changes include those made by the current user or by other users in a multiuser environment.</span></span> <span data-ttu-id="8fbd6-114">Это эквивалентно метод **[Refresh](https://msdn.microsoft.com/library/ff836021\(v=office.15\))** .</span><span class="sxs-lookup"><span data-stu-id="8fbd6-114">It is equivalent to the **[Refresh](https://msdn.microsoft.com/library/ff836021\(v=office.15\))** method.</span></span>

<span data-ttu-id="8fbd6-115">Действия макроса **RefreshRecord** производит следующие действия в базе данных клиента:</span><span class="sxs-lookup"><span data-stu-id="8fbd6-115">The **RefreshRecord** macro action does the following in a client database:</span></span>

1.  <span data-ttu-id="8fbd6-116">Обновляет источник записей для активной формы или таблицы для отражения изменений, внесенных в строки в текущий набор.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-116">Updates the record source for the active form or datasheet to reflect the changes made to rows in the current set.</span></span> <span data-ttu-id="8fbd6-117">Для ODBC связанные таблицы, извлекает изменения в записи в текущий набор из источника данных.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-117">For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="8fbd6-118">Обновляет текущий набор в соответствии с изменениями.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-118">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="8fbd6-119">Если была удалена строка в источнике записей, он изменяется для отображения \#удалено.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-119">If a row in the record source has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="8fbd6-120">Обновляет активный или таблицы для отображения какие-либо изменения записей и какие-либо \#удаленных записей в текущий набор.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-120">Refreshes the active or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="8fbd6-121">Вызывает повторный запрос все подчиненные формы и отчеты на активную форму или таблицы.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-121">Requeries any subforms and subreports on the active form or datasheet.</span></span>

## <a name="web-database"></a><span data-ttu-id="8fbd6-122">Веб-база данных</span><span class="sxs-lookup"><span data-stu-id="8fbd6-122">Web database</span></span>

<span data-ttu-id="8fbd6-123">В веб-база данных можно использовать действие **RefreshRecord** обновление базового источника данных для активной формы или таблицы для отражения изменений, внесенных в записи в текущий набор.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-123">In a web database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span></span> <span data-ttu-id="8fbd6-124">Изменения включают сделанные текущего пользователя и других пользователей.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-124">Changes include those made by the current user or other users.</span></span>

<span data-ttu-id="8fbd6-125">Действия макроса **RefreshRecord** выполняет следующие действия в веб-база данных:</span><span class="sxs-lookup"><span data-stu-id="8fbd6-125">The **RefreshRecord** macro action does the following in a web database:</span></span>

1.  <span data-ttu-id="8fbd6-126">Извлекает изменяется с сервера для любого базовые таблицы в текущий набор.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-126">Retrieves changes from the server for any base tables in the current set.</span></span> <span data-ttu-id="8fbd6-127">Для ODBC связанные таблицы, извлекает изменения в записи в текущий набор из источника данных.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-127">For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="8fbd6-128">Обновляет текущий набор в соответствии с изменениями.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-128">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="8fbd6-129">Если строка в текущий набор был удален, он изменяется для отображения \#удалено.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-129">If a row in the current set has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="8fbd6-130">Обновляет активной формы или таблицы для отображения какие-либо изменения записей и какие-либо \#удаленных записей в текущий набор.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-130">Refreshes the active form or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="8fbd6-131">Вызывает повторный запрос все подчиненные формы и отчеты на активную форму или таблицы.</span><span class="sxs-lookup"><span data-stu-id="8fbd6-131">Requeries any subforms and subreports on the active form or datasheet.</span></span>

