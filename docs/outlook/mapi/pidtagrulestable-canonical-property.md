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
ms.openlocfilehash: e1c670cd566e838104ae3d5480c2297f8632d899
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428503"
---
# <a name="pidtagrulestable-canonical-property"></a><span data-ttu-id="0de6c-103">Каноническое свойство PidTagRulesTable</span><span class="sxs-lookup"><span data-stu-id="0de6c-103">PidTagRulesTable Canonical Property</span></span>

  
  
<span data-ttu-id="0de6c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0de6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0de6c-105">Содержит таблицу со всеми правилами, применяемыми к папке.</span><span class="sxs-lookup"><span data-stu-id="0de6c-105">Contains a table with all rules applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0de6c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0de6c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0de6c-107">PR_RULES_TABLE</span><span class="sxs-lookup"><span data-stu-id="0de6c-107">PR_RULES_TABLE</span></span>  <br/> |
|<span data-ttu-id="0de6c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0de6c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0de6c-109">0x3FE1</span><span class="sxs-lookup"><span data-stu-id="0de6c-109">0x3FE1</span></span>  <br/> |
|<span data-ttu-id="0de6c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0de6c-110">Data type:</span></span>  <br/> |<span data-ttu-id="0de6c-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="0de6c-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="0de6c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0de6c-112">Area:</span></span>  <br/> |<span data-ttu-id="0de6c-113">Правила стороне сервера</span><span class="sxs-lookup"><span data-stu-id="0de6c-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0de6c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0de6c-114">Remarks</span></span>

<span data-ttu-id="0de6c-115">Это свойство присутствует во всех объектах папок на Exchange Server с правилами.</span><span class="sxs-lookup"><span data-stu-id="0de6c-115">This property is present on all folder objects on an Exchange Server that have rules.</span></span> <span data-ttu-id="0de6c-116">Значения, включенные в это свойство, используются для чтения и изменения правил.</span><span class="sxs-lookup"><span data-stu-id="0de6c-116">Values included in this property are used for reading and modifying rules.</span></span> <span data-ttu-id="0de6c-117">Вы можете использовать метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с идентификатором **IID_IExchangeModifyTable** интерфейса для получения [интерфейса IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) к таблице правил в папке.</span><span class="sxs-lookup"><span data-stu-id="0de6c-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the rules table on a folder.</span></span> <span data-ttu-id="0de6c-118">Этот интерфейс можно использовать для чтения и изменения этих правил.</span><span class="sxs-lookup"><span data-stu-id="0de6c-118">You can use this interface to read and modify those rules.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0de6c-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0de6c-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0de6c-120">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="0de6c-120">Header files</span></span>

<span data-ttu-id="0de6c-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0de6c-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="0de6c-122">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0de6c-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="0de6c-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0de6c-123">Mapitags.h</span></span>
  
> <span data-ttu-id="0de6c-124">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="0de6c-124">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0de6c-125">См. также</span><span class="sxs-lookup"><span data-stu-id="0de6c-125">See also</span></span>



[<span data-ttu-id="0de6c-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0de6c-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="0de6c-127">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="0de6c-127">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)


[<span data-ttu-id="0de6c-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0de6c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0de6c-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0de6c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0de6c-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0de6c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0de6c-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="0de6c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

