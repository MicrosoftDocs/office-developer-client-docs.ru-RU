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
ms.openlocfilehash: 4b4b60084b8cb53a0a245b502b8fe70241fb4eb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591691"
---
# <a name="pidtagrulestable-canonical-property"></a><span data-ttu-id="950b2-103">Каноническое свойство PidTagRulesTable</span><span class="sxs-lookup"><span data-stu-id="950b2-103">PidTagRulesTable Canonical Property</span></span>

  
  
<span data-ttu-id="950b2-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="950b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="950b2-105">Содержит таблицу со всех правил, применяемых в папку.</span><span class="sxs-lookup"><span data-stu-id="950b2-105">Contains a table with all rules applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="950b2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="950b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="950b2-107">PR_RULES_TABLE</span><span class="sxs-lookup"><span data-stu-id="950b2-107">PR_RULES_TABLE</span></span>  <br/> |
|<span data-ttu-id="950b2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="950b2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="950b2-109">0x3FE1</span><span class="sxs-lookup"><span data-stu-id="950b2-109">0x3FE1</span></span>  <br/> |
|<span data-ttu-id="950b2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="950b2-110">Data type:</span></span>  <br/> |<span data-ttu-id="950b2-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="950b2-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="950b2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="950b2-112">Area:</span></span>  <br/> |<span data-ttu-id="950b2-113">Правила со стороны сервера</span><span class="sxs-lookup"><span data-stu-id="950b2-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="950b2-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="950b2-114">Remarks</span></span>

<span data-ttu-id="950b2-115">Это свойство присутствует на всех объектов папок на сервере Exchange, которые имеют правила.</span><span class="sxs-lookup"><span data-stu-id="950b2-115">This property is present on all folder objects on an Exchange Server that have rules.</span></span> <span data-ttu-id="950b2-116">Значения, включенные в этом свойстве используются для чтения и изменения правил.</span><span class="sxs-lookup"><span data-stu-id="950b2-116">Values included in this property are used for reading and modifying rules.</span></span> <span data-ttu-id="950b2-117">Можно использовать метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с идентификатором интерфейса **IID_IExchangeModifyTable** для получения [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) интерфейс к таблице правил для папки.</span><span class="sxs-lookup"><span data-stu-id="950b2-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the rules table on a folder.</span></span> <span data-ttu-id="950b2-118">Этот интерфейс можно использовать для чтения и изменения этих правил.</span><span class="sxs-lookup"><span data-stu-id="950b2-118">You can use this interface to read and modify those rules.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="950b2-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="950b2-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="950b2-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="950b2-120">Header files</span></span>

<span data-ttu-id="950b2-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="950b2-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="950b2-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="950b2-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="950b2-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="950b2-123">Mapitags.h</span></span>
  
> <span data-ttu-id="950b2-124">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="950b2-124">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="950b2-125">См. также</span><span class="sxs-lookup"><span data-stu-id="950b2-125">See also</span></span>



[<span data-ttu-id="950b2-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="950b2-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="950b2-127">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="950b2-127">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)


[<span data-ttu-id="950b2-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="950b2-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="950b2-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="950b2-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="950b2-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="950b2-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="950b2-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="950b2-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

