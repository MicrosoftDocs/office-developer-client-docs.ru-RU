---
title: Состояние отправки данных иерархии
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3ed24682086556addf76b8451674a73bd82ce050
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572188"
---
# <a name="upload-hierarchy-state"></a><span data-ttu-id="0b572-103">Состояние отправки данных иерархии</span><span class="sxs-lookup"><span data-stu-id="0b572-103">Upload Hierarchy State</span></span>

  
  
<span data-ttu-id="0b572-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b572-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="0b572-105">В этом разделе описываются двоичных файлов состояние иерархии отправляемых конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="0b572-105">This topic describes what happens during the upload hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="0b572-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="0b572-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b572-107">Идентификатор состояний:</span><span class="sxs-lookup"><span data-stu-id="0b572-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="0b572-108">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="0b572-108">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="0b572-109">Структура связанных данных:</span><span class="sxs-lookup"><span data-stu-id="0b572-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="0b572-110">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="0b572-110">**[UPHIER](uphier.md)**</span></span> <br/> |
|<span data-ttu-id="0b572-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="0b572-111">From this state:</span></span>  <br/> |[<span data-ttu-id="0b572-112">Состояние синхронизации</span><span class="sxs-lookup"><span data-stu-id="0b572-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="0b572-113">Это состояние:</span><span class="sxs-lookup"><span data-stu-id="0b572-113">To this state:</span></span>  <br/> |<span data-ttu-id="0b572-114">[Отправить состояние папки](upload-folder-state.md), или синхронизировать состояние</span><span class="sxs-lookup"><span data-stu-id="0b572-114">[Upload folder state](upload-folder-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="0b572-115">Конечный автомат репликации является детерминированным конечного автомата.</span><span class="sxs-lookup"><span data-stu-id="0b572-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="0b572-116">Клиент чрезмерных изменений одного состояния в другое должны в конечном счете возврата на первый из последний.</span><span class="sxs-lookup"><span data-stu-id="0b572-116">A client departing one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="0b572-117">Описание</span><span class="sxs-lookup"><span data-stu-id="0b572-117">Description</span></span>

<span data-ttu-id="0b572-118">Это состояние означает инициирует отправку дерева иерархии папок, которые были заданы в предыдущих синхронизировать состояние.</span><span class="sxs-lookup"><span data-stu-id="0b572-118">This state initiates uploading a folder tree hierarchy that has been specified in a preceding synchronize state.</span></span> <span data-ttu-id="0b572-119">Outlook определяет число папок, которые были созданы или изменены в этой иерархии и инициализирует *централизованной* в **UPHIER**.</span><span class="sxs-lookup"><span data-stu-id="0b572-119">Outlook determines the number of folders that have been created or modified in that hierarchy and initializes  *cEnt*  in **UPHIER**.</span></span> <span data-ttu-id="0b572-120">Outlook также поддерживает счетчик количество загруженному папок с другого члена *iEnt* .</span><span class="sxs-lookup"><span data-stu-id="0b572-120">Outlook also keeps a count of the number of uploaded folders with another member  *iEnt*  .</span></span> <span data-ttu-id="0b572-121">Отправка каждой папки *централизованной* клиента перемещает локального хранилища в папку состояние передачи, возвращает состояние иерархии отправки после завершения загрузки папки.</span><span class="sxs-lookup"><span data-stu-id="0b572-121">To upload each of the  *cEnt*  folders, the client moves the local store into the upload folder state, returning to the upload hierarchy state when the folder upload finishes.</span></span> 
  
<span data-ttu-id="0b572-122">По окончании состояние иерархии отправляемых локального хранилища возвращается в состояние синхронизации.</span><span class="sxs-lookup"><span data-stu-id="0b572-122">When the upload hierarchy state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0b572-123">См. также</span><span class="sxs-lookup"><span data-stu-id="0b572-123">See also</span></span>



[<span data-ttu-id="0b572-124">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="0b572-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="0b572-125">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="0b572-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="0b572-126">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="0b572-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="0b572-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="0b572-127">SYNCSTATE</span></span>](syncstate.md)

