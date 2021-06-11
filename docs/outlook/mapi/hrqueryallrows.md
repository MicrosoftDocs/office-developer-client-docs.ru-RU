---
title: HrQueryAllRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrQueryAllRows
api_type:
- HeaderDef
ms.assetid: b08fadcf-cdf3-48b7-9489-d7f745266482
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0f09304f21180d9ebc2a1e1dcc54ebadd3622804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422896"
---
# <a name="hrqueryallrows"></a><span data-ttu-id="b0b85-103">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="b0b85-103">HrQueryAllRows</span></span>

  
  
<span data-ttu-id="b0b85-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0b85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0b85-105">Извлекает все строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="b0b85-105">Retrieves all rows of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0b85-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b0b85-106">Header file:</span></span>  <br/> |<span data-ttu-id="b0b85-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b0b85-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b0b85-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="b0b85-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b0b85-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b0b85-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b0b85-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="b0b85-110">Called by:</span></span>  <br/> |<span data-ttu-id="b0b85-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="b0b85-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrQueryAllRows(
  LPMAPITABLE ptable,
  LPSPropTagArray ptaga,
  LPSRestriction pres,
  LPSSortOrderSet psos,
  LONG crowsMax,
  LPSRowSet FAR * pprows
);
```

## <a name="parameters"></a><span data-ttu-id="b0b85-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="b0b85-112">Parameters</span></span>

 <span data-ttu-id="b0b85-113">_ptable_</span><span class="sxs-lookup"><span data-stu-id="b0b85-113">_ptable_</span></span>
  
> <span data-ttu-id="b0b85-114">[in] Указатель на таблицу MAPI, из которой извлекаются строки.</span><span class="sxs-lookup"><span data-stu-id="b0b85-114">[in] Pointer to the MAPI table from which rows are retrieved.</span></span> 
    
 <span data-ttu-id="b0b85-115">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="b0b85-115">_ptaga_</span></span>
  
> <span data-ttu-id="b0b85-116">[in] Указатель на [структуру SPropTagArray,](sproptagarray.md) содержащий массив тегов свойств, указывающих столбцы таблиц.</span><span class="sxs-lookup"><span data-stu-id="b0b85-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating table columns.</span></span> <span data-ttu-id="b0b85-117">Эти теги используются для выбора определенных столбцов, которые будут извлечены.</span><span class="sxs-lookup"><span data-stu-id="b0b85-117">These tags are used to select the specific columns to be retrieved.</span></span> <span data-ttu-id="b0b85-118">Если _параметром ptaga_ является NULL, **hrQueryAllRows** извлекает весь набор столбцов текущего представления таблицы, переданного в _параметре ptable._</span><span class="sxs-lookup"><span data-stu-id="b0b85-118">If the  _ptaga_ parameter is NULL, **HrQueryAllRows** retrieves the entire column set of the current table view passed in the  _ptable_ parameter.</span></span> 
    
 <span data-ttu-id="b0b85-119">_pres_</span><span class="sxs-lookup"><span data-stu-id="b0b85-119">_pres_</span></span>
  
> <span data-ttu-id="b0b85-120">[in] Указатель на [структуру SRestriction,](srestriction.md) которая содержит ограничения на ирисовку.</span><span class="sxs-lookup"><span data-stu-id="b0b85-120">[in] Pointer to an [SRestriction](srestriction.md) structure that contains retrieval restrictions.</span></span> <span data-ttu-id="b0b85-121">Если параметр  _pres_ NULL, **hrQueryAllRows** не создает ограничений.</span><span class="sxs-lookup"><span data-stu-id="b0b85-121">If the  _pres_ parameter is NULL, **HrQueryAllRows** makes no restrictions.</span></span> 
    
 <span data-ttu-id="b0b85-122">_psos_</span><span class="sxs-lookup"><span data-stu-id="b0b85-122">_psos_</span></span>
  
> <span data-ttu-id="b0b85-123">[in] Указатель на [структуру SSortOrderSet,](ssortorderset.md) определяя порядок сортировки извлекаемой колонны.</span><span class="sxs-lookup"><span data-stu-id="b0b85-123">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order of the columns to be retrieved.</span></span> <span data-ttu-id="b0b85-124">Если параметр  _psos_ — NULL, используется порядок сортировки по умолчанию для таблицы.</span><span class="sxs-lookup"><span data-stu-id="b0b85-124">If the  _psos_ parameter is NULL, the default sort order for the table is used.</span></span> 
    
 <span data-ttu-id="b0b85-125">_crowsMax_</span><span class="sxs-lookup"><span data-stu-id="b0b85-125">_crowsMax_</span></span>
  
> <span data-ttu-id="b0b85-126">[in] Максимальное количество строк, которые необходимо извлечь.</span><span class="sxs-lookup"><span data-stu-id="b0b85-126">[in] Maximum number of rows to be retrieved.</span></span> <span data-ttu-id="b0b85-127">Если значение параметра  _crowsMax_ нулевое, не устанавливается ограничение на количество извлеченных строк.</span><span class="sxs-lookup"><span data-stu-id="b0b85-127">If the value of the  _crowsMax_ parameter is zero, no limit on the number of rows retrieved is set.</span></span> 
    
 <span data-ttu-id="b0b85-128">_pprows_</span><span class="sxs-lookup"><span data-stu-id="b0b85-128">_pprows_</span></span>
  
> <span data-ttu-id="b0b85-129">[вышел] Указатель на указатель на возвращенную [структуру SRowSet,](srowset.md) которая содержит массив указателей к извлеченным строкам таблицы.</span><span class="sxs-lookup"><span data-stu-id="b0b85-129">[out] Pointer to a pointer to the returned [SRowSet](srowset.md) structure that contains an array of pointers to the retrieved table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b0b85-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0b85-130">Return value</span></span>

<span data-ttu-id="b0b85-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="b0b85-131">S_OK</span></span> 
  
> <span data-ttu-id="b0b85-132">Вызов извлек ожидаемые строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="b0b85-132">The call retrieved the expected rows of a table.</span></span> 
    
<span data-ttu-id="b0b85-133">MAPI_E_TABLE_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="b0b85-133">MAPI_E_TABLE_TOO_BIG</span></span> 
  
> <span data-ttu-id="b0b85-134">Количество строк в таблице больше, чем число, переданного для _параметра crowsMax._</span><span class="sxs-lookup"><span data-stu-id="b0b85-134">The number of rows in the table is larger than the number passed for the  _crowsMax_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b0b85-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="b0b85-135">Remarks</span></span>

<span data-ttu-id="b0b85-136">Клиентские приложения или поставщик услуг не могут контролировать количество строк, которые **hrQueryAllRows** пытается получить, за исключением введения ограничения, на которое указывает параметр _pres._</span><span class="sxs-lookup"><span data-stu-id="b0b85-136">A client application or service provider has no control over the number of rows **HrQueryAllRows** attempts to retrieve, other than by imposing a restriction pointed to by the  _pres_ parameter.</span></span> <span data-ttu-id="b0b85-137">Параметр  _crowsMax_ не ограничивает извлечение определенным количеством строк таблицы, а определяет максимальное количество памяти, доступной для удержания всех извлеченных строк.</span><span class="sxs-lookup"><span data-stu-id="b0b85-137">The  _crowsMax_ parameter does not limit the retrieval to a certain number of table rows, but rather defines a maximum amount of memory available to hold all retrieved rows.</span></span> <span data-ttu-id="b0b85-138">Единственной защитой от массового переполнения памяти является функция stopgap, предоставляемая установкой _crowsMax._</span><span class="sxs-lookup"><span data-stu-id="b0b85-138">The only protection against massive memory overflow is the stopgap feature provided by setting  _crowsMax_.</span></span> <span data-ttu-id="b0b85-139">Возврат ошибок MAPI_E_TABLE_TOO_BIG означает, что в таблице содержится слишком много строк, которые должны быть одновременно в памяти.</span><span class="sxs-lookup"><span data-stu-id="b0b85-139">The error return MAPI_E_TABLE_TOO_BIG means the table contains too many rows to be held all at once in memory.</span></span> 
  
<span data-ttu-id="b0b85-140">Таблицы, обычно небольшие, например таблица хранения сообщений или таблица поставщиков, обычно можно безопасно получить с **помощью HrQueryAllRows.**</span><span class="sxs-lookup"><span data-stu-id="b0b85-140">Tables that are typically small, such as a message store table or a provider table, usually can be safely retrieved with **HrQueryAllRows**.</span></span> <span data-ttu-id="b0b85-141">Таблицы с риском быть очень большими, например таблица содержимого или даже таблица получателей, должны быть пройдены в подразделах с помощью метода [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="b0b85-141">Tables at risk of being very large, such as a contents table or even a recipients table, should be traversed in subsections using the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> 
  
<span data-ttu-id="b0b85-142">Если какие-либо свойства таблицы не определены при призыве **HrQueryAllRows,** они возвращаются с помощью PT_NULL свойства и идентификатора PROP_ID_NULL</span><span class="sxs-lookup"><span data-stu-id="b0b85-142">If any table properties are undefined when **HrQueryAllRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL</span></span> 
  

