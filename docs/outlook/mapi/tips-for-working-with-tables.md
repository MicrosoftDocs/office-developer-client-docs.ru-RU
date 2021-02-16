---
title: Советы по работе с таблицами
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8f310c6331df941d3093b276b6dec47f740412e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439739"
---
# <a name="tips-for-working-with-tables"></a><span data-ttu-id="7b198-103">Советы по работе с таблицами</span><span class="sxs-lookup"><span data-stu-id="7b198-103">Tips for Working with Tables</span></span>

  
  
<span data-ttu-id="7b198-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b198-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b198-105">Работа с таблицей MAPI немного похоже на работу с реляционной таблицей базы данных.</span><span class="sxs-lookup"><span data-stu-id="7b198-105">Working with a MAPI table is a little like working with a relational database table.</span></span> <span data-ttu-id="7b198-106">Пользователь может ограничить число строк и столбцов в представлении и указать их порядок.</span><span class="sxs-lookup"><span data-stu-id="7b198-106">A user can limit the number of rows and columns in the view and specify their order.</span></span> <span data-ttu-id="7b198-107">Строки можно получать по одной или группам.</span><span class="sxs-lookup"><span data-stu-id="7b198-107">Rows can be retrieved one at a time or in groups.</span></span> <span data-ttu-id="7b198-108">Курсор, отслеживая текущее положение, можно перемещен в определенное место в таблице.</span><span class="sxs-lookup"><span data-stu-id="7b198-108">A cursor that keeps track of the current position can be moved to a specific place in the table.</span></span> 
  
<span data-ttu-id="7b198-109">Для работы с таблицами клиенты используют интерфейс только для [чтения, IMAPITable : IUnknown,](imapitableiunknown.md)тогда как поставщики услуг, в зависимости от того, являются ли они владельцем данных, на которых основана таблица, могут использовать **IMAPITable** или [ITableData : IUnknown](itabledataiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7b198-109">To work with tables, clients use the read-only interface, [IMAPITable : IUnknown](imapitableiunknown.md), whereas service providers, depending on whether they own the data that the table is based on, can use either **IMAPITable** or [ITableData : IUnknown](itabledataiunknown.md).</span></span> <span data-ttu-id="7b198-110">Операции, определенные в этих интерфейсах, можно классифицируются как операции, которые все пользователи таблиц либо делают, либо могут вызывать, и операции, которые не так широко используются, так как они являются более расширенными.</span><span class="sxs-lookup"><span data-stu-id="7b198-110">The operations defined in these interfaces can be categorized as operations that all users of tables either do or can invoke and operations that are not as widely used because they are more advanced.</span></span> <span data-ttu-id="7b198-111">Некоторые расширенные операции сложнее реализовать; другие компоненты не являются более сложными, но их интересует небольшая часть компонентов MAPI.</span><span class="sxs-lookup"><span data-stu-id="7b198-111">Some of the advanced operations are more complex to implement; others are no more complex, but are of interest to a small minority of MAPI components.</span></span> 
  
<span data-ttu-id="7b198-112">Наиболее распространенные операции:</span><span class="sxs-lookup"><span data-stu-id="7b198-112">The more common operations are:</span></span>
  
- <span data-ttu-id="7b198-113">Операции столбцов, влияющие на отдельные столбцы.</span><span class="sxs-lookup"><span data-stu-id="7b198-113">Column operations, which affect single columns.</span></span> <span data-ttu-id="7b198-114">К ним относятся указание свойств, которые необходимо включить в набор столбцов, и порядок их включаемой информации.</span><span class="sxs-lookup"><span data-stu-id="7b198-114">These include specifying the properties to be included in the column set and the order in which they should be included.</span></span>
    
- <span data-ttu-id="7b198-115">Операции со строками, влияющие на отдельные строки.</span><span class="sxs-lookup"><span data-stu-id="7b198-115">Row operations, which affect single rows.</span></span> <span data-ttu-id="7b198-116">К ним относятся и сбор данных и операции обслуживания: добавление, удаление и изменение одной строки или строки.</span><span class="sxs-lookup"><span data-stu-id="7b198-116">These include data retrieval and the maintenance operations: adding, deleting, and modifying a single row or rows.</span></span>
    
- <span data-ttu-id="7b198-117">Глобальные операции, влияющие на всю таблицу.</span><span class="sxs-lookup"><span data-stu-id="7b198-117">Global operations, which affect the entire table.</span></span> <span data-ttu-id="7b198-118">К ним относятся уведомления о событиях, поиск и сортировка.</span><span class="sxs-lookup"><span data-stu-id="7b198-118">These include event notification, searching and sorting.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b198-119">См. также</span><span class="sxs-lookup"><span data-stu-id="7b198-119">See also</span></span>



[<span data-ttu-id="7b198-120">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="7b198-120">MAPI Tables</span></span>](mapi-tables.md)

