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
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="5ec2c-103">Каноническое свойство PidTagContactAddressBookMultipleAddressFlag</span><span class="sxs-lookup"><span data-stu-id="5ec2c-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="5ec2c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ec2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ec2c-105">Содержит флаг TRUE, если поставщик поддерживает несколько адресов электронной почты для каждого элемента контакта.</span><span class="sxs-lookup"><span data-stu-id="5ec2c-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ec2c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5ec2c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ec2c-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="5ec2c-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="5ec2c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5ec2c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5ec2c-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="5ec2c-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="5ec2c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5ec2c-110">Data type:</span></span>  <br/> |<span data-ttu-id="5ec2c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5ec2c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5ec2c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5ec2c-112">Area:</span></span>  <br/> |<span data-ttu-id="5ec2c-113">Адресная книга контакта</span><span class="sxs-lookup"><span data-stu-id="5ec2c-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ec2c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5ec2c-114">Remarks</span></span>

<span data-ttu-id="5ec2c-115">Если это свойство имеет true, поставщик не разрешает контакты без адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5ec2c-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="5ec2c-116">Если имеется false, поставщик отображает все контакты независимо от того, есть ли у них основной адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5ec2c-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="5ec2c-117">Будет соблюдаться только основной адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5ec2c-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="5ec2c-118">Это свойство контейнера адресной книги контактов и столбец в таблице контейнеров адресной книги контактов.</span><span class="sxs-lookup"><span data-stu-id="5ec2c-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5ec2c-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5ec2c-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5ec2c-120">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="5ec2c-120">Header files</span></span>

<span data-ttu-id="5ec2c-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5ec2c-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ec2c-122">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5ec2c-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="5ec2c-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5ec2c-123">Mapitags.h</span></span>
  
> <span data-ttu-id="5ec2c-124">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="5ec2c-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ec2c-125">См. также</span><span class="sxs-lookup"><span data-stu-id="5ec2c-125">See also</span></span>



[<span data-ttu-id="5ec2c-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5ec2c-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ec2c-127">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5ec2c-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ec2c-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5ec2c-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ec2c-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5ec2c-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

