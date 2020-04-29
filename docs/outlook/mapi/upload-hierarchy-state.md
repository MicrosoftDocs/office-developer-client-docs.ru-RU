---
title: Состояние отправки иерархии
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f789f4d7bbaf585d0d80f2208c35313542dfc191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415427"
---
# <a name="upload-hierarchy-state"></a><span data-ttu-id="97243-103">Состояние отправки иерархии</span><span class="sxs-lookup"><span data-stu-id="97243-103">Upload Hierarchy State</span></span>

  
  
<span data-ttu-id="97243-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97243-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="97243-105">В этом разделе описывается, что происходит во время состояния иерархии отправки конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="97243-105">This topic describes what happens during the upload hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="97243-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="97243-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="97243-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="97243-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="97243-108">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="97243-108">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="97243-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="97243-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="97243-110">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="97243-110">**[UPHIER](uphier.md)**</span></span> <br/> |
|<span data-ttu-id="97243-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="97243-111">From this state:</span></span>  <br/> |[<span data-ttu-id="97243-112">Состояние синхронизации</span><span class="sxs-lookup"><span data-stu-id="97243-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="97243-113">В это состояние:</span><span class="sxs-lookup"><span data-stu-id="97243-113">To this state:</span></span>  <br/> |<span data-ttu-id="97243-114">[Состояние отправки папки](upload-folder-state.md)или Синхронизация состояния</span><span class="sxs-lookup"><span data-stu-id="97243-114">[Upload folder state](upload-folder-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="97243-115">Конечный автомат репликации — это детерминированный конечный автомат.</span><span class="sxs-lookup"><span data-stu-id="97243-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="97243-116">Клиент, который отменяет одно состояние на другое, должен в конечном итоге вернуться к предыдущему из последнего.</span><span class="sxs-lookup"><span data-stu-id="97243-116">A client departing one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="97243-117">Описание</span><span class="sxs-lookup"><span data-stu-id="97243-117">Description</span></span>

<span data-ttu-id="97243-118">Это состояние инициирует отправку иерархии дерева папок, которая была указана в предыдущем состоянии синхронизации.</span><span class="sxs-lookup"><span data-stu-id="97243-118">This state initiates uploading a folder tree hierarchy that has been specified in a preceding synchronize state.</span></span> <span data-ttu-id="97243-119">Outlook определяет количество папок, созданных или измененных в этой иерархии, и инициализация *цента* в **уфиер**.</span><span class="sxs-lookup"><span data-stu-id="97243-119">Outlook determines the number of folders that have been created or modified in that hierarchy and initializes  *cEnt*  in **UPHIER**.</span></span> <span data-ttu-id="97243-120">В Outlook также хранится количество отправленных папок с помощью другого элемента *иент* .</span><span class="sxs-lookup"><span data-stu-id="97243-120">Outlook also keeps a count of the number of uploaded folders with another member  *iEnt*  .</span></span> <span data-ttu-id="97243-121">Чтобы отправить каждую из папок *цент* , клиент переместит локальное хранилище в состояние папки отправки, вернувшись к состоянию иерархии отправки после завершения загрузки папки.</span><span class="sxs-lookup"><span data-stu-id="97243-121">To upload each of the  *cEnt*  folders, the client moves the local store into the upload folder state, returning to the upload hierarchy state when the folder upload finishes.</span></span> 
  
<span data-ttu-id="97243-122">При завершении состояния иерархии отправки локальное хранилище возвращается в состояние Synchronize.</span><span class="sxs-lookup"><span data-stu-id="97243-122">When the upload hierarchy state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="97243-123">См. также</span><span class="sxs-lookup"><span data-stu-id="97243-123">See also</span></span>



[<span data-ttu-id="97243-124">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="97243-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="97243-125">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="97243-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="97243-126">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="97243-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="97243-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="97243-127">SYNCSTATE</span></span>](syncstate.md)

