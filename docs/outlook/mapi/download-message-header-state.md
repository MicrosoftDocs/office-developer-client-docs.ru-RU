---
title: Состояние скачивания заголовка сообщения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7407b6606634ecc0151f582e4481ecbff5e7dc57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808328"
---
# <a name="download-message-header-state"></a><span data-ttu-id="61d43-103">Состояние скачивания заголовка сообщения</span><span class="sxs-lookup"><span data-stu-id="61d43-103">Download Message Header State</span></span>

  
  
<span data-ttu-id="61d43-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61d43-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="61d43-105">В этом разделе описываются двоичных файлов состояния заголовок сообщения загрузки конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="61d43-105">This topic describes what happens during the download message header state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="61d43-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="61d43-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61d43-107">Идентификатор состояний:</span><span class="sxs-lookup"><span data-stu-id="61d43-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="61d43-108">**LR_SYNC_DOWNLOAD_HEADER**</span><span class="sxs-lookup"><span data-stu-id="61d43-108">**LR_SYNC_DOWNLOAD_HEADER**</span></span> <br/> |
|<span data-ttu-id="61d43-109">Структура связанных данных:</span><span class="sxs-lookup"><span data-stu-id="61d43-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="61d43-110">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="61d43-110">**[HDRSYNC](hdrsync.md)**</span></span> <br/> |
|<span data-ttu-id="61d43-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="61d43-111">From this state:</span></span>  <br/> |[<span data-ttu-id="61d43-112">Состояние простоя</span><span class="sxs-lookup"><span data-stu-id="61d43-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="61d43-113">Это состояние:</span><span class="sxs-lookup"><span data-stu-id="61d43-113">To this state:</span></span>  <br/> |<span data-ttu-id="61d43-114">Состояние простоя</span><span class="sxs-lookup"><span data-stu-id="61d43-114">Idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="61d43-115">Конечный автомат репликации является детерминированным конечного автомата.</span><span class="sxs-lookup"><span data-stu-id="61d43-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="61d43-116">Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний.</span><span class="sxs-lookup"><span data-stu-id="61d43-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="61d43-117">Описание</span><span class="sxs-lookup"><span data-stu-id="61d43-117">Description</span></span>

<span data-ttu-id="61d43-118">В этом состоянии клиента обновляет заголовка сообщения для локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="61d43-118">During this state, the client updates the header of a message on a local store.</span></span> <span data-ttu-id="61d43-119">Локальное хранилище в этот режим на **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** и завершает работу при вызове **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** .</span><span class="sxs-lookup"><span data-stu-id="61d43-119">The local store enters this state upon **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** and exits when **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** is called.</span></span> <span data-ttu-id="61d43-120">В этом состоянии Outlook инициализирует элементы связанной структуры данных **HDRSYNC** со сведениями о заголовке сообщения.</span><span class="sxs-lookup"><span data-stu-id="61d43-120">During this state, Outlook initializes members of the associated **HDRSYNC** data structure with information about the header of a message.</span></span> <span data-ttu-id="61d43-121">Клиент сначала загружает элемент полного сообщения с сервера и обновляет заголовка сообщения локально.</span><span class="sxs-lookup"><span data-stu-id="61d43-121">The client first downloads the full message item from the server and then updates the header of the message item locally.</span></span> 
  
<span data-ttu-id="61d43-122">По окончании о синхронизации клиента задает файл для загрузки результатов.</span><span class="sxs-lookup"><span data-stu-id="61d43-122">When syncrhonization ends, the client sets the download results.</span></span> <span data-ttu-id="61d43-123">Локальное хранилище возвращается в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="61d43-123">The local store returns to the idle state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="61d43-124">См. также</span><span class="sxs-lookup"><span data-stu-id="61d43-124">See also</span></span>



[<span data-ttu-id="61d43-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="61d43-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="61d43-126">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="61d43-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="61d43-127">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="61d43-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="61d43-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="61d43-128">SYNCSTATE</span></span>](syncstate.md)

