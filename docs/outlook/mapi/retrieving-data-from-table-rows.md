---
title: Получение данных из строк таблиц
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 91b1fa06fd47321e9c19d9751caac793e27e8f16
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812148"
---
# <a name="retrieving-data-from-table-rows"></a><span data-ttu-id="514c0-103">Получение данных из строк таблиц</span><span class="sxs-lookup"><span data-stu-id="514c0-103">Retrieving Data from Table Rows</span></span>

  
  
<span data-ttu-id="514c0-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="514c0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="514c0-105">Извлечение строк из таблицы включает в себя:</span><span class="sxs-lookup"><span data-stu-id="514c0-105">Retrieving rows from a table involves:</span></span>
  
- <span data-ttu-id="514c0-106">Получение значений свойств для всех столбцов.</span><span class="sxs-lookup"><span data-stu-id="514c0-106">Obtaining the property values for all the columns.</span></span>
    
- <span data-ttu-id="514c0-107">Изменение текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="514c0-107">Modifying the current position.</span></span>
    
<span data-ttu-id="514c0-108">Один из обязательные столбцы в большинстве таблицах — это идентификатор операции — свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) — используется для открытия объект, представляющий строку.</span><span class="sxs-lookup"><span data-stu-id="514c0-108">One of the required columns in most tables is an entry identifier — the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property — that can be used to open the object that represents the row.</span></span> <span data-ttu-id="514c0-109">Этот идентификатор записи обычно является краткосрочных идентификатор записи, которая не сохраняет за время жизни таблицы.</span><span class="sxs-lookup"><span data-stu-id="514c0-109">This entry identifier is usually a short-term entry identifier, one that does not persist past the lifetime of the table.</span></span> <span data-ttu-id="514c0-110">Тем не менее может быть долгосрочного идентификатор, если реализация в таблице только поставщик услуг поддерживает один тип идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="514c0-110">However, it can be a long-term identifier if the service provider implementing the table only supports one type of entry identifier.</span></span>
  
<span data-ttu-id="514c0-111">Клиенты и поставщиков услуг можно сделать одного из следующих вызовов для извлечения строк:</span><span class="sxs-lookup"><span data-stu-id="514c0-111">Clients and service providers can make one of the following calls to retrieve rows:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="514c0-112">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="514c0-112">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="514c0-113">Извлекает указанное число строк, начиная с текущей строки в прямом или обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="514c0-113">Retrieves a specified number of rows starting with the current row in either a forward or backward direction.</span></span>  <br/> |
|[<span data-ttu-id="514c0-114">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="514c0-114">HrQueryAllRows</span></span>](hrqueryallrows.md) <br/> |<span data-ttu-id="514c0-115">Извлекает все строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="514c0-115">Retrieves all of the rows in a table.</span></span>  <br/> |
|[<span data-ttu-id="514c0-116">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="514c0-116">ITableData::HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="514c0-117">Получает строку в таблице определяется значение его индекс столбца.</span><span class="sxs-lookup"><span data-stu-id="514c0-117">Retrieves a row in a table according to the value of its index column.</span></span> <span data-ttu-id="514c0-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) — это обычно индекс столбца для таблицы.</span><span class="sxs-lookup"><span data-stu-id="514c0-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) is usually the index column for a table.</span></span>  <br/> |
   
<span data-ttu-id="514c0-119">Когда это необязательное свойство используется в качестве одного из столбцов в таблице, некоторые строки во время другие пользователи могут не может быть допустимые значения для столбца.</span><span class="sxs-lookup"><span data-stu-id="514c0-119">When an optional property is included as one of the columns in a table, some of the rows might have valid values for the column while others might not.</span></span> <span data-ttu-id="514c0-120">Существует ли допустимое значение для столбца зависит от того, является ли объект, предоставляющий сведения о строке устанавливает для свойства.</span><span class="sxs-lookup"><span data-stu-id="514c0-120">Whether a valid value exists for a column depends on whether the object providing the information for the row sets the property.</span></span> <span data-ttu-id="514c0-121">В зависимости от реализации объектов несуществующее свойство может быть представлен в таблице как **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) или произвольного значения.</span><span class="sxs-lookup"><span data-stu-id="514c0-121">Depending on the implementation of the object, a non-existent property can be represented in the table as **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) or an arbitrary value.</span></span> <span data-ttu-id="514c0-122">Пользователи таблиц необходимо следить за тем отличать свойства, которые не существуют и не имеет смысла значения и свойства, которые существуют и имеют допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="514c0-122">Users of tables must be careful to differentiate between properties that are nonexistent and have meaningless values and properties that do exist and have valid values.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="514c0-123">См. также</span><span class="sxs-lookup"><span data-stu-id="514c0-123">See also</span></span>



[<span data-ttu-id="514c0-124">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="514c0-124">MAPI Tables</span></span>](mapi-tables.md)

