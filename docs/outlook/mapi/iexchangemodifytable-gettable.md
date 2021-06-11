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
ms.openlocfilehash: 87c60f424e08eea011bb643041196ca9445a3aa1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436246"
---
# <a name="iexchangemodifytablegettable"></a><span data-ttu-id="e1cc2-103">IExchangeModifyTable::GetTable</span><span class="sxs-lookup"><span data-stu-id="e1cc2-103">IExchangeModifyTable::GetTable</span></span>

  
  
<span data-ttu-id="e1cc2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1cc2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1cc2-105">Возвращает указатель в интерфейс для объекта таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="e1cc2-105">Returns a pointer to an interface for a MAPI table object.</span></span>
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a><span data-ttu-id="e1cc2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e1cc2-106">Parameters</span></span>

 <span data-ttu-id="e1cc2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e1cc2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e1cc2-108">[in] Зарезервировано; должно быть 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="e1cc2-108">[in] Reserved; must be 0 (zero).</span></span>
    
<span data-ttu-id="e1cc2-109">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="e1cc2-109">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="e1cc2-110">Задает новые права.</span><span class="sxs-lookup"><span data-stu-id="e1cc2-110">Sets new rights.</span></span>
    
<span data-ttu-id="e1cc2-111">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="e1cc2-111">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="e1cc2-112">При ACLTABLE_FREEBUSY вы можете подробно отображать новые права на свободный и занятый доступ.</span><span class="sxs-lookup"><span data-stu-id="e1cc2-112">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="e1cc2-113">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="e1cc2-113">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="e1cc2-114">При ACLTABLE_FREEBUSY вы можете просто отображать новые свободные и занятые права.</span><span class="sxs-lookup"><span data-stu-id="e1cc2-114">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
 <span data-ttu-id="e1cc2-115">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="e1cc2-115">_lppTable_</span></span>
  
> <span data-ttu-id="e1cc2-116">[вышел] Указывает на [интерфейс IMAPITable : IUnknown,](imapitableiunknown.md) содержащий объект таблицы.</span><span class="sxs-lookup"><span data-stu-id="e1cc2-116">[out] Points to a [IMAPITable : IUnknown](imapitableiunknown.md) interface containing the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="e1cc2-117">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e1cc2-117">MFCMAPI reference</span></span>

<span data-ttu-id="e1cc2-118">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="e1cc2-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e1cc2-119">**Файл**</span><span class="sxs-lookup"><span data-stu-id="e1cc2-119">**File**</span></span>|<span data-ttu-id="e1cc2-120">**Функция**</span><span class="sxs-lookup"><span data-stu-id="e1cc2-120">**Function**</span></span>|<span data-ttu-id="e1cc2-121">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="e1cc2-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e1cc2-122">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="e1cc2-122">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="e1cc2-123">CRulesDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="e1cc2-123">CRulesDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="e1cc2-124">MFCMAPI использует **метод IExchangeModifyTable::GetTable** для получения таблицы правил.</span><span class="sxs-lookup"><span data-stu-id="e1cc2-124">MFCMAPI uses the **IExchangeModifyTable::GetTable** method to get a table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1cc2-125">См. также</span><span class="sxs-lookup"><span data-stu-id="e1cc2-125">See also</span></span>



[<span data-ttu-id="e1cc2-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e1cc2-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="e1cc2-127">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="e1cc2-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

