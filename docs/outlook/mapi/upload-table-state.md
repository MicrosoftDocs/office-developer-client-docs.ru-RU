---
title: Upload Состояние таблицы
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a2a9b3f214c76b8ec965c84c4731e0dc57e83352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405823"
---
# <a name="upload-table-state"></a><span data-ttu-id="18fd1-103">Upload Состояние таблицы</span><span class="sxs-lookup"><span data-stu-id="18fd1-103">Upload Table State</span></span>

  
  
<span data-ttu-id="18fd1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18fd1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="18fd1-105">В этом разделе описывается, что происходит во время состояния таблицы загрузки машины состояния репликации.</span><span class="sxs-lookup"><span data-stu-id="18fd1-105">This topic describes what happens during the upload table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="18fd1-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="18fd1-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18fd1-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="18fd1-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="18fd1-108">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="18fd1-108">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="18fd1-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="18fd1-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="18fd1-110">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="18fd1-110">**[UPTBL](uptbl.md)**</span></span> <br/> |
|<span data-ttu-id="18fd1-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="18fd1-111">From this state:</span></span>  <br/> |[<span data-ttu-id="18fd1-112">Синхронизация состояния содержимого</span><span class="sxs-lookup"><span data-stu-id="18fd1-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="18fd1-113">Для этого состояния:</span><span class="sxs-lookup"><span data-stu-id="18fd1-113">To this state:</span></span>  <br/> |<span data-ttu-id="18fd1-114">[Upload, загрузите](upload-message-state.md) [состояние](upload-delete-status-state.md) [удаления,](upload-read-status-state.md)загрузите состояние состояния чтения или синхронизуйте состояние содержимого</span><span class="sxs-lookup"><span data-stu-id="18fd1-114">[Upload message state](upload-message-state.md), [upload delete status state](upload-delete-status-state.md), [upload read status state](upload-read-status-state.md), or synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="18fd1-115">Машина состояния репликации — это детерминистический автомат состояния.</span><span class="sxs-lookup"><span data-stu-id="18fd1-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="18fd1-116">Клиент, отправляющийся из одного состояния в другое, должен в конечном итоге вернуться в первое из последнего.</span><span class="sxs-lookup"><span data-stu-id="18fd1-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="18fd1-117">Описание</span><span class="sxs-lookup"><span data-stu-id="18fd1-117">Description</span></span>

<span data-ttu-id="18fd1-118">Это состояние инициирует отправку содержимого папки, указанной в предыдущем состоянии синхронизации содержимого.</span><span class="sxs-lookup"><span data-stu-id="18fd1-118">This state initiates uploading the contents of a folder that has been specified in a preceding synchronize contents state.</span></span> <span data-ttu-id="18fd1-119">Папка может быть почтой, календарем, контактами, задачами, заметками или папкой журнала.</span><span class="sxs-lookup"><span data-stu-id="18fd1-119">The folder can be a mail, calendar, contacts, tasks, notes, or journal folder.</span></span> <span data-ttu-id="18fd1-120">В этом состоянии Outlook список элементов, которые были добавлены, изменены, перемещены, удалены или помечены как прочитанный, и подготавливает соответствующие внутренние сведения для соответствующего состояния сообщения отправки, загрузки состояния удаления или загрузки состояния состояния чтения.</span><span class="sxs-lookup"><span data-stu-id="18fd1-120">During this state, Outlook creates a list of items that have been added, modified, moved, deleted, or marked as read, and prepares the appropriate internal information for the corresponding upload message state, upload delete status state, or upload read status state.</span></span>
  
<span data-ttu-id="18fd1-121">Когда это состояние закончится, Outlook пометит папку как синхронизированную с ее содержимым, чтобы содержимое не было загружено снова до тех пор, пока не будет сделано другое изменение.</span><span class="sxs-lookup"><span data-stu-id="18fd1-121">When this state ends, Outlook marks the folder as having its contents synchronized, so that the contents will not be uploaded again until another modification is made.</span></span> <span data-ttu-id="18fd1-122">Локальный магазин возвращается в состояние синхронизации содержимого.</span><span class="sxs-lookup"><span data-stu-id="18fd1-122">The local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="18fd1-123">См. также</span><span class="sxs-lookup"><span data-stu-id="18fd1-123">See also</span></span>



[<span data-ttu-id="18fd1-124">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="18fd1-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="18fd1-125">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="18fd1-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="18fd1-126">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="18fd1-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="18fd1-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="18fd1-127">SYNCSTATE</span></span>](syncstate.md)

