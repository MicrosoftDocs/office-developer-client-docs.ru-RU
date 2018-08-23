---
title: ROWLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWLIST
api_type:
- COM
ms.assetid: ce0be0d5-4962-4d53-828f-c93d1c5aae32
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4cbaf08c58a98be45ad33aebb8f230fb53c234f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577662"
---
# <a name="rowlist"></a><span data-ttu-id="dca49-103">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="dca49-103">ROWLIST</span></span>

  
  
<span data-ttu-id="dca49-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dca49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dca49-105">Содержит массив структур [ROWENTRY](rowentry.md) , представляющее строк и операции, выполняемые на соответствующие строки в таблице через интерфейс [IExchangeModifyTable](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="dca49-105">Contains an array of [ROWENTRY](rowentry.md) structures representing rows and the operations that are performed on those rows in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a><span data-ttu-id="dca49-106">Members</span><span class="sxs-lookup"><span data-stu-id="dca49-106">Members</span></span>

 <span data-ttu-id="dca49-107">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="dca49-107">**cEntries**</span></span>
  
> <span data-ttu-id="dca49-108">Число записей в массива, указанного параметром члена **aEntries** .</span><span class="sxs-lookup"><span data-stu-id="dca49-108">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
 <span data-ttu-id="dca49-109">**aEntries [MAPI_DIM]**</span><span class="sxs-lookup"><span data-stu-id="dca49-109">**aEntries[MAPI_DIM]**</span></span>
  
> <span data-ttu-id="dca49-110">Массив структур **ROWENTRY** , содержащий строки и операции, выполняемые на соответствующие строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="dca49-110">Array of **ROWENTRY** structures that contains the rows and the operations that are performed on those rows in the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="dca49-111">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="dca49-111">MFCMAPI reference</span></span>

<span data-ttu-id="dca49-112">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="dca49-112">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dca49-113">**����**</span><span class="sxs-lookup"><span data-stu-id="dca49-113">**File**</span></span>|<span data-ttu-id="dca49-114">**�������**</span><span class="sxs-lookup"><span data-stu-id="dca49-114">**Function**</span></span>|<span data-ttu-id="dca49-115">**�����������**</span><span class="sxs-lookup"><span data-stu-id="dca49-115">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dca49-116">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="dca49-116">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="dca49-117">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="dca49-117">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="dca49-118">Используются для формирования список выбранных правил для последующих действий **ModifyTable** .</span><span class="sxs-lookup"><span data-stu-id="dca49-118">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dca49-119">См. также</span><span class="sxs-lookup"><span data-stu-id="dca49-119">See also</span></span>



[<span data-ttu-id="dca49-120">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="dca49-120">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="dca49-121">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dca49-121">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="dca49-122">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="dca49-122">MAPI Structures</span></span>](mapi-structures.md)

