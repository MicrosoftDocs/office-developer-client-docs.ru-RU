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
# <a name="pidtagrpcoverhttpproxyauthscheme-canonical-property"></a><span data-ttu-id="5d98f-103">Каноническое свойство PidTagRpcOverHttpProxyAuthScheme</span><span class="sxs-lookup"><span data-stu-id="5d98f-103">PidTagRpcOverHttpProxyAuthScheme Canonical Property</span></span>

  
  
<span data-ttu-id="5d98f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d98f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d98f-105">Представляет протокол проверки подлинности, который будет использоваться для этого профиля.</span><span class="sxs-lookup"><span data-stu-id="5d98f-105">Represents the authentication protocol to be used for this profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d98f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5d98f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5d98f-107">PR_ROH_PROXY_AUTH_SCHEME</span><span class="sxs-lookup"><span data-stu-id="5d98f-107">PR_ROH_PROXY_AUTH_SCHEME</span></span>  <br/> |
|<span data-ttu-id="5d98f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5d98f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5d98f-109">0x6627</span><span class="sxs-lookup"><span data-stu-id="5d98f-109">0x6627</span></span>  <br/> |
|<span data-ttu-id="5d98f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5d98f-110">Data type:</span></span>  <br/> |<span data-ttu-id="5d98f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5d98f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5d98f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5d98f-112">Area:</span></span>  <br/> |<span data-ttu-id="5d98f-113">Разное</span><span class="sxs-lookup"><span data-stu-id="5d98f-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d98f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5d98f-114">Remarks</span></span>

<span data-ttu-id="5d98f-115">Это свойство можно настроить для обычной проверки подлинности или проверки подлинности с помощью NT LAN Manager (NTLM).</span><span class="sxs-lookup"><span data-stu-id="5d98f-115">This property can be set for either basic authentication or NT LAN Manager (NTLM) authentication.</span></span> <span data-ttu-id="5d98f-116">Ниже приведены возможные значения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="5d98f-116">The possible values for this property are as follow.</span></span>
  
|<span data-ttu-id="5d98f-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="5d98f-117">**Name**</span></span>|<span data-ttu-id="5d98f-118">**Value**</span><span class="sxs-lookup"><span data-stu-id="5d98f-118">**Value**</span></span>|<span data-ttu-id="5d98f-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5d98f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5d98f-120">**ROHAUTH_BASIC**</span><span class="sxs-lookup"><span data-stu-id="5d98f-120">**ROHAUTH_BASIC**</span></span> <br/> |<span data-ttu-id="5d98f-121">0x1</span><span class="sxs-lookup"><span data-stu-id="5d98f-121">0x1</span></span>  <br/> |<span data-ttu-id="5d98f-122">Обычная проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="5d98f-122">Basic authentication</span></span>  <br/> |
|<span data-ttu-id="5d98f-123">**ROHAUTH_NTLM**</span><span class="sxs-lookup"><span data-stu-id="5d98f-123">**ROHAUTH_NTLM**</span></span> <br/> |<span data-ttu-id="5d98f-124">0x2</span><span class="sxs-lookup"><span data-stu-id="5d98f-124">0x2</span></span>  <br/> |<span data-ttu-id="5d98f-125">Проверка подлинности NTLM</span><span class="sxs-lookup"><span data-stu-id="5d98f-125">NTLM authentication</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5d98f-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5d98f-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5d98f-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5d98f-127">Protocol specifications</span></span>

<span data-ttu-id="5d98f-128">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d98f-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d98f-129">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5d98f-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5d98f-130">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d98f-130">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d98f-131">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="5d98f-131">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="5d98f-132">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d98f-132">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d98f-133">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5d98f-133">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5d98f-134">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5d98f-134">Header files</span></span>

<span data-ttu-id="5d98f-135">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="5d98f-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="5d98f-136">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5d98f-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="5d98f-137">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="5d98f-137">Mapitags.h</span></span>
  
> <span data-ttu-id="5d98f-138">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="5d98f-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d98f-139">См. также</span><span class="sxs-lookup"><span data-stu-id="5d98f-139">See also</span></span>



[<span data-ttu-id="5d98f-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5d98f-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5d98f-141">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="5d98f-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5d98f-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5d98f-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5d98f-143">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5d98f-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

