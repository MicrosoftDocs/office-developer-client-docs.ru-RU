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
ms.openlocfilehash: 243ab1e926171ee66b95cfd8e969cd77e2b31faf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436036"
---
# <a name="rowentry"></a><span data-ttu-id="5853c-103">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="5853c-103">ROWENTRY</span></span>

<span data-ttu-id="5853c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5853c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5853c-105">Содержит строку и операцию, выполняемую над этой строкой в таблице через интерфейс [иексчанжемодифитабле](iexchangemodifytableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="5853c-105">Contains a row and the operation that is performed on that row in a table through the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface.</span></span> 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a><span data-ttu-id="5853c-106">Members</span><span class="sxs-lookup"><span data-stu-id="5853c-106">Members</span></span>

<span data-ttu-id="5853c-107">**Улровфлагс**</span><span class="sxs-lookup"><span data-stu-id="5853c-107">**ulRowFlags**</span></span>
  
> <span data-ttu-id="5853c-108">Одна из следующих операций, которые необходимо выполнить для данных:</span><span class="sxs-lookup"><span data-stu-id="5853c-108">One of the following operations to be performed on the data:</span></span> 
    
  - <span data-ttu-id="5853c-109">РОВ_АДД: Добавление данных в таблицу в качестве новой строки.</span><span class="sxs-lookup"><span data-stu-id="5853c-109">ROW_ADD: Add the data to the table as a new row.</span></span>
      
  - <span data-ttu-id="5853c-110">РОВ_МОДИФИ: измените эту строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="5853c-110">ROW_MODIFY: Modify this row in the table.</span></span>
      
  - <span data-ttu-id="5853c-111">РОВ_РЕМОВЕ: удалите эту строку из таблицы.</span><span class="sxs-lookup"><span data-stu-id="5853c-111">ROW_REMOVE: Remove this row from the table.</span></span>
      
  - <span data-ttu-id="5853c-112">РОВ_ЕМПТИ: не добавляйте данные строк в таблицу.</span><span class="sxs-lookup"><span data-stu-id="5853c-112">ROW_EMPTY: Do not add the row data to the table.</span></span> <span data-ttu-id="5853c-113">(Строка пуста.)</span><span class="sxs-lookup"><span data-stu-id="5853c-113">(The row is empty.)</span></span>
    
<span data-ttu-id="5853c-114">**Квалуес**</span><span class="sxs-lookup"><span data-stu-id="5853c-114">**cValues**</span></span>
  
> <span data-ttu-id="5853c-115">Число значений свойств в **ргпропвалс**.</span><span class="sxs-lookup"><span data-stu-id="5853c-115">The number of property values in **rgPropvals**.</span></span>
    
<span data-ttu-id="5853c-116">**Ргпропвалс**</span><span class="sxs-lookup"><span data-stu-id="5853c-116">**rgPropVals**</span></span>
  
> <span data-ttu-id="5853c-117">Массив структур [спропвалуе](spropvalue.md) , представляющих значения столбцов, которые должны быть вставлены в таблицу.</span><span class="sxs-lookup"><span data-stu-id="5853c-117">An array of [SPropValue](spropvalue.md) structures representing the columns values to be inserted into the table.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="5853c-118">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5853c-118">MFCMAPI reference</span></span>

<span data-ttu-id="5853c-119">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="5853c-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5853c-120">**Файл**</span><span class="sxs-lookup"><span data-stu-id="5853c-120">**File**</span></span>|<span data-ttu-id="5853c-121">**Функция**</span><span class="sxs-lookup"><span data-stu-id="5853c-121">**Function**</span></span>|<span data-ttu-id="5853c-122">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="5853c-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5853c-123">Рулесдлг. cpp</span><span class="sxs-lookup"><span data-stu-id="5853c-123">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="5853c-124">Крулесдлг:: Жетселектедитемс</span><span class="sxs-lookup"><span data-stu-id="5853c-124">CRulesDlg::GetSelectedItems</span></span>  <br/> |<span data-ttu-id="5853c-125">Используется для создания списка выбранных правил для последующих действий **модифитабле** .</span><span class="sxs-lookup"><span data-stu-id="5853c-125">Used to build a list of selected rules for subsequent **ModifyTable** actions.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5853c-126">См. также</span><span class="sxs-lookup"><span data-stu-id="5853c-126">See also</span></span>
  
- [<span data-ttu-id="5853c-127">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5853c-127">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
- [<span data-ttu-id="5853c-128">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="5853c-128">MAPI Structures</span></span>](mapi-structures.md)

