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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357934"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="bf72b-103">Каноническое свойство PidTagContactAddressBookMultipleAddressFlags</span><span class="sxs-lookup"><span data-stu-id="bf72b-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="bf72b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf72b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf72b-105">Содержит флаги, указывающие, будут ли поставщики поддерживать несколько адресов электронной почты для каждого элемента контакта.</span><span class="sxs-lookup"><span data-stu-id="bf72b-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf72b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bf72b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf72b-107">ПР_КОНТАБ_МУЛТИ_АДДР_ФЛАГС</span><span class="sxs-lookup"><span data-stu-id="bf72b-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="bf72b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bf72b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bf72b-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="bf72b-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="bf72b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bf72b-110">Data type:</span></span>  <br/> |<span data-ttu-id="bf72b-111">ПТ_МВ_ЛОНГ</span><span class="sxs-lookup"><span data-stu-id="bf72b-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="bf72b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="bf72b-112">Area:</span></span>  <br/> |<span data-ttu-id="bf72b-113">Адресная книга контактов</span><span class="sxs-lookup"><span data-stu-id="bf72b-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf72b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf72b-114">Remarks</span></span>

<span data-ttu-id="bf72b-115">Если флаги в этом свойстве имеют значение TRUE, то поставщик не включает контакты без адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="bf72b-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="bf72b-116">Будет учитываться только основной адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="bf72b-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="bf72b-117">Это свойство раздела профиля адресной книги контакта.</span><span class="sxs-lookup"><span data-stu-id="bf72b-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bf72b-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bf72b-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bf72b-119">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="bf72b-119">Header files</span></span>

<span data-ttu-id="bf72b-120">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="bf72b-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf72b-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bf72b-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="bf72b-122">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="bf72b-122">Mapitags.h</span></span>
  
> <span data-ttu-id="bf72b-123">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="bf72b-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf72b-124">См. также</span><span class="sxs-lookup"><span data-stu-id="bf72b-124">See also</span></span>



[<span data-ttu-id="bf72b-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bf72b-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf72b-126">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="bf72b-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf72b-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bf72b-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf72b-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="bf72b-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

