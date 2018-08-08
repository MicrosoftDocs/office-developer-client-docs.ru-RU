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
ms.openlocfilehash: 9e7f24fb4b444f63b6277d1844a7948f5ab0c590
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808807"
---
# <a name="iexchangemodifytablemodifytable"></a><span data-ttu-id="c7244-103">IExchangeModifyTable::ModifyTable</span><span class="sxs-lookup"><span data-stu-id="c7244-103">IExchangeModifyTable::ModifyTable</span></span>

  
  
<span data-ttu-id="c7244-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c7244-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c7244-105">Обновляет объект таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="c7244-105">Updates a MAPI table object.</span></span>
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a><span data-ttu-id="c7244-106">���������</span><span class="sxs-lookup"><span data-stu-id="c7244-106">Parameters</span></span>

 <span data-ttu-id="c7244-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c7244-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c7244-108">[in] Используйте один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="c7244-108">[in] Use one of the following values:</span></span> 
    
<span data-ttu-id="c7244-109">нуль (0)</span><span class="sxs-lookup"><span data-stu-id="c7244-109">0 (zero)</span></span>
  
> <span data-ttu-id="c7244-110">Используйте значение член **ulRowFlags** структуры [ROWENTRY](rowentry.md) .</span><span class="sxs-lookup"><span data-stu-id="c7244-110">Use the value of the **ulRowFlags** member of the [ROWENTRY](rowentry.md) structure.</span></span> 
    
<span data-ttu-id="c7244-111">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="c7244-111">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="c7244-112">Задает новый правами.</span><span class="sxs-lookup"><span data-stu-id="c7244-112">Sets new rights.</span></span>
    
<span data-ttu-id="c7244-113">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="c7244-113">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="c7244-114">При передаче ACLTABLE_FREEBUSY предоставляет подробное отображение новые права сведениям о доступности.</span><span class="sxs-lookup"><span data-stu-id="c7244-114">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="c7244-115">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="c7244-115">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="c7244-116">При передаче ACLTABLE_FREEBUSY предоставляет простого отображения новые права сведениям о доступности.</span><span class="sxs-lookup"><span data-stu-id="c7244-116">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
<span data-ttu-id="c7244-117">ROWLIST_REPLACE</span><span class="sxs-lookup"><span data-stu-id="c7244-117">ROWLIST_REPLACE</span></span>
  
> <span data-ttu-id="c7244-118">Замените все строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="c7244-118">Replace all the rows in the table.</span></span>
    
 <span data-ttu-id="c7244-119">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="c7244-119">_lpMods_</span></span>
  
> <span data-ttu-id="c7244-120">[in] Указывает на [ROWLIST](rowlist.md) структура, содержащая свойства для объекта в таблице.</span><span class="sxs-lookup"><span data-stu-id="c7244-120">[in] Points to a [ROWLIST](rowlist.md) structure containing the properties for the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="c7244-121">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="c7244-121">MFCMAPI reference</span></span>

<span data-ttu-id="c7244-122">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="c7244-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c7244-123">**����**</span><span class="sxs-lookup"><span data-stu-id="c7244-123">**File**</span></span>|<span data-ttu-id="c7244-124">**�������**</span><span class="sxs-lookup"><span data-stu-id="c7244-124">**Function**</span></span>|<span data-ttu-id="c7244-125">**�����������**</span><span class="sxs-lookup"><span data-stu-id="c7244-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c7244-126">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c7244-126">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="c7244-127">CRulesDlg::OnModifySelectedItem</span><span class="sxs-lookup"><span data-stu-id="c7244-127">CRulesDlg::OnModifySelectedItem</span></span>  <br/> |<span data-ttu-id="c7244-128">Mfcmapi (en) использует метод **IExchangeModifyTable::ModifyTable** для обратной записи измененные правила в таблице правил.</span><span class="sxs-lookup"><span data-stu-id="c7244-128">MFCMAPI uses the **IExchangeModifyTable::ModifyTable** method to write a modified rule back to the table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7244-129">См. также</span><span class="sxs-lookup"><span data-stu-id="c7244-129">See also</span></span>



[<span data-ttu-id="c7244-130">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c7244-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="c7244-131">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="c7244-131">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="c7244-132">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="c7244-132">ROWLIST</span></span>](rowlist.md)


[<span data-ttu-id="c7244-133">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="c7244-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

