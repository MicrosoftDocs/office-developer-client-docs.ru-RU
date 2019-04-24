---
title: Иексчанжемодифитаблежеттабле
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336619"
---
# <a name="iexchangemodifytablegettable"></a><span data-ttu-id="7d50e-103">IExchangeModifyTable::GetTable</span><span class="sxs-lookup"><span data-stu-id="7d50e-103">IExchangeModifyTable::GetTable</span></span>

  
  
<span data-ttu-id="7d50e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d50e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d50e-105">Возвращает указатель на интерфейс для объекта таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="7d50e-105">Returns a pointer to an interface for a MAPI table object.</span></span>
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a><span data-ttu-id="7d50e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d50e-106">Parameters</span></span>

 <span data-ttu-id="7d50e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7d50e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7d50e-108">возврата Резервирования должен иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="7d50e-108">[in] Reserved; must be 0 (zero).</span></span>
    
<span data-ttu-id="7d50e-109">АКЛТАБЛЕ_ФРИБУСИ</span><span class="sxs-lookup"><span data-stu-id="7d50e-109">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="7d50e-110">Задает новые права.</span><span class="sxs-lookup"><span data-stu-id="7d50e-110">Sets new rights.</span></span>
    
<span data-ttu-id="7d50e-111">Фригхтсфрибусидетаилед</span><span class="sxs-lookup"><span data-stu-id="7d50e-111">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="7d50e-112">Когда АКЛТАБЛЕ_ФРИБУСИ передается, вы можете просмотреть подробные сведения о новых правах на сведения о доступности.</span><span class="sxs-lookup"><span data-stu-id="7d50e-112">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="7d50e-113">Фригхтсфрибусисимпле</span><span class="sxs-lookup"><span data-stu-id="7d50e-113">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="7d50e-114">Когда АКЛТАБЛЕ_ФРИБУСИ передается, вы можете легко отобразить новые права на доступ к сведениям о доступности.</span><span class="sxs-lookup"><span data-stu-id="7d50e-114">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
 <span data-ttu-id="7d50e-115">_Лпптабле_</span><span class="sxs-lookup"><span data-stu-id="7d50e-115">_lppTable_</span></span>
  
> <span data-ttu-id="7d50e-116">вышли Указывает на [IMAPITable: интерфейс IUnknown](imapitableiunknown.md) , содержащий объект Table.</span><span class="sxs-lookup"><span data-stu-id="7d50e-116">[out] Points to a [IMAPITable : IUnknown](imapitableiunknown.md) interface containing the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="7d50e-117">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7d50e-117">MFCMAPI reference</span></span>

<span data-ttu-id="7d50e-118">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="7d50e-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7d50e-119">**Файл**</span><span class="sxs-lookup"><span data-stu-id="7d50e-119">**File**</span></span>|<span data-ttu-id="7d50e-120">**Функция**</span><span class="sxs-lookup"><span data-stu-id="7d50e-120">**Function**</span></span>|<span data-ttu-id="7d50e-121">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="7d50e-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7d50e-122">Рулесдлг. cpp</span><span class="sxs-lookup"><span data-stu-id="7d50e-122">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="7d50e-123">Крулесдлг:: Онрефрешвиев</span><span class="sxs-lookup"><span data-stu-id="7d50e-123">CRulesDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="7d50e-124">MFCMAPI использует метод **иексчанжемодифитабле:: table** для получения таблицы правил.</span><span class="sxs-lookup"><span data-stu-id="7d50e-124">MFCMAPI uses the **IExchangeModifyTable::GetTable** method to get a table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d50e-125">См. также</span><span class="sxs-lookup"><span data-stu-id="7d50e-125">See also</span></span>



[<span data-ttu-id="7d50e-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d50e-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="7d50e-127">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="7d50e-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

