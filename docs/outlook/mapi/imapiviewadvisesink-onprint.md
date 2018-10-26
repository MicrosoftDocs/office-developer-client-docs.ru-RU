---
title: IMAPIViewAdviseSinkOnPrint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnPrint
api_type:
- COM
ms.assetid: d16219a0-268c-428d-9f02-4f06eb5b6d7d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 202d461d4acefe18e69b47db9319cb328c61406e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592320"
---
# <a name="imapiviewadvisesinkonprint"></a><span data-ttu-id="2eb90-103">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="2eb90-103">IMAPIViewAdviseSink::OnPrint</span></span>

  
  
<span data-ttu-id="2eb90-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2eb90-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2eb90-105">Уведомляет средство просмотра формы из состояния печати формы.</span><span class="sxs-lookup"><span data-stu-id="2eb90-105">Notifies the form viewer of the printing status of a form.</span></span>
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a><span data-ttu-id="2eb90-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2eb90-106">Parameters</span></span>

 <span data-ttu-id="2eb90-107">_dwPageNumber_</span><span class="sxs-lookup"><span data-stu-id="2eb90-107">_dwPageNumber_</span></span>
  
> <span data-ttu-id="2eb90-108">[in] Номер последней страницы при выводе на печать.</span><span class="sxs-lookup"><span data-stu-id="2eb90-108">[in] Number of the last page printed.</span></span>
    
 <span data-ttu-id="2eb90-109">_hrStatus_</span><span class="sxs-lookup"><span data-stu-id="2eb90-109">_hrStatus_</span></span>
  
> <span data-ttu-id="2eb90-110">[in] Значение HRESULT, указывающее состояние задания печати.</span><span class="sxs-lookup"><span data-stu-id="2eb90-110">[in] An HRESULT value indicating the status of the print job.</span></span> <span data-ttu-id="2eb90-111">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="2eb90-111">Possible values are:</span></span>
    
<span data-ttu-id="2eb90-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="2eb90-112">S_FALSE</span></span> 
  
> <span data-ttu-id="2eb90-113">Задание печати успешно завершено.</span><span class="sxs-lookup"><span data-stu-id="2eb90-113">The printing job has finished successfully.</span></span>
    
<span data-ttu-id="2eb90-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="2eb90-114">S_OK</span></span> 
  
> <span data-ttu-id="2eb90-115">Задание печати находится в стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="2eb90-115">The printing job is in progress.</span></span>
    
<span data-ttu-id="2eb90-116">НЕ УДАЛОСЬ</span><span class="sxs-lookup"><span data-stu-id="2eb90-116">FAILED</span></span> 
  
> <span data-ttu-id="2eb90-117">Задание печати был завершен из-за сбоя.</span><span class="sxs-lookup"><span data-stu-id="2eb90-117">The printing job was terminated due to a failure.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2eb90-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2eb90-118">Return value</span></span>

<span data-ttu-id="2eb90-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="2eb90-119">S_OK</span></span> 
  
> <span data-ttu-id="2eb90-120">Уведомление успешно завершен.</span><span class="sxs-lookup"><span data-stu-id="2eb90-120">The notification succeeded.</span></span>
    
<span data-ttu-id="2eb90-121">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="2eb90-121">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="2eb90-122">Пользователь отменил операцию, как правило, нажав кнопку "Отмена" в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="2eb90-122">The user canceled the operation, typically by clicking the Cancel button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2eb90-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="2eb90-123">Remarks</span></span>

<span data-ttu-id="2eb90-124">Объекты формы вызовите метод **IMAPIViewAdviseSink::OnPrint** при печати для оповещения просмотра ход печати.</span><span class="sxs-lookup"><span data-stu-id="2eb90-124">Form objects call the **IMAPIViewAdviseSink::OnPrint** method while printing to inform the viewer of printing progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2eb90-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="2eb90-125">Notes to callers</span></span>

<span data-ttu-id="2eb90-126">Если задание печати состоит из нескольких страниц, можно позвонить **OnPrint** после печати каждой страницы.</span><span class="sxs-lookup"><span data-stu-id="2eb90-126">If the printing job involves multiple pages, you can call **OnPrint** after each page is printed.</span></span> <span data-ttu-id="2eb90-127">Значение S_OK _dwPageNumber_ на страницу в настоящее время печатается и _hrStatus_ .</span><span class="sxs-lookup"><span data-stu-id="2eb90-127">Set  _dwPageNumber_ to the page currently being printed and  _hrStatus_ to S_OK.</span></span> <span data-ttu-id="2eb90-128">По завершении задания печати звонок, **OnPrint** с _dwPageNumber_ к последнему задать страницы при выводе на печать и _hrStatus_ значение S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="2eb90-128">When the printing job is complete, call **OnPrint** with  _dwPageNumber_ set to the last page printed and  _hrStatus_ set to S_FALSE.</span></span> 
  
<span data-ttu-id="2eb90-129">Дополнительные сведения о уведомлений формы можно [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="2eb90-129">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2eb90-130">См. также</span><span class="sxs-lookup"><span data-stu-id="2eb90-130">See also</span></span>



[<span data-ttu-id="2eb90-131">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2eb90-131">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

