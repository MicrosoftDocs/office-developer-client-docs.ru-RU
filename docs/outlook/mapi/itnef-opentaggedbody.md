---
title: Итнефопентагжедбоди
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
# <a name="itnefopentaggedbody"></a><span data-ttu-id="316a2-103">ITnef::OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="316a2-103">ITnef::OpenTaggedBody</span></span>

  
  
<span data-ttu-id="316a2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="316a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="316a2-105">Открывает потоковый интерфейс на тексте инкапсулированного сообщения.</span><span class="sxs-lookup"><span data-stu-id="316a2-105">Opens a stream interface on the text of an encapsulated message.</span></span>
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="316a2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="316a2-106">Parameters</span></span>

 <span data-ttu-id="316a2-107">_Лпмессаже_</span><span class="sxs-lookup"><span data-stu-id="316a2-107">_lpMessage_</span></span>
  
> <span data-ttu-id="316a2-108">возврата Указатель на сообщение, с которым связан поток.</span><span class="sxs-lookup"><span data-stu-id="316a2-108">[in] A pointer to the message with which the stream is associated.</span></span> <span data-ttu-id="316a2-109">Это сообщение не обязательно должно совпадать с сообщением, передаваемым при вызове функции [опентнефстреам](opentnefstream.md) или [опентнефстреамекс](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="316a2-109">This message is not required to be the same message that is passed in the call to the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
 <span data-ttu-id="316a2-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="316a2-110">_ulFlags_</span></span>
  
> <span data-ttu-id="316a2-111">возврата Битовая маска флагов, которые управляют способом открытия интерфейса потока.</span><span class="sxs-lookup"><span data-stu-id="316a2-111">[in] A bitmask of flags that controls how the stream interface is opened.</span></span> <span data-ttu-id="316a2-112">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="316a2-112">The following flags can be set:</span></span>
    
<span data-ttu-id="316a2-113">МАПИ_КРЕАТЕ</span><span class="sxs-lookup"><span data-stu-id="316a2-113">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="316a2-114">Если свойство не существует в текущем сообщении, оно должно быть создано.</span><span class="sxs-lookup"><span data-stu-id="316a2-114">If a property does not exist in the current message, it should be created.</span></span> <span data-ttu-id="316a2-115">Если свойство существует, текущие данные в свойстве должны быть заменены данными из потока данных из формата данных Transport-Neutral (TNEF).</span><span class="sxs-lookup"><span data-stu-id="316a2-115">If the property does exist, the current data in the property should be replaced with the data from the Transport-Neutral Encapsulation Format (TNEF) stream.</span></span> <span data-ttu-id="316a2-116">Когда реализация устанавливает флаг МАПИ_КРЕАТЕ, она также должна устанавливать флаг МАПИ_МОДИФИ.</span><span class="sxs-lookup"><span data-stu-id="316a2-116">When an implementation sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="316a2-117">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="316a2-117">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="316a2-118">ЗаПрашивает разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="316a2-118">Requests read/write permission.</span></span> <span data-ttu-id="316a2-119">Интерфейс по умолчанию доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="316a2-119">The default interface is read-only.</span></span> <span data-ttu-id="316a2-120">МАПИ_МОДИФИ должен быть задан всегда, когда задано значение МАПИ_КРЕАТЕ.</span><span class="sxs-lookup"><span data-stu-id="316a2-120">MAPI_MODIFY must be set whenever MAPI_CREATE is set.</span></span>
    
 <span data-ttu-id="316a2-121">_Лппстреам_</span><span class="sxs-lookup"><span data-stu-id="316a2-121">_lppStream_</span></span>
  
> <span data-ttu-id="316a2-122">вышли Указатель на указатель на объект Stream, который содержит текст из свойства **пр_боди** ([PidTagBody](pidtagbody-canonical-property.md)) переданного инкапсулированного сообщения и который поддерживает интерфейс [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="316a2-122">[out] A pointer to a pointer to a stream object that contains the text from the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of the passed-in encapsulated message and that supports the [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="316a2-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="316a2-123">Return value</span></span>

<span data-ttu-id="316a2-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="316a2-124">S_OK</span></span> 
  
> <span data-ttu-id="316a2-125">Вызов выполнен успешно и вернул ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="316a2-125">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="316a2-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="316a2-126">Remarks</span></span>

<span data-ttu-id="316a2-127">Поставщики транспорта, поставщики хранилищ сообщений и шлюзы вызывают метод **итнеф:: опентагжедбоди** для открытия интерфейса потока для текста инкапсулированного сообщения (то есть для объекта TNEF).</span><span class="sxs-lookup"><span data-stu-id="316a2-127">Transport providers, message store providers, and gateways call the **ITnef::OpenTaggedBody** method to open a stream interface on the text of an encapsulated message (that is, on a TNEF object).</span></span> 
  
<span data-ttu-id="316a2-128">В процессе обработки **опентагжедбоди** вставляет или анализирует Теги вложений, указывающие положение любых вложений или объектов OLE в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="316a2-128">As part of its processing, **OpenTaggedBody** either inserts or parses attachment tags that indicate the position of any attachments or OLE objects in the message text.</span></span> <span data-ttu-id="316a2-129">Теги вложений имеют следующий формат:</span><span class="sxs-lookup"><span data-stu-id="316a2-129">The attachment tags are in the following format:</span></span> 
  
 <span data-ttu-id="316a2-130">**[[** _имя вложения_ **:** _n_ **в** _имени контейнера вложения_ **]]**</span><span class="sxs-lookup"><span data-stu-id="316a2-130">**[[** _attachment name_ **:** _n_ **in** _attachment container name_ **]]**</span></span>
  
 <span data-ttu-id="316a2-131">_имя вложения_ описание объекта вложения;  _n_ — это число, которое определяет вложение, которое является частью последовательности и получает значение, которое передается в параметре _лпкэй_ функции [опентнефстреам](opentnefstream.md) или [опентнефстреамекс](opentnefstreamex.md) ; и _имя контейнера вложений_ описывает физический компонент, в котором находится объект вложения.</span><span class="sxs-lookup"><span data-stu-id="316a2-131">_attachment name_ describes the attachment object;  _n_ is a number that identifies the attachment that is part of a sequence, incrementing from the value passed in the  _lpKey_ parameter of the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function; and  _attachment container name_ describes the physical component where the attachment object resides.</span></span> 
  
 <span data-ttu-id="316a2-132">**Опентагжедбоди** считывает текст сообщения и вставляет тег вложения везде, где в тексте присутствует объект вложения.</span><span class="sxs-lookup"><span data-stu-id="316a2-132">**OpenTaggedBody** reads out message text and inserts an attachment tag wherever an attachment object originally appeared in the text.</span></span> <span data-ttu-id="316a2-133">Текст исходного сообщения не изменяется.</span><span class="sxs-lookup"><span data-stu-id="316a2-133">The original message text is not changed.</span></span> 
  
<span data-ttu-id="316a2-134">Когда сообщение с тегами передается в поток, теги удаляются, а объекты вложений перемещаются в позицию тегов в потоке.</span><span class="sxs-lookup"><span data-stu-id="316a2-134">When a message that has tags is passed to a stream, the tags are stripped out and the attachment objects are relocated in the position of the tags in the stream.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="316a2-135">См. также</span><span class="sxs-lookup"><span data-stu-id="316a2-135">See also</span></span>



[<span data-ttu-id="316a2-136">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="316a2-136">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="316a2-137">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="316a2-137">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="316a2-138">Каноническое свойство PidTagBody</span><span class="sxs-lookup"><span data-stu-id="316a2-138">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)
  
[<span data-ttu-id="316a2-139">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="316a2-139">ITnef : IUnknown</span></span>](itnefiunknown.md)

