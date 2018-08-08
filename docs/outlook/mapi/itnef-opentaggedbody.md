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
ms.openlocfilehash: ed433dc1fcf2a366d2ece07ac06d4e12558e4aa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809606"
---
# <a name="itnefopentaggedbody"></a><span data-ttu-id="be940-103">ITnef::OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="be940-103">ITnef::OpenTaggedBody</span></span>

  
  
<span data-ttu-id="be940-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="be940-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="be940-105">Открывает интерфейс потока на основе текста инкапсулированное сообщение.</span><span class="sxs-lookup"><span data-stu-id="be940-105">Opens a stream interface on the text of an encapsulated message.</span></span>
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="be940-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="be940-106">Parameters</span></span>

 <span data-ttu-id="be940-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="be940-107">_lpMessage_</span></span>
  
> <span data-ttu-id="be940-108">[in] Указатель на сообщение, с которым связано потока.</span><span class="sxs-lookup"><span data-stu-id="be940-108">[in] A pointer to the message with which the stream is associated.</span></span> <span data-ttu-id="be940-109">Это сообщение не требуется, чтобы то же сообщение, которое передается в вызове функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="be940-109">This message is not required to be the same message that is passed in the call to the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
 <span data-ttu-id="be940-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="be940-110">_ulFlags_</span></span>
  
> <span data-ttu-id="be940-111">[in] Битовая маска флаги, который определяет, как открыть интерфейс потока.</span><span class="sxs-lookup"><span data-stu-id="be940-111">[in] A bitmask of flags that controls how the stream interface is opened.</span></span> <span data-ttu-id="be940-112">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="be940-112">The following flags can be set:</span></span>
    
<span data-ttu-id="be940-113">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="be940-113">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="be940-114">Если свойство не существует в текущем сообщении, он должен быть создан.</span><span class="sxs-lookup"><span data-stu-id="be940-114">If a property does not exist in the current message, it should be created.</span></span> <span data-ttu-id="be940-115">Если свойство существует, следует заменить текущие данные в свойстве с данными в потоке Transport-Neutral Encapsulation формата TNEF ().</span><span class="sxs-lookup"><span data-stu-id="be940-115">If the property does exist, the current data in the property should be replaced with the data from the Transport-Neutral Encapsulation Format (TNEF) stream.</span></span> <span data-ttu-id="be940-116">При реализации задает флаг MAPI_CREATE, он должен установить флаг MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="be940-116">When an implementation sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="be940-117">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="be940-117">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="be940-118">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="be940-118">Requests read/write permission.</span></span> <span data-ttu-id="be940-119">Интерфейс по умолчанию доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="be940-119">The default interface is read-only.</span></span> <span data-ttu-id="be940-120">При использовании MAPI_CREATE необходимо установить MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="be940-120">MAPI_MODIFY must be set whenever MAPI_CREATE is set.</span></span>
    
 <span data-ttu-id="be940-121">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="be940-121">_lppStream_</span></span>
  
> <span data-ttu-id="be940-122">[out] Указатель на указатель на объект потока, который содержит текст из свойства **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) передается в инкапсулированное сообщение, которая поддерживает интерфейс [IStream](http://msdn.microsoft.com/library/stg.istream%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="be940-122">[out] A pointer to a pointer to a stream object that contains the text from the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of the passed-in encapsulated message and that supports the [IStream](http://msdn.microsoft.com/library/stg.istream%28Office.15%29.aspx) interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="be940-123">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="be940-123">Return value</span></span>

<span data-ttu-id="be940-124">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="be940-124">S_OK</span></span> 
  
> <span data-ttu-id="be940-125">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="be940-125">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="be940-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="be940-126">Remarks</span></span>

<span data-ttu-id="be940-127">Поставщики транспорта, поставщиков хранилища сообщений и шлюзов вызовите метод **ITnef::OpenTaggedBody** для открытия интерфейс потока на основе текста инкапсулированное сообщение (то есть на TNEF объектов).</span><span class="sxs-lookup"><span data-stu-id="be940-127">Transport providers, message store providers, and gateways call the **ITnef::OpenTaggedBody** method to open a stream interface on the text of an encapsulated message (that is, on a TNEF object).</span></span> 
  
<span data-ttu-id="be940-128">В процессе обработки **OpenTaggedBody** вставляет или анализирует теги вложения, которые указывают положения любого вложения или объекты OLE в качестве текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="be940-128">As part of its processing, **OpenTaggedBody** either inserts or parses attachment tags that indicate the position of any attachments or OLE objects in the message text.</span></span> <span data-ttu-id="be940-129">Теги вложения, в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="be940-129">The attachment tags are in the following format:</span></span> 
  
 <span data-ttu-id="be940-130">**[[** _имя вложения_ **:** _n_ **в** _имени контейнера вложения_ **]]**</span><span class="sxs-lookup"><span data-stu-id="be940-130">**[[** _attachment name_ **:** _n_ **in** _attachment container name_ **]]**</span></span>
  
 <span data-ttu-id="be940-131">_имя вложения_ описывает объект вложения;  _n_ — это число, определяющее вложения, который является частью последовательности, увеличивающееся из значение, переданное в параметре _lpKey_ [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx](opentnefstreamex.md) функции; и _имени контейнера вложения_ описывает физические компоненты, где находится объект вложения.</span><span class="sxs-lookup"><span data-stu-id="be940-131">_attachment name_ describes the attachment object;  _n_ is a number that identifies the attachment that is part of a sequence, incrementing from the value passed in the  _lpKey_ parameter of the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function; and  _attachment container name_ describes the physical component where the attachment object resides.</span></span> 
  
 <span data-ttu-id="be940-132">**OpenTaggedBody** считывает текст сообщения и вставляет тег вложения везде, где объект вложения был записан в текст.</span><span class="sxs-lookup"><span data-stu-id="be940-132">**OpenTaggedBody** reads out message text and inserts an attachment tag wherever an attachment object originally appeared in the text.</span></span> <span data-ttu-id="be940-133">Текст исходного сообщения не изменяется.</span><span class="sxs-lookup"><span data-stu-id="be940-133">The original message text is not changed.</span></span> 
  
<span data-ttu-id="be940-134">При передаче сообщения с тегами потока, перечень тегов, будут опущены и объекты вложения будут перемещены в положение теги в потоке.</span><span class="sxs-lookup"><span data-stu-id="be940-134">When a message that has tags is passed to a stream, the tags are stripped out and the attachment objects are relocated in the position of the tags in the stream.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="be940-135">См. также</span><span class="sxs-lookup"><span data-stu-id="be940-135">See also</span></span>



[<span data-ttu-id="be940-136">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="be940-136">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="be940-137">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="be940-137">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="be940-138">Каноническое свойство PidTagBody</span><span class="sxs-lookup"><span data-stu-id="be940-138">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)
  
[<span data-ttu-id="be940-139">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be940-139">ITnef : IUnknown</span></span>](itnefiunknown.md)

