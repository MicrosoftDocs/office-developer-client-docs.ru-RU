---
title: ИмаписуппортстатусреЦипс
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StatusRecips
api_type:
- COM
ms.assetid: 9c34538e-5ba4-47c8-8002-85afa9d6c067
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 39d8786bf558ade4599d69e0a764f87fe60d99f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408770"
---
# <a name="imapisupportstatusrecips"></a><span data-ttu-id="2dbd5-103">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="2dbd5-103">IMAPISupport::StatusRecips</span></span>

  
  
<span data-ttu-id="2dbd5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2dbd5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2dbd5-105">Создание отчетов о доставке и недоставке.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-105">Generates delivery and nondelivery reports.</span></span>
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="2dbd5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2dbd5-106">Parameters</span></span>

 <span data-ttu-id="2dbd5-107">_Лпмессаже_</span><span class="sxs-lookup"><span data-stu-id="2dbd5-107">_lpMessage_</span></span>
  
> <span data-ttu-id="2dbd5-108">возврата Указатель на сообщение, для которого должен быть создан отчет.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-108">[in] A pointer to the message for which the report should be generated.</span></span>
    
 <span data-ttu-id="2dbd5-109">_ЛпреЦиплист_</span><span class="sxs-lookup"><span data-stu-id="2dbd5-109">_lpRecipList_</span></span>
  
> <span data-ttu-id="2dbd5-110">возврата Указатель на структуру [ADRLIST](adrlist.md) , которая описывает получателей сообщения, на которое указывает _лпмессаже_.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-110">[in] A pointer to an [ADRLIST](adrlist.md) structure that describes the recipients of the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2dbd5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2dbd5-111">Return value</span></span>

<span data-ttu-id="2dbd5-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="2dbd5-112">S_OK</span></span> 
  
> <span data-ttu-id="2dbd5-113">Отчет успешно создан.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-113">The report was successfully generated.</span></span>
    
<span data-ttu-id="2dbd5-114">МАПИ_В_ЕРРОРС_РЕТУРНЕД</span><span class="sxs-lookup"><span data-stu-id="2dbd5-114">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="2dbd5-115">Вызов выполнен в целом, но для этого типа получателя не заданы параметры получателя.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-115">The call succeeded overall, but there are no recipient options for this type of recipient.</span></span> <span data-ttu-id="2dbd5-116">При возвращении этого предупреждения вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="2dbd5-117">Чтобы проверить это предупреждение, используйте макрос **хр_фаилед** .</span><span class="sxs-lookup"><span data-stu-id="2dbd5-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="2dbd5-118">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="2dbd5-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2dbd5-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="2dbd5-119">Remarks</span></span>

<span data-ttu-id="2dbd5-120">Метод **имаписуппорт:: статусреЦипс** реализован для объектов поддержки поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-120">The **IMAPISupport::StatusRecips** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="2dbd5-121">Поставщики транспорта вызывают **статусреЦипс** , чтобы запросить отправку отчета о доставке или недоставке в набор из одного или нескольких получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-121">Transport providers call **StatusRecips** to request that MAPI send a delivery or nondelivery report to a set of one or more of the recipients of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2dbd5-122">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="2dbd5-122">Notes to callers</span></span>

<span data-ttu-id="2dbd5-123">Вы можете вызвать **статусреЦипс** несколько раз во время обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-123">You can call **StatusRecips** multiple times during the processing of a message.</span></span> <span data-ttu-id="2dbd5-124">Однако при вызове **статусреЦипс** для открытого сообщения рекомендуется собрать все сведения о доставке и недоставке для получателей сообщения и вызвать **статусреЦипс** для этого списка получателей.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-124">However, if you call **StatusRecips** for an open message, do your best to collect all delivery and nondelivery information for the message recipients and call **StatusRecips** for that recipient list.</span></span> <span data-ttu-id="2dbd5-125">Единственная точка семейства важна, так как несколько вызовов **статусреЦипс** для одного получателя могут привести к отправке нескольких одинаковых отчетов.</span><span class="sxs-lookup"><span data-stu-id="2dbd5-125">A single point of collection is important, because multiple **StatusRecips** calls for one recipient can result in multiple identical reports being sent.</span></span> 
  
<span data-ttu-id="2dbd5-126">Хранение свойств, которые относятся к доставке или доставке сообщений, в структуре **ADRLIST** , указанной параметром _лпреЦиплист_ .</span><span class="sxs-lookup"><span data-stu-id="2dbd5-126">Store properties that relate to message delivery or nondelivery in the **ADRLIST** structure indicated by the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="2dbd5-127">Полный список обязательных и необязательных свойств для отчетов о доставке и отчетов о недоставке см. в разделе [обязательные свойства сообщений отчета](required-report-message-properties.md) и неОбязательные [Свойства сообщения отчета](optional-report-message-properties.md).</span><span class="sxs-lookup"><span data-stu-id="2dbd5-127">For a complete list of required and optional properties for delivery reports and nondelivery reports, see [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties](optional-report-message-properties.md).</span></span> 
  
<span data-ttu-id="2dbd5-128">Выделение памяти для структуры **ADRLIST** в _лпреЦиплист_ с помощью функций [мапиаллокатебуффер](mapiallocatebuffer.md) и [мапиаллокатеморе](mapiallocatemore.md) .</span><span class="sxs-lookup"><span data-stu-id="2dbd5-128">Allocate memory for the **ADRLIST** structure in  _lpRecipList_ by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions.</span></span> <span data-ttu-id="2dbd5-129">MAPI освобождает память, вызывая функцию [мапифрибуффер](mapifreebuffer.md) только в случае успешного выполнения **статусреЦипс** .</span><span class="sxs-lookup"><span data-stu-id="2dbd5-129">MAPI releases the memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **StatusRecips** succeeds.</span></span> 
  
<span data-ttu-id="2dbd5-130">Обзор отчетов о доставке и недоставке можно найти в разделе [сообщения отчетов MAPI](mapi-report-messages.md).</span><span class="sxs-lookup"><span data-stu-id="2dbd5-130">For an overview of delivery and nondelivery reports, see [MAPI Report Messages](mapi-report-messages.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2dbd5-131">См. также</span><span class="sxs-lookup"><span data-stu-id="2dbd5-131">See also</span></span>



[<span data-ttu-id="2dbd5-132">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="2dbd5-132">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="2dbd5-133">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="2dbd5-133">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="2dbd5-134">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="2dbd5-134">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="2dbd5-135">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="2dbd5-135">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="2dbd5-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="2dbd5-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="2dbd5-137">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="2dbd5-137">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="2dbd5-138">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2dbd5-138">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2dbd5-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2dbd5-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

