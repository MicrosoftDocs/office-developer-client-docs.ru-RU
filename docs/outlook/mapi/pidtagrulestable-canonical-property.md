---
title: Каноническое свойство PidTagRulesTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fc520720-8190-4dff-8f6c-1bebf7080b57
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 945dabec4ee34d38d2474c918e779d894f4a917c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811804"
---
# <a name="pidtagrulestable-canonical-property"></a><span data-ttu-id="fc80d-103">Каноническое свойство PidTagRulesTable</span><span class="sxs-lookup"><span data-stu-id="fc80d-103">PidTagRulesTable Canonical Property</span></span>

  
  
<span data-ttu-id="fc80d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc80d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc80d-105">Содержит таблицу со всех правил, применяемых в папку.</span><span class="sxs-lookup"><span data-stu-id="fc80d-105">Contains a table with all rules applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc80d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="fc80d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc80d-107">PR_RULES_TABLE</span><span class="sxs-lookup"><span data-stu-id="fc80d-107">PR_RULES_TABLE</span></span>  <br/> |
|<span data-ttu-id="fc80d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="fc80d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fc80d-109">0x3FE1</span><span class="sxs-lookup"><span data-stu-id="fc80d-109">0x3FE1</span></span>  <br/> |
|<span data-ttu-id="fc80d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="fc80d-110">Data type:</span></span>  <br/> |<span data-ttu-id="fc80d-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="fc80d-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="fc80d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="fc80d-112">Area:</span></span>  <br/> |<span data-ttu-id="fc80d-113">Правила со стороны сервера</span><span class="sxs-lookup"><span data-stu-id="fc80d-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc80d-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="fc80d-114">Remarks</span></span>

<span data-ttu-id="fc80d-115">Это свойство присутствует на всех объектов папок на сервере Exchange, которые имеют правила.</span><span class="sxs-lookup"><span data-stu-id="fc80d-115">This property is present on all folder objects on an Exchange Server that have rules.</span></span> <span data-ttu-id="fc80d-116">Значения, включенные в этом свойстве используются для чтения и изменения правил.</span><span class="sxs-lookup"><span data-stu-id="fc80d-116">Values included in this property are used for reading and modifying rules.</span></span> <span data-ttu-id="fc80d-117">Можно использовать метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с идентификатором интерфейса **IID_IExchangeModifyTable** для получения [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) интерфейс к таблице правил для папки.</span><span class="sxs-lookup"><span data-stu-id="fc80d-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the rules table on a folder.</span></span> <span data-ttu-id="fc80d-118">Этот интерфейс можно использовать для чтения и изменения этих правил.</span><span class="sxs-lookup"><span data-stu-id="fc80d-118">You can use this interface to read and modify those rules.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fc80d-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fc80d-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fc80d-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="fc80d-120">Header files</span></span>

<span data-ttu-id="fc80d-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc80d-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc80d-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="fc80d-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="fc80d-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fc80d-123">Mapitags.h</span></span>
  
> <span data-ttu-id="fc80d-124">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="fc80d-124">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="fc80d-125">См. также</span><span class="sxs-lookup"><span data-stu-id="fc80d-125">See also</span></span>



[<span data-ttu-id="fc80d-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fc80d-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="fc80d-127">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="fc80d-127">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)


[<span data-ttu-id="fc80d-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fc80d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc80d-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fc80d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc80d-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="fc80d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc80d-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="fc80d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

