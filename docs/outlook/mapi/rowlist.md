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
ms.openlocfilehash: d0427e36d07d1cdc4f88e471f9ca006e737b73f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812164"
---
# <a name="rowlist"></a><span data-ttu-id="76559-103">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="76559-103">ROWLIST</span></span>

  
  
<span data-ttu-id="76559-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76559-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76559-105">Содержит массив структур [ROWENTRY](rowentry.md) , представляющее строк и операции, выполняемые на соответствующие строки в таблице через интерфейс [IExchangeModifyTable](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="76559-105">Contains an array of [ROWENTRY](rowentry.md) structures representing rows and the operations that are performed on those rows in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a><span data-ttu-id="76559-106">Members</span><span class="sxs-lookup"><span data-stu-id="76559-106">Members</span></span>

 <span data-ttu-id="76559-107">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="76559-107">**cEntries**</span></span>
  
> <span data-ttu-id="76559-108">Число записей в массива, указанного параметром члена **aEntries** .</span><span class="sxs-lookup"><span data-stu-id="76559-108">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
 <span data-ttu-id="76559-109">**aEntries [MAPI_DIM]**</span><span class="sxs-lookup"><span data-stu-id="76559-109">**aEntries[MAPI_DIM]**</span></span>
  
> <span data-ttu-id="76559-110">Массив структур **ROWENTRY** , содержащий строки и операции, выполняемые на соответствующие строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="76559-110">Array of **ROWENTRY** structures that contains the rows and the operations that are performed on those rows in the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="76559-111">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="76559-111">MFCMAPI reference</span></span>

<span data-ttu-id="76559-112">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="76559-112">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="76559-113">**����**</span><span class="sxs-lookup"><span data-stu-id="76559-113">**File**</span></span>|<span data-ttu-id="76559-114">**�������**</span><span class="sxs-lookup"><span data-stu-id="76559-114">**Function**</span></span>|<span data-ttu-id="76559-115">**�����������**</span><span class="sxs-lookup"><span data-stu-id="76559-115">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="76559-116">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="76559-116">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="76559-117">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="76559-117">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="76559-118">Используются для формирования список выбранных правил для последующих действий **ModifyTable** .</span><span class="sxs-lookup"><span data-stu-id="76559-118">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="76559-119">См. также</span><span class="sxs-lookup"><span data-stu-id="76559-119">See also</span></span>



[<span data-ttu-id="76559-120">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="76559-120">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="76559-121">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="76559-121">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="76559-122">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="76559-122">MAPI Structures</span></span>](mapi-structures.md)

