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
# <a name="itnefopentaggedbody"></a><span data-ttu-id="a0b99-103">ITnef::OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="a0b99-103">ITnef::OpenTaggedBody</span></span>

  
  
<span data-ttu-id="a0b99-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0b99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0b99-105">Открывает интерфейс потока в тексте инкапсулированного сообщения.</span><span class="sxs-lookup"><span data-stu-id="a0b99-105">Opens a stream interface on the text of an encapsulated message.</span></span>
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="a0b99-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0b99-106">Parameters</span></span>

 <span data-ttu-id="a0b99-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="a0b99-107">_lpMessage_</span></span>
  
> <span data-ttu-id="a0b99-108">[in] Указатель на сообщение, с которым связан поток.</span><span class="sxs-lookup"><span data-stu-id="a0b99-108">[in] A pointer to the message with which the stream is associated.</span></span> <span data-ttu-id="a0b99-109">Это сообщение не обязательно должно быть тем же сообщением, которое передается при вызове функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="a0b99-109">This message is not required to be the same message that is passed in the call to the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
 <span data-ttu-id="a0b99-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a0b99-110">_ulFlags_</span></span>
  
> <span data-ttu-id="a0b99-111">[in] Битоваяmas флагов, которая управляет открытием интерфейса потока.</span><span class="sxs-lookup"><span data-stu-id="a0b99-111">[in] A bitmask of flags that controls how the stream interface is opened.</span></span> <span data-ttu-id="a0b99-112">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="a0b99-112">The following flags can be set:</span></span>
    
<span data-ttu-id="a0b99-113">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="a0b99-113">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="a0b99-114">Если свойство не существует в текущем сообщении, его следует создать.</span><span class="sxs-lookup"><span data-stu-id="a0b99-114">If a property does not exist in the current message, it should be created.</span></span> <span data-ttu-id="a0b99-115">Если свойство существует, текущие данные в свойстве должны быть заменены данными из потока Transport-Neutral формата инкапсуляции (TNEF).</span><span class="sxs-lookup"><span data-stu-id="a0b99-115">If the property does exist, the current data in the property should be replaced with the data from the Transport-Neutral Encapsulation Format (TNEF) stream.</span></span> <span data-ttu-id="a0b99-116">Когда реализация устанавливает флаг MAPI_CREATE, она также должна MAPI_MODIFY флага.</span><span class="sxs-lookup"><span data-stu-id="a0b99-116">When an implementation sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="a0b99-117">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="a0b99-117">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="a0b99-118">Запрашивает разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="a0b99-118">Requests read/write permission.</span></span> <span data-ttu-id="a0b99-119">Интерфейс по умолчанию находится только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a0b99-119">The default interface is read-only.</span></span> <span data-ttu-id="a0b99-120">MAPI_MODIFY необходимо устанавливать каждый раз, MAPI_CREATE установлено.</span><span class="sxs-lookup"><span data-stu-id="a0b99-120">MAPI_MODIFY must be set whenever MAPI_CREATE is set.</span></span>
    
 <span data-ttu-id="a0b99-121">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="a0b99-121">_lppStream_</span></span>
  
> <span data-ttu-id="a0b99-122">[out] Указатель на указатель на объект потока, который содержит текст из свойства **PR_BODY** ([PidTagBody)](pidtagbody-canonical-property.md)переданного сообщения инкапсулированного сообщения, который поддерживает [интерфейс IStream.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream)</span><span class="sxs-lookup"><span data-stu-id="a0b99-122">[out] A pointer to a pointer to a stream object that contains the text from the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of the passed-in encapsulated message and that supports the [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a0b99-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0b99-123">Return value</span></span>

<span data-ttu-id="a0b99-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="a0b99-124">S_OK</span></span> 
  
> <span data-ttu-id="a0b99-125">Вызов был успешным и возвратил ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="a0b99-125">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0b99-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="a0b99-126">Remarks</span></span>

<span data-ttu-id="a0b99-127">Поставщики транспорта, поставщики хранимых сообщений и шлюзы вызывали метод **ITnef::OpenTaggedBody,** чтобы открыть интерфейс потока в тексте инкапсулированного сообщения (т. е. в объекте TNEF).</span><span class="sxs-lookup"><span data-stu-id="a0b99-127">Transport providers, message store providers, and gateways call the **ITnef::OpenTaggedBody** method to open a stream interface on the text of an encapsulated message (that is, on a TNEF object).</span></span> 
  
<span data-ttu-id="a0b99-128">В рамках обработки **OpenTaggedBody** вставляет или обрабатывает теги вложений, которые указывают положение любых вложений или объектов OLE в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="a0b99-128">As part of its processing, **OpenTaggedBody** either inserts or parses attachment tags that indicate the position of any attachments or OLE objects in the message text.</span></span> <span data-ttu-id="a0b99-129">Теги вложений имеют следующий формат:</span><span class="sxs-lookup"><span data-stu-id="a0b99-129">The attachment tags are in the following format:</span></span> 
  
 <span data-ttu-id="a0b99-130">**[[** _имя вложения:_  _n_ в **имени** _контейнера вложений_ **]]**</span><span class="sxs-lookup"><span data-stu-id="a0b99-130">**[[** _attachment name_ **:** _n_ **in** _attachment container name_ **]]**</span></span>
  
 <span data-ttu-id="a0b99-131">_имя вложения_ описывает объект вложения;  _n_ — это число, которое идентифицирует вложение, которое является частью последовательности, инкрементным от значения, переданного в  _параметре lpKey_ функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx;](opentnefstreamex.md) и  _имя контейнера вложений_ описывает физический компонент, в котором находится объект вложения.</span><span class="sxs-lookup"><span data-stu-id="a0b99-131">_attachment name_ describes the attachment object;  _n_ is a number that identifies the attachment that is part of a sequence, incrementing from the value passed in the  _lpKey_ parameter of the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function; and  _attachment container name_ describes the physical component where the attachment object resides.</span></span> 
  
 <span data-ttu-id="a0b99-132">**OpenTaggedBody** считывает текст сообщения и вставляет тег вложения везде, где изначально в тексте был объект вложения.</span><span class="sxs-lookup"><span data-stu-id="a0b99-132">**OpenTaggedBody** reads out message text and inserts an attachment tag wherever an attachment object originally appeared in the text.</span></span> <span data-ttu-id="a0b99-133">Исходный текст сообщения не меняется.</span><span class="sxs-lookup"><span data-stu-id="a0b99-133">The original message text is not changed.</span></span> 
  
<span data-ttu-id="a0b99-134">Когда сообщение с тегами передается в поток, теги срезаются, а объекты вложений находятся в положении тегов в потоке.</span><span class="sxs-lookup"><span data-stu-id="a0b99-134">When a message that has tags is passed to a stream, the tags are stripped out and the attachment objects are relocated in the position of the tags in the stream.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a0b99-135">См. также</span><span class="sxs-lookup"><span data-stu-id="a0b99-135">See also</span></span>



[<span data-ttu-id="a0b99-136">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="a0b99-136">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="a0b99-137">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="a0b99-137">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="a0b99-138">Каноническое свойство PidTagBody</span><span class="sxs-lookup"><span data-stu-id="a0b99-138">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)
  
[<span data-ttu-id="a0b99-139">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0b99-139">ITnef : IUnknown</span></span>](itnefiunknown.md)

