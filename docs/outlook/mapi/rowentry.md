---
title: ROWENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWENTRY
api_type:
- COM
ms.assetid: bd6c0d8e-68cc-4d60-9029-13ed81c816cd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f8ac73b1977886208290285fec2d1bd0de1b4f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812166"
---
# <a name="rowentry"></a><span data-ttu-id="3f4a8-103">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="3f4a8-103">ROWENTRY</span></span>

<span data-ttu-id="3f4a8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3f4a8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3f4a8-105">Содержит строку и операцию, выполняемую с этой строки в таблице через интерфейс [IExchangeModifyTable](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="3f4a8-105">Contains a row and the operation that is performed on that row in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a><span data-ttu-id="3f4a8-106">Members</span><span class="sxs-lookup"><span data-stu-id="3f4a8-106">Members</span></span>

<span data-ttu-id="3f4a8-107">**ulRowFlags**</span><span class="sxs-lookup"><span data-stu-id="3f4a8-107">**ulRowFlags**</span></span>
  
> <span data-ttu-id="3f4a8-108">Один из следующих операций выполняется на данные.</span><span class="sxs-lookup"><span data-stu-id="3f4a8-108">One of the following operations to be performed on the data:</span></span> 
    
  - <span data-ttu-id="3f4a8-109">ROW_ADD: Добавление данных в таблицу как новую строку.</span><span class="sxs-lookup"><span data-stu-id="3f4a8-109">ROW_ADD: Add the data to the table as a new row.</span></span>
      
  - <span data-ttu-id="3f4a8-110">ROW_MODIFY: Изменение этой строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="3f4a8-110">ROW_MODIFY: Modify this row in the table.</span></span>
      
  - <span data-ttu-id="3f4a8-111">ROW_REMOVE: Удаление этой строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="3f4a8-111">ROW_REMOVE: Remove this row from the table.</span></span>
      
  - <span data-ttu-id="3f4a8-112">ROW_EMPTY: Не добавляйте строку данных в таблицу.</span><span class="sxs-lookup"><span data-stu-id="3f4a8-112">ROW_EMPTY: Do not add the row data to the table.</span></span> <span data-ttu-id="3f4a8-113">(Строка является пустым.)</span><span class="sxs-lookup"><span data-stu-id="3f4a8-113">(The row is empty.)</span></span>
    
<span data-ttu-id="3f4a8-114">**cValues**</span><span class="sxs-lookup"><span data-stu-id="3f4a8-114">**cValues**</span></span>
  
> <span data-ttu-id="3f4a8-115">Количество значений свойств в **rgPropvals**.</span><span class="sxs-lookup"><span data-stu-id="3f4a8-115">The number of property values in **rgPropvals**.</span></span>
    
<span data-ttu-id="3f4a8-116">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="3f4a8-116">**rgPropVals**</span></span>
  
> <span data-ttu-id="3f4a8-117">Массив структур [SPropValue](spropvalue.md) , представляющих значения столбцов для вставки в таблице.</span><span class="sxs-lookup"><span data-stu-id="3f4a8-117">An array of [SPropValue](spropvalue.md) structures representing the columns values to be inserted into the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="3f4a8-118">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="3f4a8-118">MFCMAPI reference</span></span>

<span data-ttu-id="3f4a8-119">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="3f4a8-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3f4a8-120">**����**</span><span class="sxs-lookup"><span data-stu-id="3f4a8-120">**File**</span></span>|<span data-ttu-id="3f4a8-121">**�������**</span><span class="sxs-lookup"><span data-stu-id="3f4a8-121">**Function**</span></span>|<span data-ttu-id="3f4a8-122">**�����������**</span><span class="sxs-lookup"><span data-stu-id="3f4a8-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3f4a8-123">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="3f4a8-123">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="3f4a8-124">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="3f4a8-124">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="3f4a8-125">Используются для формирования список выбранных правил для последующих действий **ModifyTable** .</span><span class="sxs-lookup"><span data-stu-id="3f4a8-125">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f4a8-126">См. также</span><span class="sxs-lookup"><span data-stu-id="3f4a8-126">See also</span></span>
  
- [<span data-ttu-id="3f4a8-127">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f4a8-127">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
- [<span data-ttu-id="3f4a8-128">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="3f4a8-128">MAPI Structures</span></span>](mapi-structures.md)

