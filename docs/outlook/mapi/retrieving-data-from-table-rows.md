---
title: Искомые данные из строк таблицы
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2f389d26ec80b9af3ed28c5eb85b589c9cbb26c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405256"
---
# <a name="retrieving-data-from-table-rows"></a><span data-ttu-id="b1ebe-103">Искомые данные из строк таблицы</span><span class="sxs-lookup"><span data-stu-id="b1ebe-103">Retrieving Data from Table Rows</span></span>

  
  
<span data-ttu-id="b1ebe-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1ebe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1ebe-105">Искомые строки из таблицы включает в себя:</span><span class="sxs-lookup"><span data-stu-id="b1ebe-105">Retrieving rows from a table involves:</span></span>
  
- <span data-ttu-id="b1ebe-106">Получение значений свойств для всех столбцов.</span><span class="sxs-lookup"><span data-stu-id="b1ebe-106">Obtaining the property values for all the columns.</span></span>
    
- <span data-ttu-id="b1ebe-107">Изменение текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="b1ebe-107">Modifying the current position.</span></span>
    
<span data-ttu-id="b1ebe-108">Один из необходимых столбцов в большинстве таблиц — это идентификатор записи — свойство **PR_ENTRYID** ([PidTagEntryId),](pidtagentryid-canonical-property.md)которое можно использовать для открытия объекта, который представляет строку.</span><span class="sxs-lookup"><span data-stu-id="b1ebe-108">One of the required columns in most tables is an entry identifier — the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property — that can be used to open the object that represents the row.</span></span> <span data-ttu-id="b1ebe-109">Этот идентификатор записи обычно является краткосрочным идентификатором записи, который не сохраняется за время существования таблицы.</span><span class="sxs-lookup"><span data-stu-id="b1ebe-109">This entry identifier is usually a short-term entry identifier, one that does not persist past the lifetime of the table.</span></span> <span data-ttu-id="b1ebe-110">Однако это может быть долгосрочный идентификатор, если поставщик услуг, реализующий таблицу, поддерживает только один тип идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="b1ebe-110">However, it can be a long-term identifier if the service provider implementing the table only supports one type of entry identifier.</span></span>
  
<span data-ttu-id="b1ebe-111">Клиенты и поставщики услуг могут сделать один из следующих вызовов для получения строк:</span><span class="sxs-lookup"><span data-stu-id="b1ebe-111">Clients and service providers can make one of the following calls to retrieve rows:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="b1ebe-112">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="b1ebe-112">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="b1ebe-113">Извлекает указанное число строк, начиная с текущей строки в направлении вперед или назад.</span><span class="sxs-lookup"><span data-stu-id="b1ebe-113">Retrieves a specified number of rows starting with the current row in either a forward or backward direction.</span></span>  <br/> |
|[<span data-ttu-id="b1ebe-114">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="b1ebe-114">HrQueryAllRows</span></span>](hrqueryallrows.md) <br/> |<span data-ttu-id="b1ebe-115">Извлекает все строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="b1ebe-115">Retrieves all of the rows in a table.</span></span>  <br/> |
|[<span data-ttu-id="b1ebe-116">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="b1ebe-116">ITableData::HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="b1ebe-117">Извлекает строку в таблице в соответствии со значением столбца индекса.</span><span class="sxs-lookup"><span data-stu-id="b1ebe-117">Retrieves a row in a table according to the value of its index column.</span></span> <span data-ttu-id="b1ebe-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)обычно является столбцом индекса для таблицы.</span><span class="sxs-lookup"><span data-stu-id="b1ebe-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) is usually the index column for a table.</span></span>  <br/> |
   
<span data-ttu-id="b1ebe-119">Если в качестве одного из столбцов таблицы включено необязательное свойство, некоторые строки могут иметь допустимые значения для столбца, а другие — нет.</span><span class="sxs-lookup"><span data-stu-id="b1ebe-119">When an optional property is included as one of the columns in a table, some of the rows might have valid values for the column while others might not.</span></span> <span data-ttu-id="b1ebe-120">Существует ли допустимые значения для столбца, зависит от того, задает ли объект, предоставляющий сведения для строки, свойство.</span><span class="sxs-lookup"><span data-stu-id="b1ebe-120">Whether a valid value exists for a column depends on whether the object providing the information for the row sets the property.</span></span> <span data-ttu-id="b1ebe-121">В зависимости от реализации объекта несуществующее свойство может быть представлено в таблице как **PR_NULL** ([PidTagNull)](pidtagnull-canonical-property.md)или произвольное значение.</span><span class="sxs-lookup"><span data-stu-id="b1ebe-121">Depending on the implementation of the object, a non-existent property can be represented in the table as **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) or an arbitrary value.</span></span> <span data-ttu-id="b1ebe-122">Пользователи таблиц должны быть осторожны, чтобы различать несуще существовать свойства, которые не существуют и имеют бессмысленными значениями и свойствами, которые существуют и имеют допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="b1ebe-122">Users of tables must be careful to differentiate between properties that are nonexistent and have meaningless values and properties that do exist and have valid values.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1ebe-123">См. также</span><span class="sxs-lookup"><span data-stu-id="b1ebe-123">See also</span></span>



[<span data-ttu-id="b1ebe-124">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="b1ebe-124">MAPI Tables</span></span>](mapi-tables.md)

