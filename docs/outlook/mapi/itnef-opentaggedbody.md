---
title: ITnefOpenTaggedBody
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.OpenTaggedBody
api_type:
- COM
ms.assetid: 70d5b34c-85b3-4d1f-860e-2838947ba428
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 154d6e4a4e333f3a6165c3875bdcd57957ebf70c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348736"
---
# <a name="itnefopentaggedbody"></a><span data-ttu-id="44bac-103">ITnef::OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="44bac-103">ITnef::OpenTaggedBody</span></span>

  
  
<span data-ttu-id="44bac-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44bac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44bac-105">Открывает интерфейс потока в тексте инкапсулированного сообщения.</span><span class="sxs-lookup"><span data-stu-id="44bac-105">Opens a stream interface on the text of an encapsulated message.</span></span>
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="44bac-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="44bac-106">Parameters</span></span>

 <span data-ttu-id="44bac-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="44bac-107">_lpMessage_</span></span>
  
> <span data-ttu-id="44bac-108">[in] Указатель на сообщение, с которым связан поток.</span><span class="sxs-lookup"><span data-stu-id="44bac-108">[in] A pointer to the message with which the stream is associated.</span></span> <span data-ttu-id="44bac-109">Это сообщение не обязательно должно быть таким же сообщением, которое передается в вызов функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="44bac-109">This message is not required to be the same message that is passed in the call to the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
 <span data-ttu-id="44bac-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="44bac-110">_ulFlags_</span></span>
  
> <span data-ttu-id="44bac-111">[in] Немного флагов, которые контролируют открытие интерфейса потока.</span><span class="sxs-lookup"><span data-stu-id="44bac-111">[in] A bitmask of flags that controls how the stream interface is opened.</span></span> <span data-ttu-id="44bac-112">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="44bac-112">The following flags can be set:</span></span>
    
<span data-ttu-id="44bac-113">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="44bac-113">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="44bac-114">Если свойство не существует в текущем сообщении, оно должно быть создано.</span><span class="sxs-lookup"><span data-stu-id="44bac-114">If a property does not exist in the current message, it should be created.</span></span> <span data-ttu-id="44bac-115">Если свойство существует, текущие данные в свойстве должны быть заменены данными из Transport-Neutral формата Инкапсуляции (TNEF).</span><span class="sxs-lookup"><span data-stu-id="44bac-115">If the property does exist, the current data in the property should be replaced with the data from the Transport-Neutral Encapsulation Format (TNEF) stream.</span></span> <span data-ttu-id="44bac-116">Если реализация задает флаг MAPI_CREATE, она также должна установить MAPI_MODIFY флаг.</span><span class="sxs-lookup"><span data-stu-id="44bac-116">When an implementation sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="44bac-117">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="44bac-117">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="44bac-118">Запросы на чтение и написание разрешений.</span><span class="sxs-lookup"><span data-stu-id="44bac-118">Requests read/write permission.</span></span> <span data-ttu-id="44bac-119">Интерфейс по умолчанию только для чтения.</span><span class="sxs-lookup"><span data-stu-id="44bac-119">The default interface is read-only.</span></span> <span data-ttu-id="44bac-120">MAPI_MODIFY должны быть установлены всякий раз, MAPI_CREATE установлено.</span><span class="sxs-lookup"><span data-stu-id="44bac-120">MAPI_MODIFY must be set whenever MAPI_CREATE is set.</span></span>
    
 <span data-ttu-id="44bac-121">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="44bac-121">_lppStream_</span></span>
  
> <span data-ttu-id="44bac-122">[вышел] Указатель на указатель на объект **потока,** содержащий текст из свойства [PR_BODY (PidTagBody)](pidtagbody-canonical-property.md)инкапсулированного сообщения, поддерживаемого интерфейсом [IStream.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream)</span><span class="sxs-lookup"><span data-stu-id="44bac-122">[out] A pointer to a pointer to a stream object that contains the text from the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of the passed-in encapsulated message and that supports the [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="44bac-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44bac-123">Return value</span></span>

<span data-ttu-id="44bac-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="44bac-124">S_OK</span></span> 
  
> <span data-ttu-id="44bac-125">Вызов удался и возвращает ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="44bac-125">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="44bac-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="44bac-126">Remarks</span></span>

<span data-ttu-id="44bac-127">Поставщики транспорта, поставщики магазинов сообщений и шлюзы звонят по методу **ITnef::OpenTaggedBody,** чтобы открыть интерфейс потока в тексте инкапсулированного сообщения (т. е. на объекте TNEF).</span><span class="sxs-lookup"><span data-stu-id="44bac-127">Transport providers, message store providers, and gateways call the **ITnef::OpenTaggedBody** method to open a stream interface on the text of an encapsulated message (that is, on a TNEF object).</span></span> 
  
<span data-ttu-id="44bac-128">В рамках своей обработки **OpenTaggedBody** вставляет или обрабатывает теги вложений, которые указывают расположение любых вложений или объектов OLE в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="44bac-128">As part of its processing, **OpenTaggedBody** either inserts or parses attachment tags that indicate the position of any attachments or OLE objects in the message text.</span></span> <span data-ttu-id="44bac-129">Теги вложений находятся в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="44bac-129">The attachment tags are in the following format:</span></span> 
  
 <span data-ttu-id="44bac-130">**[[** _имя вложения:_  _n в_  _имени контейнера вложения]]_ </span><span class="sxs-lookup"><span data-stu-id="44bac-130">**[[** _attachment name_ **:** _n_ **in** _attachment container name_ **]]**</span></span>
  
 <span data-ttu-id="44bac-131">_Имя вложения_ описывает объект вложения;  _n_ — это число, которое определяет вложение, которое является частью последовательности, инкрементное значение, переданное в  _параметре lpKey_ функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx;](opentnefstreamex.md) и  _имя контейнера вложения_ описывает физический компонент, в котором находится объект вложения.</span><span class="sxs-lookup"><span data-stu-id="44bac-131">_attachment name_ describes the attachment object;  _n_ is a number that identifies the attachment that is part of a sequence, incrementing from the value passed in the  _lpKey_ parameter of the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function; and  _attachment container name_ describes the physical component where the attachment object resides.</span></span> 
  
 <span data-ttu-id="44bac-132">**OpenTaggedBody** считывает текст сообщения и вставляет тег вложения везде, где изначально в тексте появился объект вложения.</span><span class="sxs-lookup"><span data-stu-id="44bac-132">**OpenTaggedBody** reads out message text and inserts an attachment tag wherever an attachment object originally appeared in the text.</span></span> <span data-ttu-id="44bac-133">Исходный текст сообщения не изменен.</span><span class="sxs-lookup"><span data-stu-id="44bac-133">The original message text is not changed.</span></span> 
  
<span data-ttu-id="44bac-134">Когда сообщение с тегами передается потоку, теги отсеяются, а объекты вложений будут размещены в расположении тегов в потоке.</span><span class="sxs-lookup"><span data-stu-id="44bac-134">When a message that has tags is passed to a stream, the tags are stripped out and the attachment objects are relocated in the position of the tags in the stream.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="44bac-135">См. также</span><span class="sxs-lookup"><span data-stu-id="44bac-135">See also</span></span>



[<span data-ttu-id="44bac-136">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="44bac-136">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="44bac-137">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="44bac-137">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="44bac-138">Каноническое свойство PidTagBody</span><span class="sxs-lookup"><span data-stu-id="44bac-138">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)
  
[<span data-ttu-id="44bac-139">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="44bac-139">ITnef : IUnknown</span></span>](itnefiunknown.md)

