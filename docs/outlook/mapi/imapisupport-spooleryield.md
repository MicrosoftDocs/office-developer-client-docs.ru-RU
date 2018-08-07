---
title: IMAPISupportSpoolerYield
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerYield
api_type:
- COM
ms.assetid: f5c6ba8f-4ef5-4d60-b4e6-5b9160ec4e99
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6e917991e109ac04a14ea7d93eebcf9cce835845
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809171"
---
# <a name="imapisupportspooleryield"></a><span data-ttu-id="11da0-103">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="11da0-103">IMAPISupport::SpoolerYield</span></span>

  
  
<span data-ttu-id="11da0-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="11da0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="11da0-105">Передает управление процессора диспетчер очереди MAPI, чтобы он может выполнять любые задачи рассматриваются необходимые.</span><span class="sxs-lookup"><span data-stu-id="11da0-105">Gives control of the CPU to the MAPI spooler so that it can perform any tasks it considers necessary.</span></span>
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="11da0-106">���������</span><span class="sxs-lookup"><span data-stu-id="11da0-106">Parameters</span></span>

 <span data-ttu-id="11da0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="11da0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="11da0-108">Зарезервировано; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="11da0-108">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="11da0-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="11da0-109">Return value</span></span>

<span data-ttu-id="11da0-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="11da0-110">S_OK</span></span> 
  
> <span data-ttu-id="11da0-111">Поставщика транспорта успешно выпущен ЦП.</span><span class="sxs-lookup"><span data-stu-id="11da0-111">The transport provider successfully released the CPU.</span></span>
    
<span data-ttu-id="11da0-112">MAPI_W_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="11da0-112">MAPI_W_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="11da0-113">Указывает, что поставщик транспорта для остановки доставки сообщения получателям, которые еще не получена.</span><span class="sxs-lookup"><span data-stu-id="11da0-113">Instructs the transport provider to stop the delivery of the message to any recipients that have not yet received it.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="11da0-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="11da0-114">Remarks</span></span>

<span data-ttu-id="11da0-115">Метод **IMAPISupport::SpoolerYield** реализуется для объектов поддержки поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="11da0-115">The **IMAPISupport::SpoolerYield** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="11da0-116">Поставщики транспорта вызовите **SpoolerYield** , чтобы разрешить диспетчер очереди MAPI для выполнения все необходимые действия.</span><span class="sxs-lookup"><span data-stu-id="11da0-116">Transport providers call **SpoolerYield** to allow the MAPI spooler to accomplish any necessary processing.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="11da0-117">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="11da0-117">Notes to callers</span></span>

<span data-ttu-id="11da0-118">Вызов **SpoolerYield** при выполнении длительных операций, которые могут быть приостановлено.</span><span class="sxs-lookup"><span data-stu-id="11da0-118">Call **SpoolerYield** when you are performing lengthy operations that can be paused.</span></span> <span data-ttu-id="11da0-119">Это позволяет приложениям переднего плана для запуска во время длительной операции, такие как доставки для большого количества получателей в сети «занят».</span><span class="sxs-lookup"><span data-stu-id="11da0-119">This allows foreground applications to run during a long operation, such as delivery to a large recipient list across a busy network.</span></span> 
  
<span data-ttu-id="11da0-120">Если **SpoolerYield** возвращает с MAPI_W_CANCEL_MESSAGE, диспетчер очереди MAPI определяет, что сообщение больше не было отправлено.</span><span class="sxs-lookup"><span data-stu-id="11da0-120">If **SpoolerYield** returns with MAPI_W_CANCEL_MESSAGE, the MAPI spooler has determined that the message should no longer be sent.</span></span> <span data-ttu-id="11da0-121">Снова MAPI_E_USER_CANCEL вызывающего процесса и exit, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="11da0-121">Return MAPI_E_USER_CANCEL to your calling process and exit, if possible.</span></span> 
  
<span data-ttu-id="11da0-122">Дополнительные сведения о выдаче диспетчер очереди MAPI см [Диспетчер очереди MAPI](interacting-with-the-mapi-spooler.md).</span><span class="sxs-lookup"><span data-stu-id="11da0-122">For more information about yielding to the MAPI spooler, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="11da0-123">См. также</span><span class="sxs-lookup"><span data-stu-id="11da0-123">See also</span></span>



[<span data-ttu-id="11da0-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="11da0-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

