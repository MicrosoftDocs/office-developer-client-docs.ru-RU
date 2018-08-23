---
title: Каноническое свойство PidTagContactAddressBookMultipleAddressFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 34f61f3ef64e5751f9be3df534c4379583447799
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592698"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="a7cb2-103">Каноническое свойство PidTagContactAddressBookMultipleAddressFlag</span><span class="sxs-lookup"><span data-stu-id="a7cb2-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="a7cb2-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7cb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7cb2-105">Содержит флаг, который имеет значение TRUE, если поставщик поддерживает несколько адресов электронной почты каждого элемента контакта.</span><span class="sxs-lookup"><span data-stu-id="a7cb2-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a7cb2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a7cb2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7cb2-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="a7cb2-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="a7cb2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a7cb2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a7cb2-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="a7cb2-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="a7cb2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a7cb2-110">Data type:</span></span>  <br/> |<span data-ttu-id="a7cb2-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a7cb2-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a7cb2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a7cb2-112">Area:</span></span>  <br/> |<span data-ttu-id="a7cb2-113">Адресная книга контактов</span><span class="sxs-lookup"><span data-stu-id="a7cb2-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7cb2-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a7cb2-114">Remarks</span></span>

<span data-ttu-id="a7cb2-115">Если это свойство имеет значение TRUE, поставщик не разрешает контакты без адреса электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a7cb2-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="a7cb2-116">Если задано значение FALSE, поставщик показывает все контакты ли они имеют основной адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a7cb2-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="a7cb2-117">Будет учитываться только основной адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a7cb2-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="a7cb2-118">Это свойство в контейнере контактов адресной книги и на столбец в таблице контейнеров контактов адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a7cb2-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a7cb2-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a7cb2-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a7cb2-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a7cb2-120">Header files</span></span>

<span data-ttu-id="a7cb2-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7cb2-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7cb2-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a7cb2-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="a7cb2-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a7cb2-123">Mapitags.h</span></span>
  
> <span data-ttu-id="a7cb2-124">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="a7cb2-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7cb2-125">См. также</span><span class="sxs-lookup"><span data-stu-id="a7cb2-125">See also</span></span>



[<span data-ttu-id="a7cb2-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a7cb2-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7cb2-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a7cb2-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7cb2-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a7cb2-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7cb2-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a7cb2-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

