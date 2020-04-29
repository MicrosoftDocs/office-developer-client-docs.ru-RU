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
# <a name="pidtagrulestable-canonical-property"></a><span data-ttu-id="224ee-103">Каноническое свойство PidTagRulesTable</span><span class="sxs-lookup"><span data-stu-id="224ee-103">PidTagRulesTable Canonical Property</span></span>

  
  
<span data-ttu-id="224ee-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="224ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="224ee-105">Содержит таблицу со всеми правилами, примененными к папке.</span><span class="sxs-lookup"><span data-stu-id="224ee-105">Contains a table with all rules applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="224ee-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="224ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="224ee-107">PR_RULES_TABLE</span><span class="sxs-lookup"><span data-stu-id="224ee-107">PR_RULES_TABLE</span></span>  <br/> |
|<span data-ttu-id="224ee-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="224ee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="224ee-109">0x3FE1</span><span class="sxs-lookup"><span data-stu-id="224ee-109">0x3FE1</span></span>  <br/> |
|<span data-ttu-id="224ee-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="224ee-110">Data type:</span></span>  <br/> |<span data-ttu-id="224ee-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="224ee-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="224ee-112">Область:</span><span class="sxs-lookup"><span data-stu-id="224ee-112">Area:</span></span>  <br/> |<span data-ttu-id="224ee-113">Правила на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="224ee-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="224ee-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="224ee-114">Remarks</span></span>

<span data-ttu-id="224ee-115">Это свойство присутствует во всех объектах папки на сервере Exchange с правилами.</span><span class="sxs-lookup"><span data-stu-id="224ee-115">This property is present on all folder objects on an Exchange Server that have rules.</span></span> <span data-ttu-id="224ee-116">Значения, включенные в это свойство, используются для чтения и изменения правил.</span><span class="sxs-lookup"><span data-stu-id="224ee-116">Values included in this property are used for reading and modifying rules.</span></span> <span data-ttu-id="224ee-117">Вы можете использовать метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) с идентификатором интерфейса **IID_IExchangeModifyTable** , чтобы получить интерфейс [иексчанжемодифитабле: IUnknown](iexchangemodifytableiunknown.md) для таблицы Rules в папке.</span><span class="sxs-lookup"><span data-stu-id="224ee-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the rules table on a folder.</span></span> <span data-ttu-id="224ee-118">Вы можете использовать этот интерфейс для чтения и изменения этих правил.</span><span class="sxs-lookup"><span data-stu-id="224ee-118">You can use this interface to read and modify those rules.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="224ee-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="224ee-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="224ee-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="224ee-120">Header files</span></span>

<span data-ttu-id="224ee-121">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="224ee-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="224ee-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="224ee-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="224ee-123">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="224ee-123">Mapitags.h</span></span>
  
> <span data-ttu-id="224ee-124">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="224ee-124">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="224ee-125">См. также</span><span class="sxs-lookup"><span data-stu-id="224ee-125">See also</span></span>



[<span data-ttu-id="224ee-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="224ee-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="224ee-127">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="224ee-127">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)


[<span data-ttu-id="224ee-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="224ee-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="224ee-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="224ee-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="224ee-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="224ee-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="224ee-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="224ee-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

