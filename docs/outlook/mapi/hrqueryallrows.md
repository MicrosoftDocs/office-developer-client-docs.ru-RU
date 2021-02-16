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
# <a name="hrqueryallrows"></a><span data-ttu-id="979a1-103">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="979a1-103">HrQueryAllRows</span></span>

  
  
<span data-ttu-id="979a1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="979a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="979a1-105">Извлекает все строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="979a1-105">Retrieves all rows of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="979a1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="979a1-106">Header file:</span></span>  <br/> |<span data-ttu-id="979a1-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="979a1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="979a1-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="979a1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="979a1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="979a1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="979a1-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="979a1-110">Called by:</span></span>  <br/> |<span data-ttu-id="979a1-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="979a1-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="979a1-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="979a1-112">Parameters</span></span>

 <span data-ttu-id="979a1-113">_ptable_</span><span class="sxs-lookup"><span data-stu-id="979a1-113">_ptable_</span></span>
  
> <span data-ttu-id="979a1-114">[in] Указатель на таблицу MAPI, из которой извлекаются строки.</span><span class="sxs-lookup"><span data-stu-id="979a1-114">[in] Pointer to the MAPI table from which rows are retrieved.</span></span> 
    
 <span data-ttu-id="979a1-115">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="979a1-115">_ptaga_</span></span>
  
> <span data-ttu-id="979a1-116">[in] Указатель на [структуру SPropTagArray,](sproptagarray.md) которая содержит массив тегов свойств, указывающих столбцы таблицы.</span><span class="sxs-lookup"><span data-stu-id="979a1-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating table columns.</span></span> <span data-ttu-id="979a1-117">Эти теги используются для выбора определенных столбцов, которые необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="979a1-117">These tags are used to select the specific columns to be retrieved.</span></span> <span data-ttu-id="979a1-118">Если параметр _ptaga_ имеет NULL, **HrQueryAllRows** извлекает весь набор столбцов текущего представления таблицы, переданного в _параметре ptable._</span><span class="sxs-lookup"><span data-stu-id="979a1-118">If the  _ptaga_ parameter is NULL, **HrQueryAllRows** retrieves the entire column set of the current table view passed in the  _ptable_ parameter.</span></span> 
    
 <span data-ttu-id="979a1-119">_pres_</span><span class="sxs-lookup"><span data-stu-id="979a1-119">_pres_</span></span>
  
> <span data-ttu-id="979a1-120">[in] Указатель на [структуру SRestriction,](srestriction.md) которая содержит ограничения итерации.</span><span class="sxs-lookup"><span data-stu-id="979a1-120">[in] Pointer to an [SRestriction](srestriction.md) structure that contains retrieval restrictions.</span></span> <span data-ttu-id="979a1-121">Если параметр  _pres_ имеет NULL, **HrQueryAllRows** не создает ограничений.</span><span class="sxs-lookup"><span data-stu-id="979a1-121">If the  _pres_ parameter is NULL, **HrQueryAllRows** makes no restrictions.</span></span> 
    
 <span data-ttu-id="979a1-122">_psos_</span><span class="sxs-lookup"><span data-stu-id="979a1-122">_psos_</span></span>
  
> <span data-ttu-id="979a1-123">[in] Указатель на [структуру SSortOrderSet,](ssortorderset.md) определяя порядок сортировки извлекаемого столбца.</span><span class="sxs-lookup"><span data-stu-id="979a1-123">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order of the columns to be retrieved.</span></span> <span data-ttu-id="979a1-124">Если параметр  _psos_ имеет значение NULL, используется порядок сортировки по умолчанию для таблицы.</span><span class="sxs-lookup"><span data-stu-id="979a1-124">If the  _psos_ parameter is NULL, the default sort order for the table is used.</span></span> 
    
 <span data-ttu-id="979a1-125">_многофайтовая_</span><span class="sxs-lookup"><span data-stu-id="979a1-125">_crowsMax_</span></span>
  
> <span data-ttu-id="979a1-126">[in] Максимальное число извлекаемых строк.</span><span class="sxs-lookup"><span data-stu-id="979a1-126">[in] Maximum number of rows to be retrieved.</span></span> <span data-ttu-id="979a1-127">Если значение параметра  _of themax_ — ноль, никакие ограничения на число извлекаемой строки не заданы.</span><span class="sxs-lookup"><span data-stu-id="979a1-127">If the value of the  _crowsMax_ parameter is zero, no limit on the number of rows retrieved is set.</span></span> 
    
 <span data-ttu-id="979a1-128">_pprows_</span><span class="sxs-lookup"><span data-stu-id="979a1-128">_pprows_</span></span>
  
> <span data-ttu-id="979a1-129">[out] Указатель на указатель на возвращенную структуру [SRowSet,](srowset.md) которая содержит массив указателей на полученные строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="979a1-129">[out] Pointer to a pointer to the returned [SRowSet](srowset.md) structure that contains an array of pointers to the retrieved table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="979a1-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="979a1-130">Return value</span></span>

<span data-ttu-id="979a1-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="979a1-131">S_OK</span></span> 
  
> <span data-ttu-id="979a1-132">Вызов извлек ожидаемые строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="979a1-132">The call retrieved the expected rows of a table.</span></span> 
    
<span data-ttu-id="979a1-133">MAPI_E_TABLE_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="979a1-133">MAPI_E_TABLE_TOO_BIG</span></span> 
  
> <span data-ttu-id="979a1-134">Число строк в таблице больше, чем число, переданные для параметра _параметров ofMax._</span><span class="sxs-lookup"><span data-stu-id="979a1-134">The number of rows in the table is larger than the number passed for the  _crowsMax_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="979a1-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="979a1-135">Remarks</span></span>

<span data-ttu-id="979a1-136">Клиентские приложения или поставщик службы не контролируют число строк **HrQueryAllRows,** которые пытается получить, за исключением наложенного ограничения, на которое указывает параметр _pres._</span><span class="sxs-lookup"><span data-stu-id="979a1-136">A client application or service provider has no control over the number of rows **HrQueryAllRows** attempts to retrieve, other than by imposing a restriction pointed to by the  _pres_ parameter.</span></span> <span data-ttu-id="979a1-137">Параметра  _themax_ не ограничивает извлечение определенным количеством строк таблицы, а определяет максимальный объем памяти, доступный для удержания всех полученных строк.</span><span class="sxs-lookup"><span data-stu-id="979a1-137">The  _crowsMax_ parameter does not limit the retrieval to a certain number of table rows, but rather defines a maximum amount of memory available to hold all retrieved rows.</span></span> <span data-ttu-id="979a1-138">Единственная защита от переполнения памяти — это функция остановки, предоставляемая установкой _параметра settingsMax._</span><span class="sxs-lookup"><span data-stu-id="979a1-138">The only protection against massive memory overflow is the stopgap feature provided by setting  _crowsMax_.</span></span> <span data-ttu-id="979a1-139">Возвращаемая ошибка MAPI_E_TABLE_TOO_BIG означает, что таблица содержит слишком много строк, которые необходимо одновременно удерживать в памяти.</span><span class="sxs-lookup"><span data-stu-id="979a1-139">The error return MAPI_E_TABLE_TOO_BIG means the table contains too many rows to be held all at once in memory.</span></span> 
  
<span data-ttu-id="979a1-140">Обычно небольшие таблицы, такие как таблица хранения сообщений или таблица поставщика, обычно можно безопасно получить с помощью **HrQueryAllRows.**</span><span class="sxs-lookup"><span data-stu-id="979a1-140">Tables that are typically small, such as a message store table or a provider table, usually can be safely retrieved with **HrQueryAllRows**.</span></span> <span data-ttu-id="979a1-141">Таблицы с риском очень большого размера, такие как таблица содержимого или даже таблица получателей, следует обходить в подразделах с помощью метода [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="979a1-141">Tables at risk of being very large, such as a contents table or even a recipients table, should be traversed in subsections using the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> 
  
<span data-ttu-id="979a1-142">Если при вызвании **HrQueryAllRows** какие-либо свойства таблицы не определены, они возвращаются с типом PT_NULL и идентификатором PROP_ID_NULL</span><span class="sxs-lookup"><span data-stu-id="979a1-142">If any table properties are undefined when **HrQueryAllRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL</span></span> 
  

