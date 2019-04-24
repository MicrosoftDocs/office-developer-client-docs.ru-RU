---
title: Имаписинк IUnknown
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341281"
---
# <a name="imapisync--iunknown"></a><span data-ttu-id="3143d-103">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3143d-103">IMAPISync : IUnknown</span></span>

  
  
<span data-ttu-id="3143d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3143d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3143d-105">Предоставляет механизм для синхронизации электронной почты вместо использования API транспорта.</span><span class="sxs-lookup"><span data-stu-id="3143d-105">Provides a mechanism for synchronizing email instead of using the Transport API.</span></span> <span data-ttu-id="3143d-106">Этот интерфейс предоставляется в объекте Store.</span><span class="sxs-lookup"><span data-stu-id="3143d-106">This interface is exposed on a store object.</span></span> <span data-ttu-id="3143d-107">С помощью этого интерфейса и [имаписинкпрогресскаллбакк: IUnknown](imapisyncprogresscallbackiunknown.md)поставщик транспорта может предоставлять более удобные и появляющиеся сообщения об ошибках, чем те, которые отображаются в диалоговом окне отправки и получения в Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="3143d-107">By using this interface and [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), a transport provider can provide better progress and error messages than those that appear in the Send/Receive dialog in Microsoft Outlook.</span></span>
  
<span data-ttu-id="3143d-108">Папка "Исходящие" все еще находится в хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3143d-108">The outbox is still in the default store.</span></span> <span data-ttu-id="3143d-109">Outlook продолжит использовать трансПортный API для отправки почты, так как исходящее сообщение не может находиться во внешнем хранилище.</span><span class="sxs-lookup"><span data-stu-id="3143d-109">Outlook will continue to use the Transport APIs to send mail because the outgoing message cannot be in the external store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3143d-110">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="3143d-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="3143d-111">Поставщики услуг хранения и транспорта</span><span class="sxs-lookup"><span data-stu-id="3143d-111">Store and transport providers</span></span>  <br/> |
|<span data-ttu-id="3143d-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="3143d-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="3143d-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="3143d-113">Outlook</span></span>  <br/> |
|<span data-ttu-id="3143d-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="3143d-114">Called by:</span></span>  <br/> |<span data-ttu-id="3143d-115">Поставщики услуг хранения и транспорта</span><span class="sxs-lookup"><span data-stu-id="3143d-115">Store and Transport providers</span></span>  <br/> |
|<span data-ttu-id="3143d-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="3143d-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3143d-117">Иид_имаписинк</span><span class="sxs-lookup"><span data-stu-id="3143d-117">IID_IMAPISync</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3143d-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="3143d-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3143d-119">Синчронизеинбаккграунд</span><span class="sxs-lookup"><span data-stu-id="3143d-119">SynchronizeInBackground</span></span>](imapisyncsynchronizeinbackground.md) <br/> |<span data-ttu-id="3143d-120">Реализуется поставщиками хранилищ сообщений.</span><span class="sxs-lookup"><span data-stu-id="3143d-120">Implemented by message store providers.</span></span> <span data-ttu-id="3143d-121">Этот метод вызывается Outlook 2010 и Outlook 2013 для запуска синхронизации.</span><span class="sxs-lookup"><span data-stu-id="3143d-121">This method is called by Outlook 2010 and Outlook 2013 to start synchronization.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3143d-122">См. также</span><span class="sxs-lookup"><span data-stu-id="3143d-122">See also</span></span>



[<span data-ttu-id="3143d-123">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3143d-123">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)


[<span data-ttu-id="3143d-124">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="3143d-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

