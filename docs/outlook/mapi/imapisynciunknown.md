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
ms.openlocfilehash: fb7a8ea39d6e7b1d7df1560658ceb67a79d39d92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809184"
---
# <a name="imapisync--iunknown"></a><span data-ttu-id="3f07d-103">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f07d-103">IMAPISync : IUnknown</span></span>

  
  
<span data-ttu-id="3f07d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3f07d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3f07d-105">Механизм синхронизации электронной почты, а не с помощью API транспорта.</span><span class="sxs-lookup"><span data-stu-id="3f07d-105">Provides a mechanism for synchronizing email instead of using the Transport API.</span></span> <span data-ttu-id="3f07d-106">Этот интерфейс предоставляется на объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="3f07d-106">This interface is exposed on a store object.</span></span> <span data-ttu-id="3f07d-107">С помощью этого интерфейса и [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md), поставщика транспорта можно обеспечить более хода выполнения и сообщения об ошибках чем, который отображается в диалоговом окне отправки и получения в Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="3f07d-107">By using this interface and [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), a transport provider can provide better progress and error messages than those that appear in the Send/Receive dialog in Microsoft Outlook.</span></span>
  
<span data-ttu-id="3f07d-108">Исходящие — это по-прежнему в хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3f07d-108">The outbox is still in the default store.</span></span> <span data-ttu-id="3f07d-109">Outlook будет использовать интерфейсов API транспорта для отправки почты, так как исходящее сообщение не может быть внешнего хранилища.</span><span class="sxs-lookup"><span data-stu-id="3f07d-109">Outlook will continue to use the Transport APIs to send mail because the outgoing message cannot be in the external store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3f07d-110">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="3f07d-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="3f07d-111">Поставщики хранилища и транспорта</span><span class="sxs-lookup"><span data-stu-id="3f07d-111">Store and transport providers</span></span>  <br/> |
|<span data-ttu-id="3f07d-112">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="3f07d-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="3f07d-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="3f07d-113">Outlook</span></span>  <br/> |
|<span data-ttu-id="3f07d-114">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="3f07d-114">Called by:</span></span>  <br/> |<span data-ttu-id="3f07d-115">Поставщики хранилища и транспорта</span><span class="sxs-lookup"><span data-stu-id="3f07d-115">Store and Transport providers</span></span>  <br/> |
|<span data-ttu-id="3f07d-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="3f07d-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3f07d-117">IID_IMAPISync</span><span class="sxs-lookup"><span data-stu-id="3f07d-117">IID_IMAPISync</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3f07d-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="3f07d-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3f07d-119">SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="3f07d-119">SynchronizeInBackground</span></span>](imapisyncsynchronizeinbackground.md) <br/> |<span data-ttu-id="3f07d-120">Реализации поставщиками хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="3f07d-120">Implemented by message store providers.</span></span> <span data-ttu-id="3f07d-121">Этот метод вызывается с Outlook 2010 и Outlook 2013, чтобы запустить синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="3f07d-121">This method is called by Outlook 2010 and Outlook 2013 to start synchronization.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f07d-122">См. также</span><span class="sxs-lookup"><span data-stu-id="3f07d-122">See also</span></span>



[<span data-ttu-id="3f07d-123">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f07d-123">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)


[<span data-ttu-id="3f07d-124">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="3f07d-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

