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
ms.openlocfilehash: 8e2e7a3f9279485d862fac5bb6413b3d3eb1343e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589086"
---
# <a name="imapisync--iunknown"></a><span data-ttu-id="1a6c0-103">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a6c0-103">IMAPISync : IUnknown</span></span>

  
  
<span data-ttu-id="1a6c0-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a6c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a6c0-105">Механизм синхронизации электронной почты, а не с помощью API транспорта.</span><span class="sxs-lookup"><span data-stu-id="1a6c0-105">Provides a mechanism for synchronizing email instead of using the Transport API.</span></span> <span data-ttu-id="1a6c0-106">Этот интерфейс предоставляется на объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="1a6c0-106">This interface is exposed on a store object.</span></span> <span data-ttu-id="1a6c0-107">С помощью этого интерфейса и [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md), поставщика транспорта можно обеспечить более хода выполнения и сообщения об ошибках чем, который отображается в диалоговом окне отправки и получения в Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="1a6c0-107">By using this interface and [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), a transport provider can provide better progress and error messages than those that appear in the Send/Receive dialog in Microsoft Outlook.</span></span>
  
<span data-ttu-id="1a6c0-108">Исходящие — это по-прежнему в хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1a6c0-108">The outbox is still in the default store.</span></span> <span data-ttu-id="1a6c0-109">Outlook будет использовать интерфейсов API транспорта для отправки почты, так как исходящее сообщение не может быть внешнего хранилища.</span><span class="sxs-lookup"><span data-stu-id="1a6c0-109">Outlook will continue to use the Transport APIs to send mail because the outgoing message cannot be in the external store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a6c0-110">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="1a6c0-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="1a6c0-111">Поставщики хранилища и транспорта</span><span class="sxs-lookup"><span data-stu-id="1a6c0-111">Store and transport providers</span></span>  <br/> |
|<span data-ttu-id="1a6c0-112">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="1a6c0-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="1a6c0-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="1a6c0-113">Outlook</span></span>  <br/> |
|<span data-ttu-id="1a6c0-114">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="1a6c0-114">Called by:</span></span>  <br/> |<span data-ttu-id="1a6c0-115">Поставщики хранилища и транспорта</span><span class="sxs-lookup"><span data-stu-id="1a6c0-115">Store and Transport providers</span></span>  <br/> |
|<span data-ttu-id="1a6c0-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="1a6c0-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1a6c0-117">IID_IMAPISync</span><span class="sxs-lookup"><span data-stu-id="1a6c0-117">IID_IMAPISync</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1a6c0-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="1a6c0-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1a6c0-119">SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="1a6c0-119">SynchronizeInBackground</span></span>](imapisyncsynchronizeinbackground.md) <br/> |<span data-ttu-id="1a6c0-120">Реализации поставщиками хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="1a6c0-120">Implemented by message store providers.</span></span> <span data-ttu-id="1a6c0-121">Этот метод вызывается с Outlook 2010 и Outlook 2013, чтобы запустить синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="1a6c0-121">This method is called by Outlook 2010 and Outlook 2013 to start synchronization.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a6c0-122">См. также</span><span class="sxs-lookup"><span data-stu-id="1a6c0-122">See also</span></span>



[<span data-ttu-id="1a6c0-123">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a6c0-123">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)


[<span data-ttu-id="1a6c0-124">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="1a6c0-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

