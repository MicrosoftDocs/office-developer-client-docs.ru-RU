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
ms.openlocfilehash: fb0bfaba1ca0a0d7d34096b3b0b1db9863207097
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576269"
---
# <a name="rowentry"></a><span data-ttu-id="bf2c9-103">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="bf2c9-103">ROWENTRY</span></span>

<span data-ttu-id="bf2c9-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf2c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf2c9-105">Содержит строку и операцию, выполняемую с этой строки в таблице через интерфейс [IExchangeModifyTable](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="bf2c9-105">Contains a row and the operation that is performed on that row in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a><span data-ttu-id="bf2c9-106">Members</span><span class="sxs-lookup"><span data-stu-id="bf2c9-106">Members</span></span>

<span data-ttu-id="bf2c9-107">**ulRowFlags**</span><span class="sxs-lookup"><span data-stu-id="bf2c9-107">**ulRowFlags**</span></span>
  
> <span data-ttu-id="bf2c9-108">Один из следующих операций выполняется на данные.</span><span class="sxs-lookup"><span data-stu-id="bf2c9-108">One of the following operations to be performed on the data:</span></span> 
    
  - <span data-ttu-id="bf2c9-109">ROW_ADD: Добавление данных в таблицу как новую строку.</span><span class="sxs-lookup"><span data-stu-id="bf2c9-109">ROW_ADD: Add the data to the table as a new row.</span></span>
      
  - <span data-ttu-id="bf2c9-110">ROW_MODIFY: Изменение этой строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="bf2c9-110">ROW_MODIFY: Modify this row in the table.</span></span>
      
  - <span data-ttu-id="bf2c9-111">ROW_REMOVE: Удаление этой строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="bf2c9-111">ROW_REMOVE: Remove this row from the table.</span></span>
      
  - <span data-ttu-id="bf2c9-112">ROW_EMPTY: Не добавляйте строку данных в таблицу.</span><span class="sxs-lookup"><span data-stu-id="bf2c9-112">ROW_EMPTY: Do not add the row data to the table.</span></span> <span data-ttu-id="bf2c9-113">(Строка является пустым.)</span><span class="sxs-lookup"><span data-stu-id="bf2c9-113">(The row is empty.)</span></span>
    
<span data-ttu-id="bf2c9-114">**cValues**</span><span class="sxs-lookup"><span data-stu-id="bf2c9-114">**cValues**</span></span>
  
> <span data-ttu-id="bf2c9-115">Количество значений свойств в **rgPropvals**.</span><span class="sxs-lookup"><span data-stu-id="bf2c9-115">The number of property values in **rgPropvals**.</span></span>
    
<span data-ttu-id="bf2c9-116">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="bf2c9-116">**rgPropVals**</span></span>
  
> <span data-ttu-id="bf2c9-117">Массив структур [SPropValue](spropvalue.md) , представляющих значения столбцов для вставки в таблице.</span><span class="sxs-lookup"><span data-stu-id="bf2c9-117">An array of [SPropValue](spropvalue.md) structures representing the columns values to be inserted into the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="bf2c9-118">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="bf2c9-118">MFCMAPI reference</span></span>

<span data-ttu-id="bf2c9-119">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="bf2c9-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bf2c9-120">**����**</span><span class="sxs-lookup"><span data-stu-id="bf2c9-120">**File**</span></span>|<span data-ttu-id="bf2c9-121">**�������**</span><span class="sxs-lookup"><span data-stu-id="bf2c9-121">**Function**</span></span>|<span data-ttu-id="bf2c9-122">**�����������**</span><span class="sxs-lookup"><span data-stu-id="bf2c9-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bf2c9-123">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="bf2c9-123">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="bf2c9-124">CRulesDlg::GetSelectedItems</span><span class="sxs-lookup"><span data-stu-id="bf2c9-124">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="bf2c9-125">Используются для формирования список выбранных правил для последующих действий **ModifyTable** .</span><span class="sxs-lookup"><span data-stu-id="bf2c9-125">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bf2c9-126">См. также</span><span class="sxs-lookup"><span data-stu-id="bf2c9-126">See also</span></span>
  
- [<span data-ttu-id="bf2c9-127">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bf2c9-127">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
- [<span data-ttu-id="bf2c9-128">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="bf2c9-128">MAPI Structures</span></span>](mapi-structures.md)

