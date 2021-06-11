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
ms.openlocfilehash: e66315042f8b5cd5aff0e4aa076588c9f312376a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406173"
---
# <a name="imapiviewadvisesinkonprint"></a><span data-ttu-id="8e29b-103">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="8e29b-103">IMAPIViewAdviseSink::OnPrint</span></span>

  
  
<span data-ttu-id="8e29b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e29b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e29b-105">Заветив зрителю формы состояние печати формы.</span><span class="sxs-lookup"><span data-stu-id="8e29b-105">Notifies the form viewer of the printing status of a form.</span></span>
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a><span data-ttu-id="8e29b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8e29b-106">Parameters</span></span>

 <span data-ttu-id="8e29b-107">_dwPageNumber_</span><span class="sxs-lookup"><span data-stu-id="8e29b-107">_dwPageNumber_</span></span>
  
> <span data-ttu-id="8e29b-108">[in] Номер последней напечатанной страницы.</span><span class="sxs-lookup"><span data-stu-id="8e29b-108">[in] Number of the last page printed.</span></span>
    
 <span data-ttu-id="8e29b-109">_hrStatus_</span><span class="sxs-lookup"><span data-stu-id="8e29b-109">_hrStatus_</span></span>
  
> <span data-ttu-id="8e29b-110">[in] Значение HRESULT, указывающее состояние задания печати.</span><span class="sxs-lookup"><span data-stu-id="8e29b-110">[in] An HRESULT value indicating the status of the print job.</span></span> <span data-ttu-id="8e29b-111">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="8e29b-111">Possible values are:</span></span>
    
<span data-ttu-id="8e29b-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="8e29b-112">S_FALSE</span></span> 
  
> <span data-ttu-id="8e29b-113">Задание печати успешно завершено.</span><span class="sxs-lookup"><span data-stu-id="8e29b-113">The printing job has finished successfully.</span></span>
    
<span data-ttu-id="8e29b-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e29b-114">S_OK</span></span> 
  
> <span data-ttu-id="8e29b-115">Задание печати находится в процессе выполнения.</span><span class="sxs-lookup"><span data-stu-id="8e29b-115">The printing job is in progress.</span></span>
    
<span data-ttu-id="8e29b-116">FAILED</span><span class="sxs-lookup"><span data-stu-id="8e29b-116">FAILED</span></span> 
  
> <span data-ttu-id="8e29b-117">Задание печати было прекращено из-за сбоя.</span><span class="sxs-lookup"><span data-stu-id="8e29b-117">The printing job was terminated due to a failure.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8e29b-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e29b-118">Return value</span></span>

<span data-ttu-id="8e29b-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e29b-119">S_OK</span></span> 
  
> <span data-ttu-id="8e29b-120">Уведомление успешно.</span><span class="sxs-lookup"><span data-stu-id="8e29b-120">The notification succeeded.</span></span>
    
<span data-ttu-id="8e29b-121">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="8e29b-121">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="8e29b-122">Пользователь отменил операцию, как правило, нажав кнопку Отмена в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="8e29b-122">The user canceled the operation, typically by clicking the Cancel button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8e29b-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="8e29b-123">Remarks</span></span>

<span data-ttu-id="8e29b-124">Объекты формы называют **метод IMAPIViewAdviseSink::OnPrint** во время печати, чтобы сообщить зрителю о ходе печати.</span><span class="sxs-lookup"><span data-stu-id="8e29b-124">Form objects call the **IMAPIViewAdviseSink::OnPrint** method while printing to inform the viewer of printing progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8e29b-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="8e29b-125">Notes to callers</span></span>

<span data-ttu-id="8e29b-126">Если задание печати включает несколько страниц, вы можете вызвать **OnPrint** после печати каждой страницы.</span><span class="sxs-lookup"><span data-stu-id="8e29b-126">If the printing job involves multiple pages, you can call **OnPrint** after each page is printed.</span></span> <span data-ttu-id="8e29b-127">Установите  _dwPageNumber_ на страницу, напечатаемую в настоящее время, и  _hrStatus_ S_OK.</span><span class="sxs-lookup"><span data-stu-id="8e29b-127">Set  _dwPageNumber_ to the page currently being printed and  _hrStatus_ to S_OK.</span></span> <span data-ttu-id="8e29b-128">По завершению задания печати вызывайте **OnPrint** с набором  _dwPageNumber_ на последнюю напечатанную страницу,  _а hrStatus_ — S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="8e29b-128">When the printing job is complete, call **OnPrint** with  _dwPageNumber_ set to the last page printed and  _hrStatus_ set to S_FALSE.</span></span> 
  
<span data-ttu-id="8e29b-129">Дополнительные сведения об уведомлениях формы см. в рублях [Отправка и получение уведомлений о форме.](sending-and-receiving-form-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="8e29b-129">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8e29b-130">См. также</span><span class="sxs-lookup"><span data-stu-id="8e29b-130">See also</span></span>



[<span data-ttu-id="8e29b-131">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e29b-131">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

