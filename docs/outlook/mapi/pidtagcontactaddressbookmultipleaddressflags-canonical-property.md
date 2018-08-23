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
ms.openlocfilehash: b783a624ef5358a69d65dd52785b285db1a70df7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588673"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="2da01-103">Каноническое свойство PidTagContactAddressBookMultipleAddressFlags</span><span class="sxs-lookup"><span data-stu-id="2da01-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="2da01-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2da01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2da01-105">Содержит флаги, указывающее, поддерживает ли поставщики нескольких электронной почты решает каждого элемента контакта.</span><span class="sxs-lookup"><span data-stu-id="2da01-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2da01-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2da01-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2da01-107">PR_CONTAB_MULTI_ADDR_FLAGS</span><span class="sxs-lookup"><span data-stu-id="2da01-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="2da01-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2da01-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2da01-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="2da01-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="2da01-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2da01-110">Data type:</span></span>  <br/> |<span data-ttu-id="2da01-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="2da01-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="2da01-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2da01-112">Area:</span></span>  <br/> |<span data-ttu-id="2da01-113">Адресная книга контактов</span><span class="sxs-lookup"><span data-stu-id="2da01-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2da01-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2da01-114">Remarks</span></span>

<span data-ttu-id="2da01-115">Если флаги в этом свойстве значение TRUE, поставщик не включает контакты без адреса электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2da01-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="2da01-116">Будет учитываться только основной адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2da01-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="2da01-117">Это свойство в разделе профилей контактов адресной книги.</span><span class="sxs-lookup"><span data-stu-id="2da01-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2da01-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2da01-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2da01-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2da01-119">Header files</span></span>

<span data-ttu-id="2da01-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2da01-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="2da01-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2da01-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="2da01-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2da01-122">Mapitags.h</span></span>
  
> <span data-ttu-id="2da01-123">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="2da01-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2da01-124">См. также</span><span class="sxs-lookup"><span data-stu-id="2da01-124">See also</span></span>



[<span data-ttu-id="2da01-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2da01-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2da01-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2da01-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2da01-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2da01-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2da01-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2da01-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

