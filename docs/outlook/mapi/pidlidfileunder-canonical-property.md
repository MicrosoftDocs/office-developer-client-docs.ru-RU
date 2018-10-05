---
title: Каноническое свойство PidLidFileUnder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnder
api_type:
- COM
ms.assetid: 55afc4bb-c5fc-4162-a293-7d82644b1965
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 02aa1766421f7c116eabac4c9661be1b5b1adee1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393573"
---
# <a name="pidlidfileunder-canonical-property"></a><span data-ttu-id="361e4-103">Каноническое свойство PidLidFileUnder</span><span class="sxs-lookup"><span data-stu-id="361e4-103">PidLidFileUnder Canonical Property</span></span>

  
  
<span data-ttu-id="361e4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="361e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="361e4-105">Указывает имя, под которым контакт хранения при отображении списка контактов.</span><span class="sxs-lookup"><span data-stu-id="361e4-105">Specifies the name under which the contact is filed when displaying a list of contacts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="361e4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="361e4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="361e4-107">dispidFileUnder</span><span class="sxs-lookup"><span data-stu-id="361e4-107">dispidFileUnder</span></span>  <br/> |
|<span data-ttu-id="361e4-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="361e4-108">Property set:</span></span>  <br/> |<span data-ttu-id="361e4-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="361e4-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="361e4-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="361e4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="361e4-111">0x00008005</span><span class="sxs-lookup"><span data-stu-id="361e4-111">0x00008005</span></span>  <br/> |
|<span data-ttu-id="361e4-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="361e4-112">Data type:</span></span>  <br/> |<span data-ttu-id="361e4-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="361e4-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="361e4-114">Область:</span><span class="sxs-lookup"><span data-stu-id="361e4-114">Area:</span></span>  <br/> |<span data-ttu-id="361e4-115">Contact</span><span class="sxs-lookup"><span data-stu-id="361e4-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="361e4-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="361e4-116">Remarks</span></span>

<span data-ttu-id="361e4-117">Приложение следует считать это свойство пустым PT_UNICODE в случае отсутствия от контакта.</span><span class="sxs-lookup"><span data-stu-id="361e4-117">The application should treat this property as an empty PT_UNICODE if it is missing from the contact.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="361e4-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="361e4-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="361e4-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="361e4-119">Protocol specifications</span></span>

<span data-ttu-id="361e4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="361e4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="361e4-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="361e4-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="361e4-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="361e4-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="361e4-123">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="361e4-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="361e4-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="361e4-124">Header files</span></span>

<span data-ttu-id="361e4-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="361e4-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="361e4-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="361e4-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="361e4-127">См. также</span><span class="sxs-lookup"><span data-stu-id="361e4-127">See also</span></span>



[<span data-ttu-id="361e4-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="361e4-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="361e4-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="361e4-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="361e4-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="361e4-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="361e4-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="361e4-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

