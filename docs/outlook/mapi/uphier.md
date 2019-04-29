---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 45ef7ce9291376ac020035f0bde6172caf6cc01b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414923"
---
# <a name="uphier"></a><span data-ttu-id="cba6c-103">UPHIER</span><span class="sxs-lookup"><span data-stu-id="cba6c-103">UPHIER</span></span>
 
<span data-ttu-id="cba6c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cba6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cba6c-105">Сведения для синхронизации иерархии папок во время [состояния иерархии отправки](upload-hierarchy-state.md).</span><span class="sxs-lookup"><span data-stu-id="cba6c-105">Information for synchronizing a folder hierarchy during the [upload hierarchy state](upload-hierarchy-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cba6c-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="cba6c-106">Quick info</span></span>

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="cba6c-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="cba6c-107">Members</span></span>

<span data-ttu-id="cba6c-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cba6c-108">_ulFlags_</span></span>
  
> <span data-ttu-id="cba6c-109">возврата Флаги для изменения поведения при синхронизации иерархии папок.</span><span class="sxs-lookup"><span data-stu-id="cba6c-109">[in] Flags to modify the behavior when synchronizing the folder hierarchy.</span></span>
    
  - <span data-ttu-id="cba6c-110">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="cba6c-110">UPH_OK</span></span>
    
    - <span data-ttu-id="cba6c-111">возврата Отправка выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="cba6c-111">[in] Upload was successful.</span></span> <span data-ttu-id="cba6c-112">Клиент устанавливает это после успешной отправки информации на сервер.</span><span class="sxs-lookup"><span data-stu-id="cba6c-112">The client sets this after successfully uploading information to the server.</span></span> <span data-ttu-id="cba6c-113">При просмотре этого флага в Outlook удаляются все внутренние сведения о регистрации, в которых указана иерархия папок, которую необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="cba6c-113">Upon seeing this flag, Outlook clears any internal bookkeeping information that indicated the folder hierarchy needed updating.</span></span> 
    
    - <span data-ttu-id="cba6c-114">Клиент передает значение HRESULT в случае неудачной отправки.</span><span class="sxs-lookup"><span data-stu-id="cba6c-114">The client passes the HRESULT if the upload was not successful.</span></span>
    
<span data-ttu-id="cba6c-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="cba6c-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="cba6c-116">вышли Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cba6c-116">[out] This member is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="cba6c-117">_Иент_</span><span class="sxs-lookup"><span data-stu-id="cba6c-117">_iEnt_</span></span>
  
> <span data-ttu-id="cba6c-118">вышли Индекс, отслеживающий синхронизацию числа папок, заданных \*\* с помощью цента.</span><span class="sxs-lookup"><span data-stu-id="cba6c-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span></span> 
    
<span data-ttu-id="cba6c-119">_Центов_</span><span class="sxs-lookup"><span data-stu-id="cba6c-119">_cEnt_</span></span>
  
> <span data-ttu-id="cba6c-120">вышли Количество папок, которые не синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="cba6c-120">[out] Number of folders that are out of sync.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cba6c-121">См. также</span><span class="sxs-lookup"><span data-stu-id="cba6c-121">See also</span></span>

- [<span data-ttu-id="cba6c-122">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="cba6c-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="cba6c-123">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="cba6c-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="cba6c-124">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="cba6c-124">MAPI Constants</span></span>](mapi-constants.md)

