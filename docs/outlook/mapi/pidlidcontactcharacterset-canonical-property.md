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
ms.openlocfilehash: 0329147463db38fb8c547214788366444daed312
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319707"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a><span data-ttu-id="370ae-103">Каноническое свойство PidLidContactCharacterSet</span><span class="sxs-lookup"><span data-stu-id="370ae-103">PidLidContactCharacterSet Canonical Property</span></span>

  
  
<span data-ttu-id="370ae-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="370ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="370ae-105">Задает кодировку, используемую для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="370ae-105">Specifies the character set used for this contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="370ae-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="370ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="370ae-107">Диспидконтактчарсет</span><span class="sxs-lookup"><span data-stu-id="370ae-107">dispidContactCharSet</span></span>  <br/> |
|<span data-ttu-id="370ae-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="370ae-108">Property set:</span></span>  <br/> |<span data-ttu-id="370ae-109">Псетид_аддресс</span><span class="sxs-lookup"><span data-stu-id="370ae-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="370ae-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="370ae-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="370ae-111">0x00008023</span><span class="sxs-lookup"><span data-stu-id="370ae-111">0x00008023</span></span>  <br/> |
|<span data-ttu-id="370ae-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="370ae-112">Data type:</span></span>  <br/> |<span data-ttu-id="370ae-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="370ae-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="370ae-114">Область:</span><span class="sxs-lookup"><span data-stu-id="370ae-114">Area:</span></span>  <br/> |<span data-ttu-id="370ae-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="370ae-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="370ae-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="370ae-116">Remarks</span></span>

<span data-ttu-id="370ae-117">С помощью этого свойства приложения могут создавать зависимые от набора символов список вариантов для **диспидфилеундер** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)), **Диспидфилеундерлист** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) и \*\*диспидфилеундерид \*\*Свойства ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="370ae-117">Applications can use this property to aid in generating a character-set dependent list of choices for the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) , **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) , and **dispidFileUnderId** ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)) properties.</span></span> <span data-ttu-id="370ae-118">Если значение свойства — "0x00000000" или "0x00000001", то приложения должны считать это свойство незаданным.</span><span class="sxs-lookup"><span data-stu-id="370ae-118">If the value of the property is "0x00000000" or "0x00000001", applications should treat the property as not being set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="370ae-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="370ae-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="370ae-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="370ae-120">Protocol specifications</span></span>

<span data-ttu-id="370ae-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="370ae-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="370ae-122">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="370ae-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="370ae-123">[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="370ae-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="370ae-124">Задает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="370ae-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="370ae-125">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="370ae-125">Header files</span></span>

<span data-ttu-id="370ae-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="370ae-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="370ae-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="370ae-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="370ae-128">См. также</span><span class="sxs-lookup"><span data-stu-id="370ae-128">See also</span></span>



[<span data-ttu-id="370ae-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="370ae-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="370ae-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="370ae-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="370ae-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="370ae-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="370ae-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="370ae-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

