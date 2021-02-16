---
title: Каноническое свойство PidTagRpcOverHttpProxyAuthScheme
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da78f1a-6423-460c-b3a9-fd6441df9cef
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ea4b90bf1190fd71701f82d43aaee384c7987ed0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331313"
---
# <a name="pidtagrpcoverhttpproxyauthscheme-canonical-property"></a><span data-ttu-id="211cb-103">Каноническое свойство PidTagRpcOverHttpProxyAuthScheme</span><span class="sxs-lookup"><span data-stu-id="211cb-103">PidTagRpcOverHttpProxyAuthScheme Canonical Property</span></span>

  
  
<span data-ttu-id="211cb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="211cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="211cb-105">Представляет протокол проверки подлинности, используемый для этого профиля.</span><span class="sxs-lookup"><span data-stu-id="211cb-105">Represents the authentication protocol to be used for this profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="211cb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="211cb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="211cb-107">PR_ROH_PROXY_AUTH_SCHEME</span><span class="sxs-lookup"><span data-stu-id="211cb-107">PR_ROH_PROXY_AUTH_SCHEME</span></span>  <br/> |
|<span data-ttu-id="211cb-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="211cb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="211cb-109">0x6627</span><span class="sxs-lookup"><span data-stu-id="211cb-109">0x6627</span></span>  <br/> |
|<span data-ttu-id="211cb-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="211cb-110">Data type:</span></span>  <br/> |<span data-ttu-id="211cb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="211cb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="211cb-112">Область:</span><span class="sxs-lookup"><span data-stu-id="211cb-112">Area:</span></span>  <br/> |<span data-ttu-id="211cb-113">Разное</span><span class="sxs-lookup"><span data-stu-id="211cb-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="211cb-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="211cb-114">Remarks</span></span>

<span data-ttu-id="211cb-115">Это свойство можно настроить для базовой проверки подлинности или проверки подлинности NT LAN Manager (NTLM).</span><span class="sxs-lookup"><span data-stu-id="211cb-115">This property can be set for either basic authentication or NT LAN Manager (NTLM) authentication.</span></span> <span data-ttu-id="211cb-116">Возможные значения этого свойства:</span><span class="sxs-lookup"><span data-stu-id="211cb-116">The possible values for this property are as follow.</span></span>
  
|<span data-ttu-id="211cb-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="211cb-117">**Name**</span></span>|<span data-ttu-id="211cb-118">**Value**</span><span class="sxs-lookup"><span data-stu-id="211cb-118">**Value**</span></span>|<span data-ttu-id="211cb-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="211cb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="211cb-120">**ROHAUTH_BASIC**</span><span class="sxs-lookup"><span data-stu-id="211cb-120">**ROHAUTH_BASIC**</span></span> <br/> |<span data-ttu-id="211cb-121">0x1</span><span class="sxs-lookup"><span data-stu-id="211cb-121">0x1</span></span>  <br/> |<span data-ttu-id="211cb-122">Обычная проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="211cb-122">Basic authentication</span></span>  <br/> |
|<span data-ttu-id="211cb-123">**ROHAUTH_NTLM**</span><span class="sxs-lookup"><span data-stu-id="211cb-123">**ROHAUTH_NTLM**</span></span> <br/> |<span data-ttu-id="211cb-124">0x2</span><span class="sxs-lookup"><span data-stu-id="211cb-124">0x2</span></span>  <br/> |<span data-ttu-id="211cb-125">Проверка подлинности NTLM</span><span class="sxs-lookup"><span data-stu-id="211cb-125">NTLM authentication</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="211cb-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="211cb-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="211cb-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="211cb-127">Protocol specifications</span></span>

<span data-ttu-id="211cb-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="211cb-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="211cb-129">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="211cb-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="211cb-130">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="211cb-130">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="211cb-131">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="211cb-131">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="211cb-132">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="211cb-132">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="211cb-133">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="211cb-133">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="211cb-134">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="211cb-134">Header files</span></span>

<span data-ttu-id="211cb-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="211cb-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="211cb-136">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="211cb-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="211cb-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="211cb-137">Mapitags.h</span></span>
  
> <span data-ttu-id="211cb-138">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="211cb-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="211cb-139">См. также</span><span class="sxs-lookup"><span data-stu-id="211cb-139">See also</span></span>



[<span data-ttu-id="211cb-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="211cb-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="211cb-141">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="211cb-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="211cb-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="211cb-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="211cb-143">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="211cb-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

