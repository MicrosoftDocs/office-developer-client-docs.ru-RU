---
title: Каноническое свойство PidTagContactAddressBookMultipleAddressFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ecd795490d953f1aa237dfbd77585ba79c8b3234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429252"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="d1fe5-103">Каноническое свойство PidTagContactAddressBookMultipleAddressFlags</span><span class="sxs-lookup"><span data-stu-id="d1fe5-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="d1fe5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1fe5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1fe5-105">Содержит флаги, указывающие, будут ли поставщики поддерживать несколько адресов электронной почты для каждого элемента контакта.</span><span class="sxs-lookup"><span data-stu-id="d1fe5-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1fe5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d1fe5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1fe5-107">PR_CONTAB_MULTI_ADDR_FLAGS</span><span class="sxs-lookup"><span data-stu-id="d1fe5-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="d1fe5-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d1fe5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d1fe5-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="d1fe5-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="d1fe5-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d1fe5-110">Data type:</span></span>  <br/> |<span data-ttu-id="d1fe5-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="d1fe5-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="d1fe5-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d1fe5-112">Area:</span></span>  <br/> |<span data-ttu-id="d1fe5-113">Адресная книга контакта</span><span class="sxs-lookup"><span data-stu-id="d1fe5-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1fe5-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d1fe5-114">Remarks</span></span>

<span data-ttu-id="d1fe5-115">Если в этом свойстве имеются флаги TRUE, поставщик не включает контакты без адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d1fe5-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="d1fe5-116">Будет соблюдаться только основной адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d1fe5-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="d1fe5-117">Это свойство в разделе профиля адресной книги контактов.</span><span class="sxs-lookup"><span data-stu-id="d1fe5-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d1fe5-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d1fe5-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d1fe5-119">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="d1fe5-119">Header files</span></span>

<span data-ttu-id="d1fe5-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1fe5-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1fe5-121">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d1fe5-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="d1fe5-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d1fe5-122">Mapitags.h</span></span>
  
> <span data-ttu-id="d1fe5-123">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="d1fe5-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1fe5-124">См. также</span><span class="sxs-lookup"><span data-stu-id="d1fe5-124">See also</span></span>



[<span data-ttu-id="d1fe5-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d1fe5-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1fe5-126">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d1fe5-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1fe5-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d1fe5-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1fe5-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d1fe5-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

