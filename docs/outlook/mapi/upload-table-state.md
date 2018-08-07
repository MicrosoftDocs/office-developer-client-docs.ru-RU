---
title: Состояние отправки данных таблицы
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 454df4dde2062d20855e4d9bceaf4400669693ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812562"
---
# <a name="upload-table-state"></a><span data-ttu-id="e8d0b-103">Состояние отправки данных таблицы</span><span class="sxs-lookup"><span data-stu-id="e8d0b-103">Upload Table State</span></span>

  
  
<span data-ttu-id="e8d0b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e8d0b-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="e8d0b-105">В этом разделе описываются двоичных файлов состояния в таблице отправляемых конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="e8d0b-105">This topic describes what happens during the upload table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e8d0b-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="e8d0b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8d0b-107">Идентификатор состояний:</span><span class="sxs-lookup"><span data-stu-id="e8d0b-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="e8d0b-108">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="e8d0b-108">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="e8d0b-109">Структура связанных данных:</span><span class="sxs-lookup"><span data-stu-id="e8d0b-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="e8d0b-110">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="e8d0b-110">**[UPTBL](uptbl.md)**</span></span> <br/> |
|<span data-ttu-id="e8d0b-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="e8d0b-111">From this state:</span></span>  <br/> |[<span data-ttu-id="e8d0b-112">Синхронизировать состояние содержимого</span><span class="sxs-lookup"><span data-stu-id="e8d0b-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="e8d0b-113">Это состояние:</span><span class="sxs-lookup"><span data-stu-id="e8d0b-113">To this state:</span></span>  <br/> |<span data-ttu-id="e8d0b-114">[Отправка сообщения состояния](upload-message-state.md), [отправляемых удалить состояние состояние](upload-delete-status-state.md), [Отправить состояние состояние read](upload-read-status-state.md)или синхронизировать состояние содержимого</span><span class="sxs-lookup"><span data-stu-id="e8d0b-114">[Upload message state](upload-message-state.md), [upload delete status state](upload-delete-status-state.md), [upload read status state](upload-read-status-state.md), or synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="e8d0b-115">Конечный автомат репликации является детерминированным конечного автомата.</span><span class="sxs-lookup"><span data-stu-id="e8d0b-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="e8d0b-116">Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний.</span><span class="sxs-lookup"><span data-stu-id="e8d0b-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="e8d0b-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e8d0b-117">Description</span></span>

<span data-ttu-id="e8d0b-118">Это состояние означает инициирует отправку пользователями содержимого папки, которые были заданы в предыдущем состоянии содержимое синхронизировать.</span><span class="sxs-lookup"><span data-stu-id="e8d0b-118">This state initiates uploading the contents of a folder that has been specified in a preceding synchronize contents state.</span></span> <span data-ttu-id="e8d0b-119">Папка может быть папка почту, календарь, контакты, задачи, заметки или журнала.</span><span class="sxs-lookup"><span data-stu-id="e8d0b-119">The folder can be a mail, calendar, contacts, tasks, notes, or journal folder.</span></span> <span data-ttu-id="e8d0b-120">Во время это состояние означает Outlook создает список элементов, которые были добавлены, изменены, перемещен, удален или помечена как чтения и подготавливает соответствующие внутренние сведения для соответствующего состояния отправить сообщения, передача удалить состояние состояние или отправить состояние чтения состояние.</span><span class="sxs-lookup"><span data-stu-id="e8d0b-120">During this state, Outlook creates a list of items that have been added, modified, moved, deleted, or marked as read, and prepares the appropriate internal information for the corresponding upload message state, upload delete status state, or upload read status state.</span></span>
  
<span data-ttu-id="e8d0b-121">По окончании этого состояния Outlook помечает папки как имеющий синхронизирована, вместе с контентом, чтобы содержимое не будут загружаться еще раз до другого изменения.</span><span class="sxs-lookup"><span data-stu-id="e8d0b-121">When this state ends, Outlook marks the folder as having its contents synchronized, so that the contents will not be uploaded again until another modification is made.</span></span> <span data-ttu-id="e8d0b-122">Локальное хранилище возвращается в состояние содержимое синхронизировать.</span><span class="sxs-lookup"><span data-stu-id="e8d0b-122">The local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e8d0b-123">См. также</span><span class="sxs-lookup"><span data-stu-id="e8d0b-123">See also</span></span>



[<span data-ttu-id="e8d0b-124">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="e8d0b-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e8d0b-125">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="e8d0b-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="e8d0b-126">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="e8d0b-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="e8d0b-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="e8d0b-127">SYNCSTATE</span></span>](syncstate.md)

