---
title: Состояние отправки таблицы
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
# <a name="upload-table-state"></a><span data-ttu-id="0c9ae-103">Состояние отправки таблицы</span><span class="sxs-lookup"><span data-stu-id="0c9ae-103">Upload Table State</span></span>

  
  
<span data-ttu-id="0c9ae-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c9ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="0c9ae-105">В этом разделе описывается, что происходит во время состояния таблицы отправки для конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="0c9ae-105">This topic describes what happens during the upload table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="0c9ae-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="0c9ae-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c9ae-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="0c9ae-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="0c9ae-108">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="0c9ae-108">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="0c9ae-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="0c9ae-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="0c9ae-110">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="0c9ae-110">**[UPTBL](uptbl.md)**</span></span> <br/> |
|<span data-ttu-id="0c9ae-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="0c9ae-111">From this state:</span></span>  <br/> |[<span data-ttu-id="0c9ae-112">Состояние синхронизации контента</span><span class="sxs-lookup"><span data-stu-id="0c9ae-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="0c9ae-113">В это состояние:</span><span class="sxs-lookup"><span data-stu-id="0c9ae-113">To this state:</span></span>  <br/> |<span data-ttu-id="0c9ae-114">[Состояние отправки сообщения](upload-message-state.md), состояние [отправки удаления](upload-delete-status-state.md), состояние [отправки состояния чтения](upload-read-status-state.md)или состояние синхронизации контента</span><span class="sxs-lookup"><span data-stu-id="0c9ae-114">[Upload message state](upload-message-state.md), [upload delete status state](upload-delete-status-state.md), [upload read status state](upload-read-status-state.md), or synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="0c9ae-115">Конечный автомат репликации — это детерминированный конечный автомат.</span><span class="sxs-lookup"><span data-stu-id="0c9ae-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="0c9ae-116">Клиент, который отменяет от одного состояния к другому, должен, в конечном итоге, вернуться к предыдущему из последнего.</span><span class="sxs-lookup"><span data-stu-id="0c9ae-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="0c9ae-117">Описание</span><span class="sxs-lookup"><span data-stu-id="0c9ae-117">Description</span></span>

<span data-ttu-id="0c9ae-118">Это состояние инициирует отправку содержимого папки, которая была указана в предыдущем состоянии синхронизации контента.</span><span class="sxs-lookup"><span data-stu-id="0c9ae-118">This state initiates uploading the contents of a folder that has been specified in a preceding synchronize contents state.</span></span> <span data-ttu-id="0c9ae-119">Папка может представлять собой почту, календарь, контакты, задачи, заметки или папку дневника.</span><span class="sxs-lookup"><span data-stu-id="0c9ae-119">The folder can be a mail, calendar, contacts, tasks, notes, or journal folder.</span></span> <span data-ttu-id="0c9ae-120">В этом состоянии Outlook создает список элементов, добавленных, измененных, перемещенных, удаленных или помеченных как прочитанные, и подготавливает соответствующие внутренние сведения для соответствующего состояния сообщения о передаче, состояния отправки или состояния загрузки.</span><span class="sxs-lookup"><span data-stu-id="0c9ae-120">During this state, Outlook creates a list of items that have been added, modified, moved, deleted, or marked as read, and prepares the appropriate internal information for the corresponding upload message state, upload delete status state, or upload read status state.</span></span>
  
<span data-ttu-id="0c9ae-121">При завершении этого состояния Outlook помечает папку как ее содержимое синхронизированной, поэтому содержимое не будет отправлено повторно, пока не будет внесено другое изменение.</span><span class="sxs-lookup"><span data-stu-id="0c9ae-121">When this state ends, Outlook marks the folder as having its contents synchronized, so that the contents will not be uploaded again until another modification is made.</span></span> <span data-ttu-id="0c9ae-122">Локальное хранилище возвращается в состояние синхронизировать содержимое.</span><span class="sxs-lookup"><span data-stu-id="0c9ae-122">The local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0c9ae-123">См. также</span><span class="sxs-lookup"><span data-stu-id="0c9ae-123">See also</span></span>



[<span data-ttu-id="0c9ae-124">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="0c9ae-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="0c9ae-125">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="0c9ae-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="0c9ae-126">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="0c9ae-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="0c9ae-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="0c9ae-127">SYNCSTATE</span></span>](syncstate.md)

