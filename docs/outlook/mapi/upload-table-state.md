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
# <a name="upload-table-state"></a><span data-ttu-id="c8726-103">Состояние отправки таблицы</span><span class="sxs-lookup"><span data-stu-id="c8726-103">Upload Table State</span></span>

  
  
<span data-ttu-id="c8726-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8726-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="c8726-105">В этом разделе описывается, что происходит во время состояния отправки таблицы конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="c8726-105">This topic describes what happens during the upload table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="c8726-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="c8726-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8726-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="c8726-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="c8726-108">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="c8726-108">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="c8726-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="c8726-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="c8726-110">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="c8726-110">**[UPTBL](uptbl.md)**</span></span> <br/> |
|<span data-ttu-id="c8726-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="c8726-111">From this state:</span></span>  <br/> |[<span data-ttu-id="c8726-112">Синхронизация состояния содержимого</span><span class="sxs-lookup"><span data-stu-id="c8726-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="c8726-113">В этом состоянии:</span><span class="sxs-lookup"><span data-stu-id="c8726-113">To this state:</span></span>  <br/> |<span data-ttu-id="c8726-114">[Отправка состояния сообщения,](upload-message-state.md) [отправка состояния удаления,](upload-delete-status-state.md)отправка состояния [чтения](upload-read-status-state.md)или синхронизация состояния содержимого</span><span class="sxs-lookup"><span data-stu-id="c8726-114">[Upload message state](upload-message-state.md), [upload delete status state](upload-delete-status-state.md), [upload read status state](upload-read-status-state.md), or synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="c8726-115">Этот автомат репликации является детерминируемым.</span><span class="sxs-lookup"><span data-stu-id="c8726-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="c8726-116">Клиент, выступая из одного состояния в другое, должен в конечном итоге вернуться к одному из последних.</span><span class="sxs-lookup"><span data-stu-id="c8726-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="c8726-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c8726-117">Description</span></span>

<span data-ttu-id="c8726-118">Это состояние инициирует отправку содержимого папки, указанной в предыдущем состоянии синхронизации содержимого.</span><span class="sxs-lookup"><span data-stu-id="c8726-118">This state initiates uploading the contents of a folder that has been specified in a preceding synchronize contents state.</span></span> <span data-ttu-id="c8726-119">Папка может быть почтой, календарем, контактами, задачами, заметками или папкой журнала.</span><span class="sxs-lookup"><span data-stu-id="c8726-119">The folder can be a mail, calendar, contacts, tasks, notes, or journal folder.</span></span> <span data-ttu-id="c8726-120">В этом состоянии Outlook создает список элементов, которые были добавлены, изменены, перемещены, удалены или помечены как прочитанный, и подготавливает соответствующие внутренние сведения для соответствующего состояния отправки сообщения, отправки состояния удаления или отправки состояния чтения.</span><span class="sxs-lookup"><span data-stu-id="c8726-120">During this state, Outlook creates a list of items that have been added, modified, moved, deleted, or marked as read, and prepares the appropriate internal information for the corresponding upload message state, upload delete status state, or upload read status state.</span></span>
  
<span data-ttu-id="c8726-121">Когда это состояние закончится, Outlook пометит папку как синхронизированную с ее содержимым, чтобы содержимое не было загружено повторно, пока не будет выполнено другое изменение.</span><span class="sxs-lookup"><span data-stu-id="c8726-121">When this state ends, Outlook marks the folder as having its contents synchronized, so that the contents will not be uploaded again until another modification is made.</span></span> <span data-ttu-id="c8726-122">Локальное хранилище возвращается в состояние синхронизации содержимого.</span><span class="sxs-lookup"><span data-stu-id="c8726-122">The local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c8726-123">См. также</span><span class="sxs-lookup"><span data-stu-id="c8726-123">See also</span></span>



[<span data-ttu-id="c8726-124">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="c8726-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="c8726-125">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="c8726-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="c8726-126">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="c8726-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="c8726-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="c8726-127">SYNCSTATE</span></span>](syncstate.md)

