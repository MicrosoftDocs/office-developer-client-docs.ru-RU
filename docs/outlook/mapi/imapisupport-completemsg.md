---
title: Имаписуппорткомплетемсг
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
# <a name="imapisupportcompletemsg"></a><span data-ttu-id="77c75-103">IMAPISupport::CompleteMsg</span><span class="sxs-lookup"><span data-stu-id="77c75-103">IMAPISupport::CompleteMsg</span></span>

  
  
<span data-ttu-id="77c75-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77c75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77c75-105">Выполняет обработку сообщения.</span><span class="sxs-lookup"><span data-stu-id="77c75-105">Performs postprocessing on a message.</span></span> 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="77c75-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="77c75-106">Parameters</span></span>

 <span data-ttu-id="77c75-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="77c75-107">_ulFlags_</span></span>
  
> <span data-ttu-id="77c75-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="77c75-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="77c75-109">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="77c75-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="77c75-110">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="77c75-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="77c75-111">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="77c75-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="77c75-112">возврата Указатель на идентификатор записи для обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="77c75-112">[in] A pointer to the entry identifier of the message to process.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="77c75-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77c75-113">Return value</span></span>

<span data-ttu-id="77c75-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="77c75-114">S_OK</span></span> 
  
> <span data-ttu-id="77c75-115">Пошаговая обработка выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="77c75-115">The postprocessing was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="77c75-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="77c75-116">Remarks</span></span>

<span data-ttu-id="77c75-117">Метод **имаписуппорт:: комплетемсг** реализован для объектов поддержки поставщика хранилища сообщений и вызывается только поставщиками хранилищ сообщений, тесно связанными с поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="77c75-117">The **IMAPISupport::CompleteMsg** method is implemented for message store provider support objects and is called only by message store providers that are tightly coupled with transport providers.</span></span> <span data-ttu-id="77c75-118">Тесно связанные поставщики магазинов вызывают **имаписуппорт:: комплетемсг** , чтобы указать, что диспетчер очереди MAPI должен обработать сообщение.</span><span class="sxs-lookup"><span data-stu-id="77c75-118">Tightly coupled store providers call **IMAPISupport::CompleteMsg** to instruct the MAPI spooler to postprocess a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="77c75-119">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="77c75-119">Notes to callers</span></span>

<span data-ttu-id="77c75-120">Call **комплетемсг** только в том случае, если у вас тесно связаны с поставщиком транспорта, вы можете обрабатывать всех получателей сообщения и одно из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="77c75-120">Call **CompleteMsg** only when you are tightly coupled with a transport provider, you can handle all of the message's recipients, and one of the following conditions exists:</span></span> 
  
- <span data-ttu-id="77c75-121">Сообщение было предварительно обработано.</span><span class="sxs-lookup"><span data-stu-id="77c75-121">The message was preprocessed.</span></span>
    
- <span data-ttu-id="77c75-122">Для сообщения требуется обработка с помощью диспетчера очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="77c75-122">The message requires postprocessing by the MAPI spooler.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="77c75-123">См. также</span><span class="sxs-lookup"><span data-stu-id="77c75-123">See also</span></span>



[<span data-ttu-id="77c75-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="77c75-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

