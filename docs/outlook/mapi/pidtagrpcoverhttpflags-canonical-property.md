---
title: Каноническое свойство PidTagRpcOverHttpFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cf1f3b4d72426fb5f80decdc074a622b140657c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327449"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a><span data-ttu-id="74e92-103">Каноническое свойство PidTagRpcOverHttpFlags</span><span class="sxs-lookup"><span data-stu-id="74e92-103">PidTagRpcOverHttpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="74e92-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74e92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74e92-105">Содержит параметры в профиле, используемом Microsoft Office Outlook для подключения к Microsoft Exchange Server с помощью удаленного вызова процедуры (RPC) над протоколом передачи Hypertext (HTTP).</span><span class="sxs-lookup"><span data-stu-id="74e92-105">Contains the settings in a profile used by Microsoft Office Outlook to connect to Microsoft Exchange Server by using a remote procedure call (RPC) over Hypertext Transfer Protocol (HTTP).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74e92-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="74e92-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74e92-107">PR_ROH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="74e92-107">PR_ROH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="74e92-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="74e92-108">Identifier:</span></span>  <br/> |<span data-ttu-id="74e92-109">0x6623</span><span class="sxs-lookup"><span data-stu-id="74e92-109">0x6623</span></span>  <br/> |
|<span data-ttu-id="74e92-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="74e92-110">Data type:</span></span>  <br/> |<span data-ttu-id="74e92-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="74e92-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="74e92-112">Область:</span><span class="sxs-lookup"><span data-stu-id="74e92-112">Area:</span></span>  <br/> |<span data-ttu-id="74e92-113">Разное</span><span class="sxs-lookup"><span data-stu-id="74e92-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74e92-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="74e92-114">Remarks</span></span>

<span data-ttu-id="74e92-115">Свойство **PR_ROH_FLAGS** хранится в разделе Глобальный профиль интерфейса программирования приложений для обмена сообщениями (MAPI).</span><span class="sxs-lookup"><span data-stu-id="74e92-115">The **PR_ROH_FLAGS** property is stored in the Global Profile Section of a Messaging Application Programming Interface (MAPI) profile.</span></span> <span data-ttu-id="74e92-116">Значение PR_ROH_FLAGS **—** битмаска, которая состоит из одного или более из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="74e92-116">The value of **PR_ROH_FLAGS** is a bitmask that is made up of one or more of the following flags.</span></span> 
  
|<span data-ttu-id="74e92-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="74e92-117">**Name**</span></span>|<span data-ttu-id="74e92-118">**Value**</span><span class="sxs-lookup"><span data-stu-id="74e92-118">**Value**</span></span>|<span data-ttu-id="74e92-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="74e92-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="74e92-120">**ROHFLAGS_USE_ROH**</span><span class="sxs-lookup"><span data-stu-id="74e92-120">**ROHFLAGS_USE_ROH**</span></span> <br/> |<span data-ttu-id="74e92-121">0x1</span><span class="sxs-lookup"><span data-stu-id="74e92-121">0x1</span></span>  <br/> |<span data-ttu-id="74e92-122">Подключение на Exchange Server С ПОМОЩЬЮ RPC над HTTP.</span><span class="sxs-lookup"><span data-stu-id="74e92-122">Connect to the Exchange Server using RPC over HTTP.</span></span>  <br/> |
|<span data-ttu-id="74e92-123">**ROHFLAGS_SSL_ONLY**</span><span class="sxs-lookup"><span data-stu-id="74e92-123">**ROHFLAGS_SSL_ONLY**</span></span> <br/> |<span data-ttu-id="74e92-124">0x2</span><span class="sxs-lookup"><span data-stu-id="74e92-124">0x2</span></span>  <br/> |<span data-ttu-id="74e92-125">Подключение для Exchange Server только с помощью безопасного слоя socket (SSL).</span><span class="sxs-lookup"><span data-stu-id="74e92-125">Connect to the Exchange Server using Secure Socket Layer (SSL) only.</span></span>  <br/> |
|<span data-ttu-id="74e92-126">**ROHFLAGS_MUTUAL_AUTH**</span><span class="sxs-lookup"><span data-stu-id="74e92-126">**ROHFLAGS_MUTUAL_AUTH**</span></span> <br/> |<span data-ttu-id="74e92-127">0x4</span><span class="sxs-lookup"><span data-stu-id="74e92-127">0x4</span></span>  <br/> |<span data-ttu-id="74e92-128">Взаимно проверка подлинности сеанса при подключении с помощью SSL.</span><span class="sxs-lookup"><span data-stu-id="74e92-128">Mutually authenticate the session when connecting by using SSL.</span></span>  <br/> |
|<span data-ttu-id="74e92-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span><span class="sxs-lookup"><span data-stu-id="74e92-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span></span> <br/> |<span data-ttu-id="74e92-130">0x8</span><span class="sxs-lookup"><span data-stu-id="74e92-130">0x8</span></span>  <br/> |<span data-ttu-id="74e92-131">В быстрых сетях сначала подключайтесь с помощью HTTP.</span><span class="sxs-lookup"><span data-stu-id="74e92-131">On fast networks, connect by using HTTP first.</span></span> <span data-ttu-id="74e92-132">Затем подключите с помощью TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="74e92-132">Then, connect by using TCP/IP.</span></span>  <br/> |
|<span data-ttu-id="74e92-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span><span class="sxs-lookup"><span data-stu-id="74e92-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span></span> <br/> |<span data-ttu-id="74e92-134">0x20</span><span class="sxs-lookup"><span data-stu-id="74e92-134">0x20</span></span>  <br/> |<span data-ttu-id="74e92-135">В медленных сетях сначала подключайтесь с помощью HTTP.</span><span class="sxs-lookup"><span data-stu-id="74e92-135">On slow networks, connect by using HTTP first.</span></span> <span data-ttu-id="74e92-136">Затем подключите с помощью TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="74e92-136">Then, connect by using TCP/IP.</span></span>  <br/> |
   
<span data-ttu-id="74e92-137">Например, чтобы задать свойство **PR_ROH_FLAGS** включить RPC над HTTP, потребовать SSL и указать, что протокол HTTP следует использовать сначала при медленных подключениях, установите значение свойства **PR_ROH_FLAGS,** равное  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` 0x23.</span><span class="sxs-lookup"><span data-stu-id="74e92-137">For example, to set the **PR_ROH_FLAGS** property to turn on RPC over HTTP, to require SSL, and to specify that the HTTP protocol should be used first on slow connections, set the value of the **PR_ROH_FLAGS** property to  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` which is equal to 0x23.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="74e92-138">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="74e92-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="74e92-139">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="74e92-139">Protocol specifications</span></span>

<span data-ttu-id="74e92-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74e92-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74e92-141">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="74e92-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="74e92-142">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74e92-142">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74e92-143">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="74e92-143">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="74e92-144">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74e92-144">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74e92-145">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="74e92-145">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="74e92-146">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="74e92-146">Header files</span></span>

<span data-ttu-id="74e92-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74e92-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="74e92-148">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="74e92-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="74e92-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="74e92-149">Mapitags.h</span></span>
  
> <span data-ttu-id="74e92-150">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="74e92-150">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74e92-151">См. также</span><span class="sxs-lookup"><span data-stu-id="74e92-151">See also</span></span>



[<span data-ttu-id="74e92-152">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="74e92-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74e92-153">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="74e92-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74e92-154">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="74e92-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74e92-155">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="74e92-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

