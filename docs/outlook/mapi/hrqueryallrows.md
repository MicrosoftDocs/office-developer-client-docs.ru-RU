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
ms.openlocfilehash: 5c62e5919c6e605aa4b60f48072996ed1fd4c355
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808694"
---
# <a name="hrqueryallrows"></a><span data-ttu-id="de5ac-103">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="de5ac-103">HrQueryAllRows</span></span>

  
  
<span data-ttu-id="de5ac-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="de5ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="de5ac-105">Извлекает все строки из таблицы.</span><span class="sxs-lookup"><span data-stu-id="de5ac-105">Retrieves all rows of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de5ac-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="de5ac-106">Header file:</span></span>  <br/> |<span data-ttu-id="de5ac-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="de5ac-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="de5ac-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="de5ac-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="de5ac-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="de5ac-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="de5ac-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="de5ac-110">Called by:</span></span>  <br/> |<span data-ttu-id="de5ac-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="de5ac-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="de5ac-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="de5ac-112">Parameters</span></span>

 <span data-ttu-id="de5ac-113">_pВ таблице_</span><span class="sxs-lookup"><span data-stu-id="de5ac-113">_ptable_</span></span>
  
> <span data-ttu-id="de5ac-114">[in] Указатель в таблице MAPI, из которого извлекаются строк.</span><span class="sxs-lookup"><span data-stu-id="de5ac-114">[in] Pointer to the MAPI table from which rows are retrieved.</span></span> 
    
 <span data-ttu-id="de5ac-115">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="de5ac-115">_ptaga_</span></span>
  
> <span data-ttu-id="de5ac-116">[in] Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит массив свойство теги, указывающее столбцов таблицы.</span><span class="sxs-lookup"><span data-stu-id="de5ac-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating table columns.</span></span> <span data-ttu-id="de5ac-117">Эти теги используются для выбора определенных столбцов нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="de5ac-117">These tags are used to select the specific columns to be retrieved.</span></span> <span data-ttu-id="de5ac-118">Если параметр _ptaga_ имеет значение NULL, **HrQueryAllRows** получает набор целый столбец текущего представления таблицы, переданной в параметре _pВ таблице_ .</span><span class="sxs-lookup"><span data-stu-id="de5ac-118">If the  _ptaga_ parameter is NULL, **HrQueryAllRows** retrieves the entire column set of the current table view passed in the  _ptable_ parameter.</span></span> 
    
 <span data-ttu-id="de5ac-119">_веб-узла_</span><span class="sxs-lookup"><span data-stu-id="de5ac-119">_pres_</span></span>
  
> <span data-ttu-id="de5ac-120">[in] Указатель на структуру [SRestriction](srestriction.md) , содержащий извлечения ограничения.</span><span class="sxs-lookup"><span data-stu-id="de5ac-120">[in] Pointer to an [SRestriction](srestriction.md) structure that contains retrieval restrictions.</span></span> <span data-ttu-id="de5ac-121">Если параметр _веб-узла_ имеет значение NULL, **HrQueryAllRows** делает без ограничений.</span><span class="sxs-lookup"><span data-stu-id="de5ac-121">If the  _pres_ parameter is NULL, **HrQueryAllRows** makes no restrictions.</span></span> 
    
 <span data-ttu-id="de5ac-122">_параметров паролей_</span><span class="sxs-lookup"><span data-stu-id="de5ac-122">_psos_</span></span>
  
> <span data-ttu-id="de5ac-123">[in] Указатель на структуру [SSortOrderSet](ssortorderset.md) , определяющее порядок сортировки столбцов, нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="de5ac-123">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order of the columns to be retrieved.</span></span> <span data-ttu-id="de5ac-124">Если параметр _параметров паролей_ имеет значение NULL, используется порядок сортировки по умолчанию для таблицы.</span><span class="sxs-lookup"><span data-stu-id="de5ac-124">If the  _psos_ parameter is NULL, the default sort order for the table is used.</span></span> 
    
 <span data-ttu-id="de5ac-125">_crowsMax_</span><span class="sxs-lookup"><span data-stu-id="de5ac-125">_crowsMax_</span></span>
  
> <span data-ttu-id="de5ac-126">[in] Максимальное число строк нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="de5ac-126">[in] Maximum number of rows to be retrieved.</span></span> <span data-ttu-id="de5ac-127">Если значение параметра _crowsMax_ равно нулю, устанавливается без ограничения на число извлекаемых строк.</span><span class="sxs-lookup"><span data-stu-id="de5ac-127">If the value of the  _crowsMax_ parameter is zero, no limit on the number of rows retrieved is set.</span></span> 
    
 <span data-ttu-id="de5ac-128">_pprows_</span><span class="sxs-lookup"><span data-stu-id="de5ac-128">_pprows_</span></span>
  
> <span data-ttu-id="de5ac-129">[out] Указатель на указатель на структуру возвращенные [SRowSet](srowset.md) , который содержит массив указатели на строки извлеченных таблицы.</span><span class="sxs-lookup"><span data-stu-id="de5ac-129">[out] Pointer to a pointer to the returned [SRowSet](srowset.md) structure that contains an array of pointers to the retrieved table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="de5ac-130">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="de5ac-130">Return value</span></span>

<span data-ttu-id="de5ac-131">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="de5ac-131">S_OK</span></span> 
  
> <span data-ttu-id="de5ac-132">Вызов получить ожидаемый строк таблицы.</span><span class="sxs-lookup"><span data-stu-id="de5ac-132">The call retrieved the expected rows of a table.</span></span> 
    
<span data-ttu-id="de5ac-133">MAPI_E_TABLE_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="de5ac-133">MAPI_E_TABLE_TOO_BIG</span></span> 
  
> <span data-ttu-id="de5ac-134">Количество строк в таблице больше, чем значение, переданное для параметра _crowsMax_ .</span><span class="sxs-lookup"><span data-stu-id="de5ac-134">The number of rows in the table is larger than the number passed for the  _crowsMax_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="de5ac-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="de5ac-135">Remarks</span></span>

<span data-ttu-id="de5ac-136">Клиентское приложение или поставщик услуг не контролирует число строк, **HrQueryAllRows** пытается получить, отличное от, поскольку ограничение указывает параметр _веб-узла_ .</span><span class="sxs-lookup"><span data-stu-id="de5ac-136">A client application or service provider has no control over the number of rows **HrQueryAllRows** attempts to retrieve, other than by imposing a restriction pointed to by the  _pres_ parameter.</span></span> <span data-ttu-id="de5ac-137">Параметр _crowsMax_ не ограничивают извлечения на определенное количество строк в таблице, но вместо определяет максимальный объем памяти для хранения всех извлеченных строк.</span><span class="sxs-lookup"><span data-stu-id="de5ac-137">The  _crowsMax_ parameter does not limit the retrieval to a certain number of table rows, but rather defines a maximum amount of memory available to hold all retrieved rows.</span></span> <span data-ttu-id="de5ac-138">Только защиту от переполнения большой объем памяти — возможность временное, предоставленные параметру _crowsMax_.</span><span class="sxs-lookup"><span data-stu-id="de5ac-138">The only protection against massive memory overflow is the stopgap feature provided by setting  _crowsMax_.</span></span> <span data-ttu-id="de5ac-139">Возвращение ошибки MAPI_E_TABLE_TOO_BIG означает таблицы содержит слишком много строк, в течение которого будут храниться за один раз в памяти.</span><span class="sxs-lookup"><span data-stu-id="de5ac-139">The error return MAPI_E_TABLE_TOO_BIG means the table contains too many rows to be held all at once in memory.</span></span> 
  
<span data-ttu-id="de5ac-140">Таблицы, которые обычно небольшие, например таблицы хранилища сообщений или таблицы поставщика, обычно можно безопасно извлечь с **HrQueryAllRows**.</span><span class="sxs-lookup"><span data-stu-id="de5ac-140">Tables that are typically small, such as a message store table or a provider table, usually can be safely retrieved with **HrQueryAllRows**.</span></span> <span data-ttu-id="de5ac-141">Таблицы риску большим, таких как содержимое таблицы или даже таблица получателей, следует обращаться в подразделах, с помощью метода [IMAPITable::QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="de5ac-141">Tables at risk of being very large, such as a contents table or even a recipients table, should be traversed in subsections using the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> 
  
<span data-ttu-id="de5ac-142">Если при вызове **HrQueryAllRows** любого свойства таблицы не определены, они возвращаются с типом свойства PT_NULL и идентификатор свойства PROP_ID_NULL</span><span class="sxs-lookup"><span data-stu-id="de5ac-142">If any table properties are undefined when **HrQueryAllRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL</span></span> 
  

