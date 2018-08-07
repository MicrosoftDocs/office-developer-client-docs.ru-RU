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
ms.openlocfilehash: 151aa730f2ae6a4d39ffa474eb7ecd79ed5602eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811743"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a><span data-ttu-id="2bd0a-103">Каноническое свойство PidTagRpcOverHttpFlags</span><span class="sxs-lookup"><span data-stu-id="2bd0a-103">PidTagRpcOverHttpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="2bd0a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2bd0a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2bd0a-105">Содержит параметры профиля, используемые Microsoft Office Outlook для подключения к Microsoft Exchange Server с помощью удаленный вызов процедур (RPC) по протоколу (HTTP).</span><span class="sxs-lookup"><span data-stu-id="2bd0a-105">Contains the settings in a profile used by Microsoft Office Outlook to connect to Microsoft Exchange Server by using a remote procedure call (RPC) over Hypertext Transfer Protocol (HTTP).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2bd0a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2bd0a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2bd0a-107">PR_ROH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="2bd0a-107">PR_ROH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="2bd0a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2bd0a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2bd0a-109">0x6623</span><span class="sxs-lookup"><span data-stu-id="2bd0a-109">0x6623</span></span>  <br/> |
|<span data-ttu-id="2bd0a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2bd0a-110">Data type:</span></span>  <br/> |<span data-ttu-id="2bd0a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2bd0a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2bd0a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2bd0a-112">Area:</span></span>  <br/> |<span data-ttu-id="2bd0a-113">Разное</span><span class="sxs-lookup"><span data-stu-id="2bd0a-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2bd0a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2bd0a-114">Remarks</span></span>

<span data-ttu-id="2bd0a-115">Свойство **PR_ROH_FLAGS** хранится в разделе глобальные профиля в профиль по программированию интерфейса MAPI (Messaging Application).</span><span class="sxs-lookup"><span data-stu-id="2bd0a-115">The **PR_ROH_FLAGS** property is stored in the Global Profile Section of a Messaging Application Programming Interface (MAPI) profile.</span></span> <span data-ttu-id="2bd0a-116">Значение **PR_ROH_FLAGS** является битовой маской, состоящий из одного или нескольких из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-116">The value of **PR_ROH_FLAGS** is a bitmask that is made up of one or more of the following flags.</span></span> 
  
|<span data-ttu-id="2bd0a-117">**Имя**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-117">**Name**</span></span>|<span data-ttu-id="2bd0a-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-118">**Value**</span></span>|<span data-ttu-id="2bd0a-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2bd0a-120">**ROHFLAGS_USE_ROH**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-120">**ROHFLAGS_USE_ROH**</span></span> <br/> |<span data-ttu-id="2bd0a-121">0x1</span><span class="sxs-lookup"><span data-stu-id="2bd0a-121">0x1</span></span>  <br/> |<span data-ttu-id="2bd0a-122">Подключитесь к серверу Exchange, используя протокол RPC over HTTP.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-122">Connect to the Exchange Server using RPC over HTTP.</span></span>  <br/> |
|<span data-ttu-id="2bd0a-123">**ROHFLAGS_SSL_ONLY**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-123">**ROHFLAGS_SSL_ONLY**</span></span> <br/> |<span data-ttu-id="2bd0a-124">0x2</span><span class="sxs-lookup"><span data-stu-id="2bd0a-124">0x2</span></span>  <br/> |<span data-ttu-id="2bd0a-125">Подключитесь к серверу Exchange, только с помощью Secure сокетов протокол SSL.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-125">Connect to the Exchange Server using Secure Socket Layer (SSL) only.</span></span>  <br/> |
|<span data-ttu-id="2bd0a-126">**ROHFLAGS_MUTUAL_AUTH**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-126">**ROHFLAGS_MUTUAL_AUTH**</span></span> <br/> |<span data-ttu-id="2bd0a-127">0x4</span><span class="sxs-lookup"><span data-stu-id="2bd0a-127">0x4</span></span>  <br/> |<span data-ttu-id="2bd0a-128">Взаимная проверка подлинности сеанса при подключении с помощью протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-128">Mutually authenticate the session when connecting by using SSL.</span></span>  <br/> |
|<span data-ttu-id="2bd0a-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span></span> <br/> |<span data-ttu-id="2bd0a-130">0x8</span><span class="sxs-lookup"><span data-stu-id="2bd0a-130">0x8</span></span>  <br/> |<span data-ttu-id="2bd0a-131">В быстрых сетях: подключение по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-131">On fast networks, connect by using HTTP first.</span></span> <span data-ttu-id="2bd0a-132">Подключитесь с помощью протокола TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-132">Then, connect by using TCP/IP.</span></span>  <br/> |
|<span data-ttu-id="2bd0a-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span><span class="sxs-lookup"><span data-stu-id="2bd0a-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span></span> <br/> |<span data-ttu-id="2bd0a-134">0x20</span><span class="sxs-lookup"><span data-stu-id="2bd0a-134">0x20</span></span>  <br/> |<span data-ttu-id="2bd0a-135">В медленных сетях: подключение по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-135">On slow networks, connect by using HTTP first.</span></span> <span data-ttu-id="2bd0a-136">Подключитесь с помощью протокола TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-136">Then, connect by using TCP/IP.</span></span>  <br/> |
   
<span data-ttu-id="2bd0a-137">Например, установка **PR_ROH_FLAGS** свойство, чтобы включить RPC через HTTP, протокол SSL, а также указать, следует сначала использовать протокол HTTP при медленном подключении задайте значение свойства **PR_ROH_FLAGS** для `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` которого равен 0x23.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-137">For example, to set the **PR_ROH_FLAGS** property to turn on RPC over HTTP, to require SSL, and to specify that the HTTP protocol should be used first on slow connections, set the value of the **PR_ROH_FLAGS** property to  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` which is equal to 0x23.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2bd0a-138">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2bd0a-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2bd0a-139">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2bd0a-139">Protocol specifications</span></span>

<span data-ttu-id="2bd0a-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2bd0a-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2bd0a-141">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2bd0a-142">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2bd0a-142">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2bd0a-143">Определяет структуры основных данных, которые используются для удаленных операций.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-143">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="2bd0a-144">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2bd0a-144">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2bd0a-145">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-145">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2bd0a-146">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2bd0a-146">Header files</span></span>

<span data-ttu-id="2bd0a-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2bd0a-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="2bd0a-148">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="2bd0a-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2bd0a-149">Mapitags.h</span></span>
  
> <span data-ttu-id="2bd0a-150">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="2bd0a-150">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2bd0a-151">См. также</span><span class="sxs-lookup"><span data-stu-id="2bd0a-151">See also</span></span>



[<span data-ttu-id="2bd0a-152">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2bd0a-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2bd0a-153">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2bd0a-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2bd0a-154">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2bd0a-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2bd0a-155">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2bd0a-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

