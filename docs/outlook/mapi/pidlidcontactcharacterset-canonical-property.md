---
title: Каноническое свойство PidLidContactCharacterSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactCharacterSet
api_type:
- COM
ms.assetid: a167e199-a9b2-47f9-a90e-2abc7c29828c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 70d8266bf0eb8543b9bea7d2258b576b6f02bcc2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567736"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a><span data-ttu-id="f3424-103">Каноническое свойство PidLidContactCharacterSet</span><span class="sxs-lookup"><span data-stu-id="f3424-103">PidLidContactCharacterSet Canonical Property</span></span>

  
  
<span data-ttu-id="f3424-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3424-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3424-105">Задает набор символов, используемый для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="f3424-105">Specifies the character set used for this contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f3424-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f3424-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f3424-107">dispidContactCharSet</span><span class="sxs-lookup"><span data-stu-id="f3424-107">dispidContactCharSet</span></span>  <br/> |
|<span data-ttu-id="f3424-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="f3424-108">Property set:</span></span>  <br/> |<span data-ttu-id="f3424-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="f3424-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="f3424-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="f3424-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f3424-111">0x00008023</span><span class="sxs-lookup"><span data-stu-id="f3424-111">0x00008023</span></span>  <br/> |
|<span data-ttu-id="f3424-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f3424-112">Data type:</span></span>  <br/> |<span data-ttu-id="f3424-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f3424-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f3424-114">Область:</span><span class="sxs-lookup"><span data-stu-id="f3424-114">Area:</span></span>  <br/> |<span data-ttu-id="f3424-115">Contact</span><span class="sxs-lookup"><span data-stu-id="f3424-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3424-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="f3424-116">Remarks</span></span>

<span data-ttu-id="f3424-117">Это свойство можно использовать в приложениях для упрощения создания зависимые списка выбора для **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)), **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) и **dispidFileUnderId набор символов **Свойства ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f3424-117">Applications can use this property to aid in generating a character-set dependent list of choices for the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) , **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) , and **dispidFileUnderId** ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)) properties.</span></span> <span data-ttu-id="f3424-118">Если значение свойства «0x00000000» или «0x00000001», приложения следует считать свойство не задано.</span><span class="sxs-lookup"><span data-stu-id="f3424-118">If the value of the property is "0x00000000" or "0x00000001", applications should treat the property as not being set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f3424-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f3424-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f3424-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f3424-120">Protocol specifications</span></span>

<span data-ttu-id="f3424-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3424-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3424-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f3424-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f3424-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3424-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3424-124">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="f3424-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f3424-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f3424-125">Header files</span></span>

<span data-ttu-id="f3424-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f3424-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f3424-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f3424-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3424-128">См. также</span><span class="sxs-lookup"><span data-stu-id="f3424-128">See also</span></span>



[<span data-ttu-id="f3424-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f3424-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f3424-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f3424-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f3424-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f3424-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f3424-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f3424-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

