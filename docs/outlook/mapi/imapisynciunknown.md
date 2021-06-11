---
title: IMAPISync IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync
api_type:
- COM
ms.assetid: c14d1012-f3d4-47eb-8a90-3160331f94e8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4d46152136f3806c79f0dd454ed9fd41fc845721
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405594"
---
# <a name="imapisync--iunknown"></a><span data-ttu-id="45250-103">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="45250-103">IMAPISync : IUnknown</span></span>

  
  
<span data-ttu-id="45250-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45250-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45250-105">Предоставляет механизм синхронизации электронной почты вместо использования API транспорта.</span><span class="sxs-lookup"><span data-stu-id="45250-105">Provides a mechanism for synchronizing email instead of using the Transport API.</span></span> <span data-ttu-id="45250-106">Этот интерфейс выставлен на объекте магазина.</span><span class="sxs-lookup"><span data-stu-id="45250-106">This interface is exposed on a store object.</span></span> <span data-ttu-id="45250-107">С помощью этого интерфейса [и IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)поставщик транспорта может обеспечить лучший прогресс и сообщения об ошибках, чем сообщения, которые отображаются в диалоговом окне Отправка/Получение в Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="45250-107">By using this interface and [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), a transport provider can provide better progress and error messages than those that appear in the Send/Receive dialog in Microsoft Outlook.</span></span>
  
<span data-ttu-id="45250-108">Почтовый ящик по-прежнему находится в хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="45250-108">The outbox is still in the default store.</span></span> <span data-ttu-id="45250-109">Outlook будет продолжать использовать API транспорта для отправки почты, так как исходя из сообщения не может быть во внешнем хранилище.</span><span class="sxs-lookup"><span data-stu-id="45250-109">Outlook will continue to use the Transport APIs to send mail because the outgoing message cannot be in the external store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45250-110">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="45250-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="45250-111">Поставщики хранения и транспорта</span><span class="sxs-lookup"><span data-stu-id="45250-111">Store and transport providers</span></span>  <br/> |
|<span data-ttu-id="45250-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="45250-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="45250-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="45250-113">Outlook</span></span>  <br/> |
|<span data-ttu-id="45250-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="45250-114">Called by:</span></span>  <br/> |<span data-ttu-id="45250-115">Поставщики магазинов и транспорта</span><span class="sxs-lookup"><span data-stu-id="45250-115">Store and Transport providers</span></span>  <br/> |
|<span data-ttu-id="45250-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="45250-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="45250-117">IID_IMAPISync</span><span class="sxs-lookup"><span data-stu-id="45250-117">IID_IMAPISync</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="45250-118">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="45250-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="45250-119">СинхронизацияInBackground</span><span class="sxs-lookup"><span data-stu-id="45250-119">SynchronizeInBackground</span></span>](imapisyncsynchronizeinbackground.md) <br/> |<span data-ttu-id="45250-120">Реализовано поставщиками магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="45250-120">Implemented by message store providers.</span></span> <span data-ttu-id="45250-121">Этот метод называется Outlook 2010 и Outlook 2013 для начала синхронизации.</span><span class="sxs-lookup"><span data-stu-id="45250-121">This method is called by Outlook 2010 and Outlook 2013 to start synchronization.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="45250-122">См. также</span><span class="sxs-lookup"><span data-stu-id="45250-122">See also</span></span>



[<span data-ttu-id="45250-123">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="45250-123">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)


[<span data-ttu-id="45250-124">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="45250-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

