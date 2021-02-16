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
# <a name="imapisync--iunknown"></a><span data-ttu-id="4c660-103">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c660-103">IMAPISync : IUnknown</span></span>

  
  
<span data-ttu-id="4c660-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c660-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c660-105">Предоставляет механизм синхронизации электронной почты вместо использования API транспорта.</span><span class="sxs-lookup"><span data-stu-id="4c660-105">Provides a mechanism for synchronizing email instead of using the Transport API.</span></span> <span data-ttu-id="4c660-106">Этот интерфейс выставит на объекте store.</span><span class="sxs-lookup"><span data-stu-id="4c660-106">This interface is exposed on a store object.</span></span> <span data-ttu-id="4c660-107">С помощью этого интерфейса и [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)поставщик транспорта может обеспечить лучший ход выполнения и сообщения об ошибках, чем сообщения об ошибках, которые отображаются в диалоговом окне отправки и получения в Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="4c660-107">By using this interface and [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), a transport provider can provide better progress and error messages than those that appear in the Send/Receive dialog in Microsoft Outlook.</span></span>
  
<span data-ttu-id="4c660-108">Почтовый ящик по-прежнему находится в хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4c660-108">The outbox is still in the default store.</span></span> <span data-ttu-id="4c660-109">Outlook продолжит использовать API транспорта для отправки почты, так как исходя из этого сообщения не может быть во внешнем хранилище.</span><span class="sxs-lookup"><span data-stu-id="4c660-109">Outlook will continue to use the Transport APIs to send mail because the outgoing message cannot be in the external store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4c660-110">Выставим:</span><span class="sxs-lookup"><span data-stu-id="4c660-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="4c660-111">Поставщики услуг хранения и транспорта</span><span class="sxs-lookup"><span data-stu-id="4c660-111">Store and transport providers</span></span>  <br/> |
|<span data-ttu-id="4c660-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="4c660-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="4c660-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="4c660-113">Outlook</span></span>  <br/> |
|<span data-ttu-id="4c660-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="4c660-114">Called by:</span></span>  <br/> |<span data-ttu-id="4c660-115">Поставщики услуг хранения и транспорта</span><span class="sxs-lookup"><span data-stu-id="4c660-115">Store and Transport providers</span></span>  <br/> |
|<span data-ttu-id="4c660-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="4c660-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4c660-117">IID_IMAPISync</span><span class="sxs-lookup"><span data-stu-id="4c660-117">IID_IMAPISync</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4c660-118">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="4c660-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4c660-119">SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="4c660-119">SynchronizeInBackground</span></span>](imapisyncsynchronizeinbackground.md) <br/> |<span data-ttu-id="4c660-120">Реализовано поставщиками store сообщений.</span><span class="sxs-lookup"><span data-stu-id="4c660-120">Implemented by message store providers.</span></span> <span data-ttu-id="4c660-121">Этот метод вызван Outlook 2010 и Outlook 2013 для запуска синхронизации.</span><span class="sxs-lookup"><span data-stu-id="4c660-121">This method is called by Outlook 2010 and Outlook 2013 to start synchronization.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4c660-122">См. также</span><span class="sxs-lookup"><span data-stu-id="4c660-122">See also</span></span>



[<span data-ttu-id="4c660-123">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c660-123">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)


[<span data-ttu-id="4c660-124">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="4c660-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

