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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348246"
---
# <a name="hrqueryallrows"></a><span data-ttu-id="8d1d3-103">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="8d1d3-103">HrQueryAllRows</span></span>

  
  
<span data-ttu-id="8d1d3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d1d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d1d3-105">Получает все строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="8d1d3-105">Retrieves all rows of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8d1d3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8d1d3-106">Header file:</span></span>  <br/> |<span data-ttu-id="8d1d3-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="8d1d3-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8d1d3-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="8d1d3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8d1d3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8d1d3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8d1d3-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="8d1d3-110">Called by:</span></span>  <br/> |<span data-ttu-id="8d1d3-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="8d1d3-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="8d1d3-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d1d3-112">Parameters</span></span>

 <span data-ttu-id="8d1d3-113">_птабле_</span><span class="sxs-lookup"><span data-stu-id="8d1d3-113">_ptable_</span></span>
  
> <span data-ttu-id="8d1d3-114">возврата Указатель на таблицу MAPI, из которой извлекаются строки.</span><span class="sxs-lookup"><span data-stu-id="8d1d3-114">[in] Pointer to the MAPI table from which rows are retrieved.</span></span> 
    
 <span data-ttu-id="8d1d3-115">_птага_</span><span class="sxs-lookup"><span data-stu-id="8d1d3-115">_ptaga_</span></span>
  
> <span data-ttu-id="8d1d3-116">возврата Указатель на структуру [спроптагаррай](sproptagarray.md) , которая содержит массив тегов свойств, указывающих столбцы таблицы.</span><span class="sxs-lookup"><span data-stu-id="8d1d3-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating table columns.</span></span> <span data-ttu-id="8d1d3-117">Эти теги используются для выбора конкретных извлекаемых столбцов.</span><span class="sxs-lookup"><span data-stu-id="8d1d3-117">These tags are used to select the specific columns to be retrieved.</span></span> <span data-ttu-id="8d1d3-118">Если параметр _птага_ имеет значение null, **хркуеряллровс** извлекает весь набор столбцов текущего представления таблицы, переданного в параметре _птабле_ .</span><span class="sxs-lookup"><span data-stu-id="8d1d3-118">If the  _ptaga_ parameter is NULL, **HrQueryAllRows** retrieves the entire column set of the current table view passed in the  _ptable_ parameter.</span></span> 
    
 <span data-ttu-id="8d1d3-119">_Прес_</span><span class="sxs-lookup"><span data-stu-id="8d1d3-119">_pres_</span></span>
  
> <span data-ttu-id="8d1d3-120">возврата Указатель на структуру [срестриктион](srestriction.md) , которая содержит ограничения на получение.</span><span class="sxs-lookup"><span data-stu-id="8d1d3-120">[in] Pointer to an [SRestriction](srestriction.md) structure that contains retrieval restrictions.</span></span> <span data-ttu-id="8d1d3-121">Если параметр _прес_ имеет значение null, **хркуеряллровс** не делает никаких ограничений.</span><span class="sxs-lookup"><span data-stu-id="8d1d3-121">If the  _pres_ parameter is NULL, **HrQueryAllRows** makes no restrictions.</span></span> 
    
 <span data-ttu-id="8d1d3-122">_псос_</span><span class="sxs-lookup"><span data-stu-id="8d1d3-122">_psos_</span></span>
  
> <span data-ttu-id="8d1d3-123">возврата Указатель на структуру [ссортордерсет](ssortorderset.md) , определяющую порядок сортировки извлекаемых столбцов.</span><span class="sxs-lookup"><span data-stu-id="8d1d3-123">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order of the columns to be retrieved.</span></span> <span data-ttu-id="8d1d3-124">Если параметр _псос_ имеет значение null, используется порядок сортировки по умолчанию для таблицы.</span><span class="sxs-lookup"><span data-stu-id="8d1d3-124">If the  _psos_ parameter is NULL, the default sort order for the table is used.</span></span> 
    
 <span data-ttu-id="8d1d3-125">_Кровсмакс_</span><span class="sxs-lookup"><span data-stu-id="8d1d3-125">_crowsMax_</span></span>
  
> <span data-ttu-id="8d1d3-126">возврата Максимальное количество извлекаемых строк.</span><span class="sxs-lookup"><span data-stu-id="8d1d3-126">[in] Maximum number of rows to be retrieved.</span></span> <span data-ttu-id="8d1d3-127">Если значение параметра _кровсмакс_ равно нулю, не задано максимальное число извлеченных строк.</span><span class="sxs-lookup"><span data-stu-id="8d1d3-127">If the value of the  _crowsMax_ parameter is zero, no limit on the number of rows retrieved is set.</span></span> 
    
 <span data-ttu-id="8d1d3-128">_ппровс_</span><span class="sxs-lookup"><span data-stu-id="8d1d3-128">_pprows_</span></span>
  
> <span data-ttu-id="8d1d3-129">вышли Указатель на указатель на возвращаемую структуру [SRowSet](srowset.md) , содержащую массив указателей на извлеченные строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="8d1d3-129">[out] Pointer to a pointer to the returned [SRowSet](srowset.md) structure that contains an array of pointers to the retrieved table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8d1d3-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d1d3-130">Return value</span></span>

<span data-ttu-id="8d1d3-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d1d3-131">S_OK</span></span> 
  
> <span data-ttu-id="8d1d3-132">Вызов получил ожидаемые строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="8d1d3-132">The call retrieved the expected rows of a table.</span></span> 
    
<span data-ttu-id="8d1d3-133">МАПИ_Е_ТАБЛЕ_ТУ_БИГ</span><span class="sxs-lookup"><span data-stu-id="8d1d3-133">MAPI_E_TABLE_TOO_BIG</span></span> 
  
> <span data-ttu-id="8d1d3-134">Количество строк в таблице больше, чем число, переданное для параметра _кровсмакс_ .</span><span class="sxs-lookup"><span data-stu-id="8d1d3-134">The number of rows in the table is larger than the number passed for the  _crowsMax_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8d1d3-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="8d1d3-135">Remarks</span></span>

<span data-ttu-id="8d1d3-136">Клиентское приложение или поставщик услуг не могут управлять количеством строк, которые **хркуеряллровс** пытается получить, за исключением импосинг ограничения, на которые указывает параметр _прес_ .</span><span class="sxs-lookup"><span data-stu-id="8d1d3-136">A client application or service provider has no control over the number of rows **HrQueryAllRows** attempts to retrieve, other than by imposing a restriction pointed to by the  _pres_ parameter.</span></span> <span data-ttu-id="8d1d3-137">Параметр _кровсмакс_ не ограничивает извлечение определенным количеством строк таблицы, а определяет максимальный объем памяти, доступный для хранения всех извлеченных строк.</span><span class="sxs-lookup"><span data-stu-id="8d1d3-137">The  _crowsMax_ parameter does not limit the retrieval to a certain number of table rows, but rather defines a maximum amount of memory available to hold all retrieved rows.</span></span> <span data-ttu-id="8d1d3-138">Единственной защитой от значительного переполнения памяти является функция стопгап, предоставляемая параметром _кровсмакс_.</span><span class="sxs-lookup"><span data-stu-id="8d1d3-138">The only protection against massive memory overflow is the stopgap feature provided by setting  _crowsMax_.</span></span> <span data-ttu-id="8d1d3-139">Ошибка Return МАПИ_Е_ТАБЛЕ_ТУ_БИГ означает, что таблица содержит слишком много строк, которые должны храниться в памяти сразу.</span><span class="sxs-lookup"><span data-stu-id="8d1d3-139">The error return MAPI_E_TABLE_TOO_BIG means the table contains too many rows to be held all at once in memory.</span></span> 
  
<span data-ttu-id="8d1d3-140">Таблицы, которые обычно небольшие, например, таблица хранилища сообщений или таблица поставщиков, обычно могут безопасно извлекаться с помощью **хркуеряллровс**.</span><span class="sxs-lookup"><span data-stu-id="8d1d3-140">Tables that are typically small, such as a message store table or a provider table, usually can be safely retrieved with **HrQueryAllRows**.</span></span> <span data-ttu-id="8d1d3-141">Таблицы под угрозой очень большого размера, например таблица содержимого или даже таблица получателей, должны проходить через подразделы с помощью метода [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="8d1d3-141">Tables at risk of being very large, such as a contents table or even a recipients table, should be traversed in subsections using the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> 
  
<span data-ttu-id="8d1d3-142">Если какие-либо свойства таблицы не определены при вызове **хркуеряллровс** , они возвращаются с типом свойства пт_нулл и идентификатором свойства проп_ид_нулл</span><span class="sxs-lookup"><span data-stu-id="8d1d3-142">If any table properties are undefined when **HrQueryAllRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL</span></span> 
  

