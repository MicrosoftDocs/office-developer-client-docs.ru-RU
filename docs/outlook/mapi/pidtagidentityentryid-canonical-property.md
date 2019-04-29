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
# <a name="pidtagidentityentryid-canonical-property"></a><span data-ttu-id="f322c-103">Каноническое свойство PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="f322c-103">PidTagIdentityEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="f322c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f322c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f322c-105">Содержит идентификатор элемента для удостоверения поставщика услуг в соответствии с определением в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f322c-105">Contains the entry identifier for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f322c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f322c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f322c-107">ПР_ИДЕНТИТИ_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="f322c-107">PR_IDENTITY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="f322c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f322c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f322c-109">0x3E01</span><span class="sxs-lookup"><span data-stu-id="f322c-109">0x3E01</span></span>  <br/> |
|<span data-ttu-id="f322c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f322c-110">Data type:</span></span>  <br/> |<span data-ttu-id="f322c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f322c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f322c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f322c-112">Area:</span></span>  <br/> |<span data-ttu-id="f322c-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="f322c-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f322c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f322c-114">Remarks</span></span>

<span data-ttu-id="f322c-115">Это свойство не отображается как свойство ни для одного объекта, но только как столбец в таблице "состояние".</span><span class="sxs-lookup"><span data-stu-id="f322c-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="f322c-116">Он является частью удостоверения поставщика услуг, предоставляющего строку таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="f322c-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="f322c-117">Удостоверение поставщика обычно относится к его учетной записи на сервере, но может ссылаться на любое представление, которое определяет поставщик в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f322c-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="f322c-118">Для этого пропрерти обычно задается соответствующий идентификатор записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f322c-118">This proprerty is commonly set to the appropriate address book entry identifier.</span></span> 
  
<span data-ttu-id="f322c-119">Поставщик услуг, представляя любое из свойств Identity, должен отказаться от всех этих свойств.</span><span class="sxs-lookup"><span data-stu-id="f322c-119">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="f322c-120">Поставщики одной и той же службы сообщений должны предоставлять одни и те же значения для свойств Identity.</span><span class="sxs-lookup"><span data-stu-id="f322c-120">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f322c-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f322c-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f322c-122">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="f322c-122">Header files</span></span>

<span data-ttu-id="f322c-123">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="f322c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f322c-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f322c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f322c-125">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="f322c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f322c-126">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="f322c-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f322c-127">См. также</span><span class="sxs-lookup"><span data-stu-id="f322c-127">See also</span></span>



[<span data-ttu-id="f322c-128">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="f322c-128">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="f322c-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f322c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f322c-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="f322c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f322c-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f322c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f322c-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f322c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

