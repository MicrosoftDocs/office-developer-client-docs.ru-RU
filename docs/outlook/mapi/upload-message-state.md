---
title: Состояние отправки сообщения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 430734fe98799c386e71612355b194a6b8edf00a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575415"
---
# <a name="upload-message-state"></a><span data-ttu-id="909b2-103">Состояние отправки сообщения</span><span class="sxs-lookup"><span data-stu-id="909b2-103">Upload Message State</span></span>

  
  
<span data-ttu-id="909b2-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="909b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="909b2-105">В этом разделе описываются двоичных файлов состояние отправляемых сообщений конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="909b2-105">This topic describes what happens during the upload message state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="909b2-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="909b2-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="909b2-107">Идентификатор состояний:</span><span class="sxs-lookup"><span data-stu-id="909b2-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="909b2-108">**LR_SYNC_UPLOAD_MESSAGE**</span><span class="sxs-lookup"><span data-stu-id="909b2-108">**LR_SYNC_UPLOAD_MESSAGE**</span></span> <br/> |
|<span data-ttu-id="909b2-109">Структура связанных данных:</span><span class="sxs-lookup"><span data-stu-id="909b2-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="909b2-110">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="909b2-110">**[UPMSG](upmsg.md)**</span></span> <br/> |
|<span data-ttu-id="909b2-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="909b2-111">From this state:</span></span>  <br/> |[<span data-ttu-id="909b2-112">Отправка состояний в таблице</span><span class="sxs-lookup"><span data-stu-id="909b2-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="909b2-113">Это состояние:</span><span class="sxs-lookup"><span data-stu-id="909b2-113">To this state:</span></span>  <br/> |<span data-ttu-id="909b2-114">Отправка состояний в таблице</span><span class="sxs-lookup"><span data-stu-id="909b2-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="909b2-115">Конечный автомат репликации является детерминированным конечного автомата.</span><span class="sxs-lookup"><span data-stu-id="909b2-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="909b2-116">Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний.</span><span class="sxs-lookup"><span data-stu-id="909b2-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="909b2-117">Описание</span><span class="sxs-lookup"><span data-stu-id="909b2-117">Description</span></span>

<span data-ttu-id="909b2-118">Это состояние означает инициирует отправка элемента Outlook (почту, календарь, контактов, задач, примечание или журнала), который является новым или перемещена в текущую папку или, были ли изменены.</span><span class="sxs-lookup"><span data-stu-id="909b2-118">This state initiates uploading an Outlook item (mail, calendar, contact, task, note, or journal) that is new or has been moved to the current folder, or that has been modified.</span></span> <span data-ttu-id="909b2-119">Outlook инициализирует структуры данных **UPMSG** correpsonding на соответствующие сведения для элемента добавлении, перемещен или изменены.</span><span class="sxs-lookup"><span data-stu-id="909b2-119">Outlook initializes the correpsonding **UPMSG** data structure with the appropriate information for the item as being added, moved, or modified.</span></span> 
  
<span data-ttu-id="909b2-120">Если добавлена или перемещения элемента клиент затем соответствующим образом добавляет или обновляет элемент на сервере.</span><span class="sxs-lookup"><span data-stu-id="909b2-120">If the item has been added or moved, the client then appropriately adds or updates the item on the server.</span></span> 
  
<span data-ttu-id="909b2-121">Если элемент был изменен, дальнейшей Outlook указывает в структуре данных **UPMSG** являются ли изменения в заголовок сообщения (в этом случае элемент — это заголовок сообщения), свойства элемента или самого элемента, которому требуется конфликта решение.</span><span class="sxs-lookup"><span data-stu-id="909b2-121">If the item has been modified, Outlook further specifies in the **UPMSG** data structure whether the modifications are in a message header (in which case the item is the message header), in the item properties, or in the item itself that requires conflict resolution.</span></span> <span data-ttu-id="909b2-122">Клиент затем обновляет элемент на сервере.</span><span class="sxs-lookup"><span data-stu-id="909b2-122">The client then updates the item on the server.</span></span> 
  
<span data-ttu-id="909b2-123">По завершении отправки элемента Outlook заметки о, что сообщение будет отправлен, таким образом, чтобы он не обрабатывается в последующих отправить.</span><span class="sxs-lookup"><span data-stu-id="909b2-123">When the item upload ends, Outlook notes that the message has been uploaded, so that it will not be processed in a subsequent upload.</span></span> <span data-ttu-id="909b2-124">Локальное хранилище возвращается в состояние таблицы отправить.</span><span class="sxs-lookup"><span data-stu-id="909b2-124">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="909b2-125">См. также</span><span class="sxs-lookup"><span data-stu-id="909b2-125">See also</span></span>



[<span data-ttu-id="909b2-126">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="909b2-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="909b2-127">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="909b2-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="909b2-128">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="909b2-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="909b2-129">СОСТОЯНИЕ</span><span class="sxs-lookup"><span data-stu-id="909b2-129">SYNCSTATE</span></span>](syncstate.md)

