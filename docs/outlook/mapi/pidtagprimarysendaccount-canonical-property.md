---
title: Каноническое свойство PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPrimarySendAccount
api_type:
- COM
ms.assetid: 2f268b3b-2e4c-4aea-8879-bdd0ac1df35c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2c32cc61fea63cd38215c30e04e8a467d4901cc9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339377"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a><span data-ttu-id="9281e-103">Каноническое свойство PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="9281e-103">PidTagPrimarySendAccount Canonical Property</span></span>

  
  
<span data-ttu-id="9281e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9281e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9281e-105">Содержит строку, которая называет первый сервер, используемый для отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="9281e-105">Contains a string that names the first server that is used to send the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9281e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9281e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9281e-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="9281e-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="9281e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9281e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9281e-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="9281e-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="9281e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9281e-110">Data type:</span></span>  <br/> |<span data-ttu-id="9281e-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9281e-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9281e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9281e-112">Area:</span></span>  <br/> |<span data-ttu-id="9281e-113">Счет</span><span class="sxs-lookup"><span data-stu-id="9281e-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9281e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9281e-114">Remarks</span></span>

<span data-ttu-id="9281e-115">Указывает первый сервер, который клиент должен использовать для отправки почты.</span><span class="sxs-lookup"><span data-stu-id="9281e-115">Specifies the first server that a client should use to send the mail.</span></span> <span data-ttu-id="9281e-116">Формат этих свойств зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="9281e-116">The format of these properties is implementation dependent.</span></span> <span data-ttu-id="9281e-117">Эти свойства могут быть использованы клиентом для определения сервера для прямой почты, но необязательно, и значение не имеет значения для сервера.</span><span class="sxs-lookup"><span data-stu-id="9281e-117">These properties can be used by the client to determine which server to direct the mail through, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9281e-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9281e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9281e-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9281e-119">Protocol specifications</span></span>

<span data-ttu-id="9281e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9281e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9281e-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="9281e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9281e-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9281e-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9281e-123">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9281e-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9281e-124">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="9281e-124">Header files</span></span>

<span data-ttu-id="9281e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9281e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9281e-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9281e-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="9281e-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9281e-127">Mapitags.h</span></span>
  
> <span data-ttu-id="9281e-128">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="9281e-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9281e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="9281e-129">See also</span></span>



[<span data-ttu-id="9281e-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9281e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9281e-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9281e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9281e-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9281e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9281e-133">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="9281e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

