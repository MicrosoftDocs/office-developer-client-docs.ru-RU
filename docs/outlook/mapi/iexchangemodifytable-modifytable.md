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
ms.openlocfilehash: b801bdc06317738448a2205b60b94e1c9707d4f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565909"
---
# <a name="iexchangemodifytablemodifytable"></a><span data-ttu-id="62f16-103">IExchangeModifyTable::ModifyTable</span><span class="sxs-lookup"><span data-stu-id="62f16-103">IExchangeModifyTable::ModifyTable</span></span>

  
  
<span data-ttu-id="62f16-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62f16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62f16-105">Обновляет объект таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="62f16-105">Updates a MAPI table object.</span></span>
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a><span data-ttu-id="62f16-106">���������</span><span class="sxs-lookup"><span data-stu-id="62f16-106">Parameters</span></span>

 <span data-ttu-id="62f16-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="62f16-107">_ulFlags_</span></span>
  
> <span data-ttu-id="62f16-108">[in] Используйте один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="62f16-108">[in] Use one of the following values:</span></span> 
    
<span data-ttu-id="62f16-109">нуль (0)</span><span class="sxs-lookup"><span data-stu-id="62f16-109">0 (zero)</span></span>
  
> <span data-ttu-id="62f16-110">Используйте значение член **ulRowFlags** структуры [ROWENTRY](rowentry.md) .</span><span class="sxs-lookup"><span data-stu-id="62f16-110">Use the value of the **ulRowFlags** member of the [ROWENTRY](rowentry.md) structure.</span></span> 
    
<span data-ttu-id="62f16-111">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="62f16-111">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="62f16-112">Задает новый правами.</span><span class="sxs-lookup"><span data-stu-id="62f16-112">Sets new rights.</span></span>
    
<span data-ttu-id="62f16-113">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="62f16-113">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="62f16-114">При передаче ACLTABLE_FREEBUSY предоставляет подробное отображение новые права сведениям о доступности.</span><span class="sxs-lookup"><span data-stu-id="62f16-114">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="62f16-115">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="62f16-115">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="62f16-116">При передаче ACLTABLE_FREEBUSY предоставляет простого отображения новые права сведениям о доступности.</span><span class="sxs-lookup"><span data-stu-id="62f16-116">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
<span data-ttu-id="62f16-117">ROWLIST_REPLACE</span><span class="sxs-lookup"><span data-stu-id="62f16-117">ROWLIST_REPLACE</span></span>
  
> <span data-ttu-id="62f16-118">Замените все строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="62f16-118">Replace all the rows in the table.</span></span>
    
 <span data-ttu-id="62f16-119">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="62f16-119">_lpMods_</span></span>
  
> <span data-ttu-id="62f16-120">[in] Указывает на [ROWLIST](rowlist.md) структура, содержащая свойства для объекта в таблице.</span><span class="sxs-lookup"><span data-stu-id="62f16-120">[in] Points to a [ROWLIST](rowlist.md) structure containing the properties for the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="62f16-121">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="62f16-121">MFCMAPI reference</span></span>

<span data-ttu-id="62f16-122">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="62f16-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="62f16-123">**Файл**</span><span class="sxs-lookup"><span data-stu-id="62f16-123">**File**</span></span>|<span data-ttu-id="62f16-124">**Функция**</span><span class="sxs-lookup"><span data-stu-id="62f16-124">**Function**</span></span>|<span data-ttu-id="62f16-125">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="62f16-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="62f16-126">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="62f16-126">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="62f16-127">CRulesDlg::OnModifySelectedItem</span><span class="sxs-lookup"><span data-stu-id="62f16-127">CRulesDlg::OnModifySelectedItem</span></span>  <br/> |<span data-ttu-id="62f16-128">Mfcmapi (en) использует метод **IExchangeModifyTable::ModifyTable** для обратной записи измененные правила в таблице правил.</span><span class="sxs-lookup"><span data-stu-id="62f16-128">MFCMAPI uses the **IExchangeModifyTable::ModifyTable** method to write a modified rule back to the table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="62f16-129">См. также</span><span class="sxs-lookup"><span data-stu-id="62f16-129">See also</span></span>



[<span data-ttu-id="62f16-130">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="62f16-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="62f16-131">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="62f16-131">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="62f16-132">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="62f16-132">ROWLIST</span></span>](rowlist.md)


[<span data-ttu-id="62f16-133">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="62f16-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

