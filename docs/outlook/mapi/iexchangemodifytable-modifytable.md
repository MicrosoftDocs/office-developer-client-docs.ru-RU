---
title: IExchangeModifyTableModifyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.ModifyTable
api_type:
- COM
ms.assetid: b9a745cc-260d-4a1c-896e-6a038ab3cfb9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 46bb9b2cc1a4d54807d6929b4e1439b58fb3a531
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418178"
---
# <a name="iexchangemodifytablemodifytable"></a><span data-ttu-id="2239a-103">IExchangeModifyTable::ModifyTable</span><span class="sxs-lookup"><span data-stu-id="2239a-103">IExchangeModifyTable::ModifyTable</span></span>

  
  
<span data-ttu-id="2239a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2239a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2239a-105">Обновляет объект таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="2239a-105">Updates a MAPI table object.</span></span>
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a><span data-ttu-id="2239a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2239a-106">Parameters</span></span>

 <span data-ttu-id="2239a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2239a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2239a-108">[in] Используйте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="2239a-108">[in] Use one of the following values:</span></span> 
    
<span data-ttu-id="2239a-109">0 (ноль)</span><span class="sxs-lookup"><span data-stu-id="2239a-109">0 (zero)</span></span>
  
> <span data-ttu-id="2239a-110">Используйте значение члена **ulRowFlags** структуры [ROWENTRY.](rowentry.md)</span><span class="sxs-lookup"><span data-stu-id="2239a-110">Use the value of the **ulRowFlags** member of the [ROWENTRY](rowentry.md) structure.</span></span> 
    
<span data-ttu-id="2239a-111">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="2239a-111">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="2239a-112">Задает новые права.</span><span class="sxs-lookup"><span data-stu-id="2239a-112">Sets new rights.</span></span>
    
<span data-ttu-id="2239a-113">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="2239a-113">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="2239a-114">При ACLTABLE_FREEBUSY предоставляет подробные сведения о новых правах на сведения о занятости.</span><span class="sxs-lookup"><span data-stu-id="2239a-114">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="2239a-115">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="2239a-115">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="2239a-116">При ACLTABLE_FREEBUSY данные отображаются новые права занятости.</span><span class="sxs-lookup"><span data-stu-id="2239a-116">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
<span data-ttu-id="2239a-117">ROWLIST_REPLACE</span><span class="sxs-lookup"><span data-stu-id="2239a-117">ROWLIST_REPLACE</span></span>
  
> <span data-ttu-id="2239a-118">Замените все строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="2239a-118">Replace all the rows in the table.</span></span>
    
 <span data-ttu-id="2239a-119">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="2239a-119">_lpMods_</span></span>
  
> <span data-ttu-id="2239a-120">[in] Указывает на [структуру ROWLIST,](rowlist.md) содержащую свойства объекта таблицы.</span><span class="sxs-lookup"><span data-stu-id="2239a-120">[in] Points to a [ROWLIST](rowlist.md) structure containing the properties for the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="2239a-121">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2239a-121">MFCMAPI reference</span></span>

<span data-ttu-id="2239a-122">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="2239a-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2239a-123">**Файл**</span><span class="sxs-lookup"><span data-stu-id="2239a-123">**File**</span></span>|<span data-ttu-id="2239a-124">**Функция**</span><span class="sxs-lookup"><span data-stu-id="2239a-124">**Function**</span></span>|<span data-ttu-id="2239a-125">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="2239a-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2239a-126">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="2239a-126">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="2239a-127">CRulesDlg::OnModifySelectedItem</span><span class="sxs-lookup"><span data-stu-id="2239a-127">CRulesDlg::OnModifySelectedItem</span></span>  <br/> |<span data-ttu-id="2239a-128">MFCMAPI использует метод **IExchangeModifyTable::ModifyTable** для записи измененного правила обратно в таблицу правил.</span><span class="sxs-lookup"><span data-stu-id="2239a-128">MFCMAPI uses the **IExchangeModifyTable::ModifyTable** method to write a modified rule back to the table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2239a-129">См. также</span><span class="sxs-lookup"><span data-stu-id="2239a-129">See also</span></span>



[<span data-ttu-id="2239a-130">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2239a-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="2239a-131">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="2239a-131">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="2239a-132">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="2239a-132">ROWLIST</span></span>](rowlist.md)


[<span data-ttu-id="2239a-133">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="2239a-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

