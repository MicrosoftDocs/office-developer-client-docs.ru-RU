---
title: IMAPISupportCompleteMsg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompleteMsg
api_type:
- COM
ms.assetid: e7932433-abe0-4341-95e0-91b37c848145
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e8c52d71ee47966be09c6c0806eceafae0c5ff5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411192"
---
# <a name="imapisupportcompletemsg"></a><span data-ttu-id="d6fd4-103">IMAPISupport::CompleteMsg</span><span class="sxs-lookup"><span data-stu-id="d6fd4-103">IMAPISupport::CompleteMsg</span></span>

  
  
<span data-ttu-id="d6fd4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6fd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6fd4-105">Выполняет постпроцессинг в сообщении.</span><span class="sxs-lookup"><span data-stu-id="d6fd4-105">Performs postprocessing on a message.</span></span> 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="d6fd4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d6fd4-106">Parameters</span></span>

 <span data-ttu-id="d6fd4-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d6fd4-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d6fd4-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="d6fd4-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d6fd4-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d6fd4-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="d6fd4-110">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="d6fd4-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d6fd4-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d6fd4-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="d6fd4-112">[in] Указатель на идентификатор записи для обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="d6fd4-112">[in] A pointer to the entry identifier of the message to process.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d6fd4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6fd4-113">Return value</span></span>

<span data-ttu-id="d6fd4-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6fd4-114">S_OK</span></span> 
  
> <span data-ttu-id="d6fd4-115">Послепроцессинг был успешным.</span><span class="sxs-lookup"><span data-stu-id="d6fd4-115">The postprocessing was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d6fd4-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="d6fd4-116">Remarks</span></span>

<span data-ttu-id="d6fd4-117">Метод **IMAPISupport::CompleteMsg** реализуется для объектов поддержки поставщика хранения сообщений и вызван только поставщиками магазинов сообщений, тесно соедиными с поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="d6fd4-117">The **IMAPISupport::CompleteMsg** method is implemented for message store provider support objects and is called only by message store providers that are tightly coupled with transport providers.</span></span> <span data-ttu-id="d6fd4-118">Поставщики магазинов с тесной парой звонят **iMAPISupport::CompleteMsg,** чтобы поручить шпалеру MAPI отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="d6fd4-118">Tightly coupled store providers call **IMAPISupport::CompleteMsg** to instruct the MAPI spooler to postprocess a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d6fd4-119">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d6fd4-119">Notes to callers</span></span>

<span data-ttu-id="d6fd4-120">Вызов **CompleteMsg** только при тесной связи с поставщиком транспорта можно обрабатывать все получатели сообщения, и существует одно из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="d6fd4-120">Call **CompleteMsg** only when you are tightly coupled with a transport provider, you can handle all of the message's recipients, and one of the following conditions exists:</span></span> 
  
- <span data-ttu-id="d6fd4-121">Сообщение было предварительно процесировали.</span><span class="sxs-lookup"><span data-stu-id="d6fd4-121">The message was preprocessed.</span></span>
    
- <span data-ttu-id="d6fd4-122">Сообщение требует постпроцессинга шпалером MAPI.</span><span class="sxs-lookup"><span data-stu-id="d6fd4-122">The message requires postprocessing by the MAPI spooler.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6fd4-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d6fd4-123">See also</span></span>



[<span data-ttu-id="d6fd4-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6fd4-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

