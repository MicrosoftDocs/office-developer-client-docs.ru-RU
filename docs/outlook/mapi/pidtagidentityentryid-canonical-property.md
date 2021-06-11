---
title: Каноническое свойство PidTagIdentityEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityEntryId
api_type:
- HeaderDef
ms.assetid: 61a9d403-e0e5-45c3-8d18-4d53207ab927
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 099df2211e87e253ab1be520378b3a2b2ca7d4c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423337"
---
# <a name="pidtagidentityentryid-canonical-property"></a><span data-ttu-id="0442b-103">Каноническое свойство PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="0442b-103">PidTagIdentityEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="0442b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0442b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0442b-105">Содержит идентификатор входа для удостоверения поставщика услуг, определенный в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0442b-105">Contains the entry identifier for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0442b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0442b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0442b-107">PR_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0442b-107">PR_IDENTITY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="0442b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0442b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0442b-109">0x3E01</span><span class="sxs-lookup"><span data-stu-id="0442b-109">0x3E01</span></span>  <br/> |
|<span data-ttu-id="0442b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0442b-110">Data type:</span></span>  <br/> |<span data-ttu-id="0442b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0442b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0442b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0442b-112">Area:</span></span>  <br/> |<span data-ttu-id="0442b-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="0442b-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0442b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0442b-114">Remarks</span></span>

<span data-ttu-id="0442b-115">Это свойство не появляется как свойство на любом объекте, а только как столбец в таблице состояния.</span><span class="sxs-lookup"><span data-stu-id="0442b-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="0442b-116">Он является частью удостоверения поставщика услуг, обнажающего строку таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="0442b-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="0442b-117">Удостоверение поставщика обычно ссылается на его учетную запись на сервере, но может ссылаться на любое представление, определенное поставщиком в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0442b-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="0442b-118">Этот реквизит обычно заданной для соответствующего идентификатора записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="0442b-118">This proprerty is commonly set to the appropriate address book entry identifier.</span></span> 
  
<span data-ttu-id="0442b-119">Поставщик услуг, обставленный любыми свойствами удостоверений, должен предоставить все из них.</span><span class="sxs-lookup"><span data-stu-id="0442b-119">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="0442b-120">Поставщики, принадлежащие к одной и той же службе сообщений, должны выставлять те же значения для свойств удостоверений.</span><span class="sxs-lookup"><span data-stu-id="0442b-120">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0442b-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0442b-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0442b-122">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="0442b-122">Header files</span></span>

<span data-ttu-id="0442b-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0442b-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="0442b-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0442b-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="0442b-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0442b-125">Mapitags.h</span></span>
  
> <span data-ttu-id="0442b-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="0442b-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0442b-127">См. также</span><span class="sxs-lookup"><span data-stu-id="0442b-127">See also</span></span>



[<span data-ttu-id="0442b-128">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="0442b-128">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="0442b-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0442b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0442b-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0442b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0442b-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0442b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0442b-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="0442b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

