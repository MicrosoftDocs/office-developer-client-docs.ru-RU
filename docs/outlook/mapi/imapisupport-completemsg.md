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
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: db28d9684f1bb679ce36f99346f4ecc67a1a93e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19809106"
---
# <a name="imapisupportcompletemsg"></a><span data-ttu-id="c5fa0-103">IMAPISupport::CompleteMsg</span><span class="sxs-lookup"><span data-stu-id="c5fa0-103">IMAPISupport::CompleteMsg</span></span>

  
  
<span data-ttu-id="c5fa0-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c5fa0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c5fa0-105">Выполняет постобработку сообщение.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-105">Performs postprocessing on a message.</span></span> 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="c5fa0-106">���������</span><span class="sxs-lookup"><span data-stu-id="c5fa0-106">Parameters</span></span>

 <span data-ttu-id="c5fa0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c5fa0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c5fa0-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c5fa0-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c5fa0-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="c5fa0-110">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="c5fa0-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c5fa0-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c5fa0-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="c5fa0-112">[in] Указатель на идентификатор записи сообщения для обработки.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-112">[in] A pointer to the entry identifier of the message to process.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c5fa0-113">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="c5fa0-113">Return value</span></span>

<span data-ttu-id="c5fa0-114">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="c5fa0-114">S_OK</span></span> 
  
> <span data-ttu-id="c5fa0-115">Постобработку прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-115">The postprocessing was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c5fa0-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="c5fa0-116">Remarks</span></span>

<span data-ttu-id="c5fa0-117">Метод **IMAPISupport::CompleteMsg** реализуется для объектов поддержки поставщика хранилища сообщений и вызывается только у поставщиков хранилища сообщений, которые тесно связаны с поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-117">The **IMAPISupport::CompleteMsg** method is implemented for message store provider support objects and is called only by message store providers that are tightly coupled with transport providers.</span></span> <span data-ttu-id="c5fa0-118">Поставщики тесно связанных хранилища вызовите **IMAPISupport::CompleteMsg** , чтобы указать диспетчер очереди MAPI для postprocess сообщение.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-118">Tightly coupled store providers call **IMAPISupport::CompleteMsg** to instruct the MAPI spooler to postprocess a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c5fa0-119">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c5fa0-119">Notes to callers</span></span>

<span data-ttu-id="c5fa0-120">Вызовите **CompleteMsg** только в том случае, если вы тесно связан с поставщиком транспорта, может обрабатывать всех получателей сообщений и одного из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="c5fa0-120">Call **CompleteMsg** only when you are tightly coupled with a transport provider, you can handle all of the message's recipients, and one of the following conditions exists:</span></span> 
  
- <span data-ttu-id="c5fa0-121">Сообщение было предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-121">The message was preprocessed.</span></span>
    
- <span data-ttu-id="c5fa0-122">Сообщение необходимо постобработку диспетчером очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-122">The message requires postprocessing by the MAPI spooler.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5fa0-123">См. также</span><span class="sxs-lookup"><span data-stu-id="c5fa0-123">See also</span></span>



[<span data-ttu-id="c5fa0-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c5fa0-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

