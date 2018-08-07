---
title: IExchangeModifyTableGetTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetTable
api_type:
- COM
ms.assetid: 97df32c4-07c6-41f1-84e7-c6e87d396e34
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0cf9373c68d533908b857a4d8f1c0e71aa11846f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808819"
---
# <a name="iexchangemodifytablegettable"></a><span data-ttu-id="69a51-103">IExchangeModifyTable::GetTable</span><span class="sxs-lookup"><span data-stu-id="69a51-103">IExchangeModifyTable::GetTable</span></span>

  
  
<span data-ttu-id="69a51-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="69a51-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="69a51-105">Возвращает указатель на интерфейс для объекта таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="69a51-105">Returns a pointer to an interface for a MAPI table object.</span></span>
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a><span data-ttu-id="69a51-106">���������</span><span class="sxs-lookup"><span data-stu-id="69a51-106">Parameters</span></span>

 <span data-ttu-id="69a51-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="69a51-107">_ulFlags_</span></span>
  
> <span data-ttu-id="69a51-108">[in] Зарезервировано; должен иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="69a51-108">[in] Reserved; must be 0 (zero).</span></span>
    
<span data-ttu-id="69a51-109">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="69a51-109">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="69a51-110">Задает новый правами.</span><span class="sxs-lookup"><span data-stu-id="69a51-110">Sets new rights.</span></span>
    
<span data-ttu-id="69a51-111">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="69a51-111">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="69a51-112">При передаче ACLTABLE_FREEBUSY предоставляет подробное отображение новые права сведениям о доступности.</span><span class="sxs-lookup"><span data-stu-id="69a51-112">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="69a51-113">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="69a51-113">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="69a51-114">При передаче ACLTABLE_FREEBUSY предоставляет простого отображения новые права сведениям о доступности.</span><span class="sxs-lookup"><span data-stu-id="69a51-114">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
 <span data-ttu-id="69a51-115">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="69a51-115">_lppTable_</span></span>
  
> <span data-ttu-id="69a51-116">[out] Указывает на [IMAPITable: IUnknown](imapitableiunknown.md) интерфейс, содержащий объект таблицы.</span><span class="sxs-lookup"><span data-stu-id="69a51-116">[out] Points to a [IMAPITable : IUnknown](imapitableiunknown.md) interface containing the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="69a51-117">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="69a51-117">MFCMAPI reference</span></span>

<span data-ttu-id="69a51-118">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="69a51-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="69a51-119">**����**</span><span class="sxs-lookup"><span data-stu-id="69a51-119">**File**</span></span>|<span data-ttu-id="69a51-120">**�������**</span><span class="sxs-lookup"><span data-stu-id="69a51-120">**Function**</span></span>|<span data-ttu-id="69a51-121">**�����������**</span><span class="sxs-lookup"><span data-stu-id="69a51-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="69a51-122">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="69a51-122">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="69a51-123">CRulesDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="69a51-123">CRulesDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="69a51-124">Mfcmapi (en) использует метод **IExchangeModifyTable::GetTable** для получения таблицы правил.</span><span class="sxs-lookup"><span data-stu-id="69a51-124">MFCMAPI uses the **IExchangeModifyTable::GetTable** method to get a table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69a51-125">См. также</span><span class="sxs-lookup"><span data-stu-id="69a51-125">See also</span></span>



[<span data-ttu-id="69a51-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="69a51-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="69a51-127">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="69a51-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

