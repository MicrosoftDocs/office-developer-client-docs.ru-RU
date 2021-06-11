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
ms.openlocfilehash: 6fabb03d552f195c200b0ecbd8fd69f470c0e1fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431570"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="0795b-103">Каноническое свойство PidTagContactAddressBookMultipleAddressFlag</span><span class="sxs-lookup"><span data-stu-id="0795b-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="0795b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0795b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0795b-105">Содержит флаг TRUE, когда поставщик поддерживает несколько адресов электронной почты для каждого контактного элемента.</span><span class="sxs-lookup"><span data-stu-id="0795b-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0795b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0795b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0795b-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="0795b-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="0795b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0795b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0795b-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="0795b-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="0795b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0795b-110">Data type:</span></span>  <br/> |<span data-ttu-id="0795b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0795b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0795b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0795b-112">Area:</span></span>  <br/> |<span data-ttu-id="0795b-113">Адресная книга контактов</span><span class="sxs-lookup"><span data-stu-id="0795b-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0795b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0795b-114">Remarks</span></span>

<span data-ttu-id="0795b-115">Если это свойство true, поставщик не разрешает контакты без адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="0795b-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="0795b-116">Если false, поставщик показывает все контакты независимо от того, есть ли у них основной адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="0795b-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="0795b-117">Будет соблюдаться только основной адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="0795b-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="0795b-118">Это свойство в контейнере адресной книги контактов и столбец в таблице контейнеров адресной книги контактов.</span><span class="sxs-lookup"><span data-stu-id="0795b-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0795b-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0795b-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0795b-120">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="0795b-120">Header files</span></span>

<span data-ttu-id="0795b-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0795b-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="0795b-122">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0795b-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="0795b-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0795b-123">Mapitags.h</span></span>
  
> <span data-ttu-id="0795b-124">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="0795b-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0795b-125">См. также</span><span class="sxs-lookup"><span data-stu-id="0795b-125">See also</span></span>



[<span data-ttu-id="0795b-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0795b-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0795b-127">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0795b-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0795b-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0795b-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0795b-129">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="0795b-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

