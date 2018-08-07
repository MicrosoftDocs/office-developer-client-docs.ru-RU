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
ms.openlocfilehash: 451bab57d4e2e8669a25d119f9ce28a8f78e628f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812476"
---
# <a name="tips-for-working-with-tables"></a><span data-ttu-id="3eec9-103">Советы по работе с таблицами</span><span class="sxs-lookup"><span data-stu-id="3eec9-103">Tips for Working with Tables</span></span>

  
  
<span data-ttu-id="3eec9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3eec9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3eec9-105">Работа с MAPI в таблице — это немного аналогично использованию таблицы реляционной базы данных.</span><span class="sxs-lookup"><span data-stu-id="3eec9-105">Working with a MAPI table is a little like working with a relational database table.</span></span> <span data-ttu-id="3eec9-106">Пользователя можно ограничить число строк и столбцов в представлении и укажите их порядок.</span><span class="sxs-lookup"><span data-stu-id="3eec9-106">A user can limit the number of rows and columns in the view and specify their order.</span></span> <span data-ttu-id="3eec9-107">Строк может быть извлеченных по отдельности или в группах.</span><span class="sxs-lookup"><span data-stu-id="3eec9-107">Rows can be retrieved one at a time or in groups.</span></span> <span data-ttu-id="3eec9-108">Можно перемещать курсор, который хранит текущую позицию в определенное место в таблице.</span><span class="sxs-lookup"><span data-stu-id="3eec9-108">A cursor that keeps track of the current position can be moved to a specific place in the table.</span></span> 
  
<span data-ttu-id="3eec9-109">Для работы с таблицами, клиенты используют интерфейс только для чтения, [IMAPITable: IUnknown](imapitableiunknown.md), тогда как поставщиков услуг, в зависимости от того, является ли они являются данные на основании таблицы, можно использовать либо **IMAPITable** или [ITableData: IUnknown](itabledataiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="3eec9-109">To work with tables, clients use the read-only interface, [IMAPITable : IUnknown](imapitableiunknown.md), whereas service providers, depending on whether they own the data that the table is based on, can use either **IMAPITable** or [ITableData : IUnknown](itabledataiunknown.md).</span></span> <span data-ttu-id="3eec9-110">Операции, определенные в эти интерфейсы могут относиться к операции всех пользователей из таблиц или можно было вызвать и операции, которые не используются как широко так, как они более сложных.</span><span class="sxs-lookup"><span data-stu-id="3eec9-110">The operations defined in these interfaces can be categorized as operations that all users of tables either do or can invoke and operations that are not as widely used because they are more advanced.</span></span> <span data-ttu-id="3eec9-111">Некоторые из дополнительных операций, более сложная реализация; другие пользователи не более сложны, но могут представлять интерес для малых нечасто, компоненты MAPI.</span><span class="sxs-lookup"><span data-stu-id="3eec9-111">Some of the advanced operations are more complex to implement; others are no more complex, but are of interest to a small minority of MAPI components.</span></span> 
  
<span data-ttu-id="3eec9-112">Наиболее распространенных операций, являются:</span><span class="sxs-lookup"><span data-stu-id="3eec9-112">The more common operations are:</span></span>
  
- <span data-ttu-id="3eec9-113">Столбец операций, которые могут повлиять на одном столбцов.</span><span class="sxs-lookup"><span data-stu-id="3eec9-113">Column operations, which affect single columns.</span></span> <span data-ttu-id="3eec9-114">Эти возможности включают определение свойств, которые будут включены в набор столбцов и порядок, в котором они должны быть включены.</span><span class="sxs-lookup"><span data-stu-id="3eec9-114">These include specifying the properties to be included in the column set and the order in which they should be included.</span></span>
    
- <span data-ttu-id="3eec9-115">Строки операций, которые могут повлиять на отдельных строк.</span><span class="sxs-lookup"><span data-stu-id="3eec9-115">Row operations, which affect single rows.</span></span> <span data-ttu-id="3eec9-116">К ним относятся извлечения данных и операций обслуживания: Добавление, удаление и изменение одну строку или строки.</span><span class="sxs-lookup"><span data-stu-id="3eec9-116">These include data retrieval and the maintenance operations: adding, deleting, and modifying a single row or rows.</span></span>
    
- <span data-ttu-id="3eec9-117">Глобальные операции, которые влияют на всю таблицу.</span><span class="sxs-lookup"><span data-stu-id="3eec9-117">Global operations, which affect the entire table.</span></span> <span data-ttu-id="3eec9-118">К ним относятся события уведомлений, поиска и сортировки.</span><span class="sxs-lookup"><span data-stu-id="3eec9-118">These include event notification, searching and sorting.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3eec9-119">См. также</span><span class="sxs-lookup"><span data-stu-id="3eec9-119">See also</span></span>



[<span data-ttu-id="3eec9-120">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="3eec9-120">MAPI Tables</span></span>](mapi-tables.md)

