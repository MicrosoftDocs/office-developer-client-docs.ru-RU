---
title: Каноническое свойство PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNextSendAcct
api_type:
- HeaderDef
ms.assetid: b7429c2e-0d9d-4921-9f56-9ecad817f8cb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: eff053fda58266afd5500e322559059f051d5ac3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329395"
---
# <a name="pidtagnextsendacct-canonical-property"></a><span data-ttu-id="d2192-103">Каноническое свойство PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="d2192-103">PidTagNextSendAcct Canonical Property</span></span>

  
  
<span data-ttu-id="d2192-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2192-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2192-105">Указывает сервер, который клиент пытается использовать для отправки электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d2192-105">Specifies the server that a client is currently attempting to use to send email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2192-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d2192-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d2192-107">ПР_НЕКСТ_СЕНД_АККТ</span><span class="sxs-lookup"><span data-stu-id="d2192-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="d2192-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d2192-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d2192-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="d2192-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="d2192-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d2192-110">Data type:</span></span>  <br/> |<span data-ttu-id="d2192-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d2192-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d2192-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d2192-112">Area:</span></span>  <br/> |<span data-ttu-id="d2192-113">Приложение Outlook</span><span class="sxs-lookup"><span data-stu-id="d2192-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2192-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2192-114">Remarks</span></span>

<span data-ttu-id="d2192-115">Формат этого свойства зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="d2192-115">The format of this property is implementation dependent.</span></span> <span data-ttu-id="d2192-116">Это свойство можно использовать в клиенте, чтобы определить, какой сервер должен направить сообщение, но является необязательным и значение не имеет смысла для сервера.</span><span class="sxs-lookup"><span data-stu-id="d2192-116">This property can be used by the client to determine which server to direct the email to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d2192-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d2192-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d2192-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d2192-118">Protocol specifications</span></span>

<span data-ttu-id="d2192-119">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2192-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2192-120">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d2192-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d2192-121">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2192-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2192-122">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="d2192-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="d2192-123">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2192-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2192-124">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d2192-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d2192-125">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="d2192-125">Header files</span></span>

<span data-ttu-id="d2192-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d2192-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d2192-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d2192-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="d2192-128">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="d2192-128">Mapitags.h</span></span>
  
> <span data-ttu-id="d2192-129">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="d2192-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d2192-130">См. также</span><span class="sxs-lookup"><span data-stu-id="d2192-130">See also</span></span>



[<span data-ttu-id="d2192-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d2192-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d2192-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="d2192-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d2192-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d2192-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d2192-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d2192-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

