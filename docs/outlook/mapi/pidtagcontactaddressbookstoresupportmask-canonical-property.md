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
ms.openlocfilehash: 5cd113c263c97ba306fcf7bf97c750e710eac922
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810956"
---
# <a name="pidtagcontactaddressbookstoresupportmask-canonical-property"></a><span data-ttu-id="bf7ca-103">Каноническое свойство PidTagContactAddressBookStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="bf7ca-103">PidTagContactAddressBookStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="bf7ca-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bf7ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bf7ca-105">Содержит свойство **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)), полученный из хранилища, который содержит папки «Контакты».</span><span class="sxs-lookup"><span data-stu-id="bf7ca-105">Contains the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)) property obtained from the store that contains the Contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf7ca-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bf7ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf7ca-107">PR_CONTAB_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="bf7ca-107">PR_CONTAB_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="bf7ca-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bf7ca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bf7ca-109">0x6611</span><span class="sxs-lookup"><span data-stu-id="bf7ca-109">0x6611</span></span>  <br/> |
|<span data-ttu-id="bf7ca-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bf7ca-110">Data type:</span></span>  <br/> |<span data-ttu-id="bf7ca-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bf7ca-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bf7ca-112">Область:</span><span class="sxs-lookup"><span data-stu-id="bf7ca-112">Area:</span></span>  <br/> |<span data-ttu-id="bf7ca-113">Адресная книга контактов</span><span class="sxs-lookup"><span data-stu-id="bf7ca-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf7ca-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="bf7ca-114">Remarks</span></span>

<span data-ttu-id="bf7ca-115">Поставщик адресной книги для контакта использует это свойство для оценить пригодность поддерживаемые функции хранилища.</span><span class="sxs-lookup"><span data-stu-id="bf7ca-115">The Contact Address Book provider uses this property to evaluate the adequacy of the store's supported features.</span></span> <span data-ttu-id="bf7ca-116">Это свойство в контейнере контактов адресной книги и на столбец в таблице контейнеров контактов адресной книги.</span><span class="sxs-lookup"><span data-stu-id="bf7ca-116">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bf7ca-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bf7ca-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bf7ca-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="bf7ca-118">Header files</span></span>

<span data-ttu-id="bf7ca-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf7ca-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf7ca-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bf7ca-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="bf7ca-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bf7ca-121">Mapitags.h</span></span>
  
> <span data-ttu-id="bf7ca-122">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="bf7ca-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf7ca-123">См. также</span><span class="sxs-lookup"><span data-stu-id="bf7ca-123">See also</span></span>



[<span data-ttu-id="bf7ca-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bf7ca-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf7ca-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bf7ca-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf7ca-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bf7ca-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf7ca-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="bf7ca-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

