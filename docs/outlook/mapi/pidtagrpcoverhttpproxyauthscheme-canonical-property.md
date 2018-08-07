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
ms.openlocfilehash: b8c68c2cd34ba037dc725a7d15575159466d8123
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811741"
---
# <a name="pidtagrpcoverhttpproxyauthscheme-canonical-property"></a><span data-ttu-id="420bd-103">Каноническое свойство PidTagRpcOverHttpProxyAuthScheme</span><span class="sxs-lookup"><span data-stu-id="420bd-103">PidTagRpcOverHttpProxyAuthScheme Canonical Property</span></span>

  
  
<span data-ttu-id="420bd-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="420bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="420bd-105">Представляет протокол проверки подлинности, которое будет использоваться для этого профиля.</span><span class="sxs-lookup"><span data-stu-id="420bd-105">Represents the authentication protocol to be used for this profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="420bd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="420bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="420bd-107">PR_ROH_PROXY_AUTH_SCHEME</span><span class="sxs-lookup"><span data-stu-id="420bd-107">PR_ROH_PROXY_AUTH_SCHEME</span></span>  <br/> |
|<span data-ttu-id="420bd-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="420bd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="420bd-109">0x6627</span><span class="sxs-lookup"><span data-stu-id="420bd-109">0x6627</span></span>  <br/> |
|<span data-ttu-id="420bd-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="420bd-110">Data type:</span></span>  <br/> |<span data-ttu-id="420bd-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="420bd-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="420bd-112">Область:</span><span class="sxs-lookup"><span data-stu-id="420bd-112">Area:</span></span>  <br/> |<span data-ttu-id="420bd-113">Разное</span><span class="sxs-lookup"><span data-stu-id="420bd-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="420bd-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="420bd-114">Remarks</span></span>

<span data-ttu-id="420bd-115">Это свойство можно задать для обычной проверки подлинности или проверки подлинности NT LAN Manager (NTLM).</span><span class="sxs-lookup"><span data-stu-id="420bd-115">This property can be set for either basic authentication or NT LAN Manager (NTLM) authentication.</span></span> <span data-ttu-id="420bd-116">Возможны следующие возможные значения для данного свойства.</span><span class="sxs-lookup"><span data-stu-id="420bd-116">The possible values for this property are as follow.</span></span>
  
|<span data-ttu-id="420bd-117">**Имя**</span><span class="sxs-lookup"><span data-stu-id="420bd-117">**Name**</span></span>|<span data-ttu-id="420bd-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="420bd-118">**Value**</span></span>|<span data-ttu-id="420bd-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="420bd-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="420bd-120">**ROHAUTH_BASIC**</span><span class="sxs-lookup"><span data-stu-id="420bd-120">**ROHAUTH_BASIC**</span></span> <br/> |<span data-ttu-id="420bd-121">0x1</span><span class="sxs-lookup"><span data-stu-id="420bd-121">0x1</span></span>  <br/> |<span data-ttu-id="420bd-122">Обычная проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="420bd-122">Basic authentication</span></span>  <br/> |
|<span data-ttu-id="420bd-123">**ROHAUTH_NTLM**</span><span class="sxs-lookup"><span data-stu-id="420bd-123">**ROHAUTH_NTLM**</span></span> <br/> |<span data-ttu-id="420bd-124">0x2</span><span class="sxs-lookup"><span data-stu-id="420bd-124">0x2</span></span>  <br/> |<span data-ttu-id="420bd-125">Проверка подлинности NTLM</span><span class="sxs-lookup"><span data-stu-id="420bd-125">NTLM authentication</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="420bd-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="420bd-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="420bd-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="420bd-127">Protocol specifications</span></span>

<span data-ttu-id="420bd-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="420bd-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="420bd-129">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="420bd-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="420bd-130">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="420bd-130">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="420bd-131">Определяет структуры основных данных, которые используются для удаленных операций.</span><span class="sxs-lookup"><span data-stu-id="420bd-131">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="420bd-132">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="420bd-132">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="420bd-133">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="420bd-133">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="420bd-134">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="420bd-134">Header files</span></span>

<span data-ttu-id="420bd-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="420bd-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="420bd-136">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="420bd-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="420bd-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="420bd-137">Mapitags.h</span></span>
  
> <span data-ttu-id="420bd-138">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="420bd-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="420bd-139">См. также</span><span class="sxs-lookup"><span data-stu-id="420bd-139">See also</span></span>



[<span data-ttu-id="420bd-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="420bd-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="420bd-141">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="420bd-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="420bd-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="420bd-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="420bd-143">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="420bd-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

