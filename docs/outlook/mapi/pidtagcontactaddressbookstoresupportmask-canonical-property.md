---
title: Каноническое свойство PidTagContactAddressBookStoreSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookStoreSupportMask
api_type:
- HeaderDef
ms.assetid: 34f649c8-29bf-470f-9b05-31b69d069259
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7219a8936381c498e7b27898f5efae8e40697b59
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565615"
---
# <a name="pidtagcontactaddressbookstoresupportmask-canonical-property"></a><span data-ttu-id="5a2a5-103">Каноническое свойство PidTagContactAddressBookStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="5a2a5-103">PidTagContactAddressBookStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="5a2a5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a2a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a2a5-105">Содержит свойство **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)), полученный из хранилища, который содержит папки «Контакты».</span><span class="sxs-lookup"><span data-stu-id="5a2a5-105">Contains the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)) property obtained from the store that contains the Contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a2a5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5a2a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a2a5-107">PR_CONTAB_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="5a2a5-107">PR_CONTAB_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="5a2a5-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5a2a5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a2a5-109">0x6611</span><span class="sxs-lookup"><span data-stu-id="5a2a5-109">0x6611</span></span>  <br/> |
|<span data-ttu-id="5a2a5-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5a2a5-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a2a5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5a2a5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5a2a5-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5a2a5-112">Area:</span></span>  <br/> |<span data-ttu-id="5a2a5-113">Адресная книга контактов</span><span class="sxs-lookup"><span data-stu-id="5a2a5-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a2a5-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="5a2a5-114">Remarks</span></span>

<span data-ttu-id="5a2a5-115">Поставщик адресной книги для контакта использует это свойство для оценить пригодность поддерживаемые функции хранилища.</span><span class="sxs-lookup"><span data-stu-id="5a2a5-115">The Contact Address Book provider uses this property to evaluate the adequacy of the store's supported features.</span></span> <span data-ttu-id="5a2a5-116">Это свойство в контейнере контактов адресной книги и на столбец в таблице контейнеров контактов адресной книги.</span><span class="sxs-lookup"><span data-stu-id="5a2a5-116">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5a2a5-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5a2a5-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5a2a5-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5a2a5-118">Header files</span></span>

<span data-ttu-id="5a2a5-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a2a5-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a2a5-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5a2a5-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="5a2a5-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5a2a5-121">Mapitags.h</span></span>
  
> <span data-ttu-id="5a2a5-122">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="5a2a5-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a2a5-123">См. также</span><span class="sxs-lookup"><span data-stu-id="5a2a5-123">See also</span></span>



[<span data-ttu-id="5a2a5-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5a2a5-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a2a5-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5a2a5-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a2a5-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5a2a5-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a2a5-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5a2a5-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

