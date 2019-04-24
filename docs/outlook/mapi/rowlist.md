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
ms.openlocfilehash: c13b741b1e0ddfd964b9325d736a26dac4bff2af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346300"
---
# <a name="rowlist"></a><span data-ttu-id="44525-103">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="44525-103">ROWLIST</span></span>

  
  
<span data-ttu-id="44525-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44525-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44525-105">Содержит массив структур [ровентри](rowentry.md) , представляющих строки, и операции, выполняемые над этими строками в таблице через интерфейс [иексчанжемодифитабле](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="44525-105">Contains an array of [ROWENTRY](rowentry.md) structures representing rows and the operations that are performed on those rows in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a><span data-ttu-id="44525-106">Members</span><span class="sxs-lookup"><span data-stu-id="44525-106">Members</span></span>

 <span data-ttu-id="44525-107">**Центриес**</span><span class="sxs-lookup"><span data-stu-id="44525-107">**cEntries**</span></span>
  
> <span data-ttu-id="44525-108">Количество записей в массиве, указанном элементом **аентриес** .</span><span class="sxs-lookup"><span data-stu-id="44525-108">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
 <span data-ttu-id="44525-109">**Аентриес [МАПИ_ДИМ]**</span><span class="sxs-lookup"><span data-stu-id="44525-109">**aEntries[MAPI_DIM]**</span></span>
  
> <span data-ttu-id="44525-110">Массив структур **ровентри** , который содержит строки и операции, выполняемые над этими строками в таблице.</span><span class="sxs-lookup"><span data-stu-id="44525-110">Array of **ROWENTRY** structures that contains the rows and the operations that are performed on those rows in the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="44525-111">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="44525-111">MFCMAPI reference</span></span>

<span data-ttu-id="44525-112">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="44525-112">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="44525-113">**Файл**</span><span class="sxs-lookup"><span data-stu-id="44525-113">**File**</span></span>|<span data-ttu-id="44525-114">**Функция**</span><span class="sxs-lookup"><span data-stu-id="44525-114">**Function**</span></span>|<span data-ttu-id="44525-115">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="44525-115">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="44525-116">Рулесдлг. cpp</span><span class="sxs-lookup"><span data-stu-id="44525-116">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="44525-117">Крулесдлг:: Жетселектедитемс</span><span class="sxs-lookup"><span data-stu-id="44525-117">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="44525-118">Используется для создания списка выбранных правил для последующих действий **модифитабле** .</span><span class="sxs-lookup"><span data-stu-id="44525-118">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44525-119">См. также</span><span class="sxs-lookup"><span data-stu-id="44525-119">See also</span></span>



[<span data-ttu-id="44525-120">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="44525-120">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="44525-121">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="44525-121">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="44525-122">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="44525-122">MAPI Structures</span></span>](mapi-structures.md)

