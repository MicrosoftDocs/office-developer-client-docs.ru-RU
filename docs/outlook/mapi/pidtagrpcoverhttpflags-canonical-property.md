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
# <a name="pidtagrpcoverhttpflags-canonical-property"></a><span data-ttu-id="b8c66-103">Каноническое свойство PidTagRpcOverHttpFlags</span><span class="sxs-lookup"><span data-stu-id="b8c66-103">PidTagRpcOverHttpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="b8c66-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8c66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8c66-105">Содержит параметры профиля, используемого Microsoft Office Outlook для подключения к Microsoft Exchange Server с помощью удаленного вызова процедур (RPC) по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="b8c66-105">Contains the settings in a profile used by Microsoft Office Outlook to connect to Microsoft Exchange Server by using a remote procedure call (RPC) over Hypertext Transfer Protocol (HTTP).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b8c66-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b8c66-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b8c66-107">ПР_РОХ_ФЛАГС</span><span class="sxs-lookup"><span data-stu-id="b8c66-107">PR_ROH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="b8c66-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b8c66-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b8c66-109">0x6623</span><span class="sxs-lookup"><span data-stu-id="b8c66-109">0x6623</span></span>  <br/> |
|<span data-ttu-id="b8c66-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b8c66-110">Data type:</span></span>  <br/> |<span data-ttu-id="b8c66-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b8c66-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b8c66-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b8c66-112">Area:</span></span>  <br/> |<span data-ttu-id="b8c66-113">Разное</span><span class="sxs-lookup"><span data-stu-id="b8c66-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8c66-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b8c66-114">Remarks</span></span>

<span data-ttu-id="b8c66-115">Свойство **пр_рох_флагс** хранится в разделе глобального профиля в профиле MAPI.</span><span class="sxs-lookup"><span data-stu-id="b8c66-115">The **PR_ROH_FLAGS** property is stored in the Global Profile Section of a Messaging Application Programming Interface (MAPI) profile.</span></span> <span data-ttu-id="b8c66-116">Значение **пр_рох_флагс** — это битовая маска, состоящего из одного или нескольких из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="b8c66-116">The value of **PR_ROH_FLAGS** is a bitmask that is made up of one or more of the following flags.</span></span> 
  
|<span data-ttu-id="b8c66-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="b8c66-117">**Name**</span></span>|<span data-ttu-id="b8c66-118">**Value**</span><span class="sxs-lookup"><span data-stu-id="b8c66-118">**Value**</span></span>|<span data-ttu-id="b8c66-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b8c66-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b8c66-120">**РОХФЛАГС_УСЕ_РОХ**</span><span class="sxs-lookup"><span data-stu-id="b8c66-120">**ROHFLAGS_USE_ROH**</span></span> <br/> |<span data-ttu-id="b8c66-121">0x1</span><span class="sxs-lookup"><span data-stu-id="b8c66-121">0x1</span></span>  <br/> |<span data-ttu-id="b8c66-122">Подключитесь к серверу Exchange Server с помощью RPC через HTTP.</span><span class="sxs-lookup"><span data-stu-id="b8c66-122">Connect to the Exchange Server using RPC over HTTP.</span></span>  <br/> |
|<span data-ttu-id="b8c66-123">**РОХФЛАГС_ССЛ_ОНЛИ**</span><span class="sxs-lookup"><span data-stu-id="b8c66-123">**ROHFLAGS_SSL_ONLY**</span></span> <br/> |<span data-ttu-id="b8c66-124">0x2</span><span class="sxs-lookup"><span data-stu-id="b8c66-124">0x2</span></span>  <br/> |<span data-ttu-id="b8c66-125">Подключитесь к серверу Exchange по ПРОТОКОЛу SSL (Secure Socket Layer).</span><span class="sxs-lookup"><span data-stu-id="b8c66-125">Connect to the Exchange Server using Secure Socket Layer (SSL) only.</span></span>  <br/> |
|<span data-ttu-id="b8c66-126">**РОХФЛАГС_МУТУАЛ_АУС**</span><span class="sxs-lookup"><span data-stu-id="b8c66-126">**ROHFLAGS_MUTUAL_AUTH**</span></span> <br/> |<span data-ttu-id="b8c66-127">0x4</span><span class="sxs-lookup"><span data-stu-id="b8c66-127">0x4</span></span>  <br/> |<span data-ttu-id="b8c66-128">Взаимная проверка подлинности сеанса при подключении с использованием протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="b8c66-128">Mutually authenticate the session when connecting by using SSL.</span></span>  <br/> |
|<span data-ttu-id="b8c66-129">**РОХФЛАГС_ХТТП_ФИРСТ_ОН_ФАСТ**</span><span class="sxs-lookup"><span data-stu-id="b8c66-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span></span> <br/> |<span data-ttu-id="b8c66-130">0x8</span><span class="sxs-lookup"><span data-stu-id="b8c66-130">0x8</span></span>  <br/> |<span data-ttu-id="b8c66-131">В быстрых сетях подключение сначала осуществляется с помощью HTTP.</span><span class="sxs-lookup"><span data-stu-id="b8c66-131">On fast networks, connect by using HTTP first.</span></span> <span data-ttu-id="b8c66-132">Затем подключитесь с помощью TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="b8c66-132">Then, connect by using TCP/IP.</span></span>  <br/> |
|<span data-ttu-id="b8c66-133">**РОХФЛАГС_ХТТП_ФИРСТ_ОН_СЛОВ**</span><span class="sxs-lookup"><span data-stu-id="b8c66-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span></span> <br/> |<span data-ttu-id="b8c66-134">0x20</span><span class="sxs-lookup"><span data-stu-id="b8c66-134">0x20</span></span>  <br/> |<span data-ttu-id="b8c66-135">В медленных сетях подключение сначала осуществляется с помощью HTTP.</span><span class="sxs-lookup"><span data-stu-id="b8c66-135">On slow networks, connect by using HTTP first.</span></span> <span data-ttu-id="b8c66-136">Затем подключитесь с помощью TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="b8c66-136">Then, connect by using TCP/IP.</span></span>  <br/> |
   
<span data-ttu-id="b8c66-137">Например, чтобы задать для свойства **пр_рох_флагс** включение RPC через HTTP, для требования использования протокола SSL и указания того, что протокол HTTP должен использоваться первым при медленных подключениях, задайте для `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` свойства **пр_рох_флагс** значение, равное 0x23.</span><span class="sxs-lookup"><span data-stu-id="b8c66-137">For example, to set the **PR_ROH_FLAGS** property to turn on RPC over HTTP, to require SSL, and to specify that the HTTP protocol should be used first on slow connections, set the value of the **PR_ROH_FLAGS** property to  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` which is equal to 0x23.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b8c66-138">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b8c66-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b8c66-139">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b8c66-139">Protocol specifications</span></span>

<span data-ttu-id="b8c66-140">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8c66-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8c66-141">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b8c66-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b8c66-142">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8c66-142">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8c66-143">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="b8c66-143">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="b8c66-144">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8c66-144">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8c66-145">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="b8c66-145">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b8c66-146">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="b8c66-146">Header files</span></span>

<span data-ttu-id="b8c66-147">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b8c66-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="b8c66-148">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b8c66-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="b8c66-149">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="b8c66-149">Mapitags.h</span></span>
  
> <span data-ttu-id="b8c66-150">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="b8c66-150">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b8c66-151">См. также</span><span class="sxs-lookup"><span data-stu-id="b8c66-151">See also</span></span>



[<span data-ttu-id="b8c66-152">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b8c66-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b8c66-153">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="b8c66-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b8c66-154">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b8c66-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b8c66-155">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b8c66-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

