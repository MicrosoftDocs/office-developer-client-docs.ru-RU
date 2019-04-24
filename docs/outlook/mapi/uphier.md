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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359425"
---
# <a name="uphier"></a><span data-ttu-id="1dc64-103">UPHIER</span><span class="sxs-lookup"><span data-stu-id="1dc64-103">UPHIER</span></span>
 
<span data-ttu-id="1dc64-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1dc64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1dc64-105">Сведения для синхронизации иерархии папок во время [состояния иерархии отправки](upload-hierarchy-state.md).</span><span class="sxs-lookup"><span data-stu-id="1dc64-105">Information for synchronizing a folder hierarchy during the [upload hierarchy state](upload-hierarchy-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1dc64-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="1dc64-106">Quick info</span></span>

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="1dc64-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="1dc64-107">Members</span></span>

<span data-ttu-id="1dc64-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1dc64-108">_ulFlags_</span></span>
  
> <span data-ttu-id="1dc64-109">возврата Флаги для изменения поведения при синхронизации иерархии папок.</span><span class="sxs-lookup"><span data-stu-id="1dc64-109">[in] Flags to modify the behavior when synchronizing the folder hierarchy.</span></span>
    
  - <span data-ttu-id="1dc64-110">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="1dc64-110">UPH_OK</span></span>
    
    - <span data-ttu-id="1dc64-111">возврата Отправка выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1dc64-111">[in] Upload was successful.</span></span> <span data-ttu-id="1dc64-112">Клиент устанавливает это после успешной отправки информации на сервер.</span><span class="sxs-lookup"><span data-stu-id="1dc64-112">The client sets this after successfully uploading information to the server.</span></span> <span data-ttu-id="1dc64-113">При просмотре этого флага в Outlook удаляются все внутренние сведения о регистрации, в которых указана иерархия папок, которую необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="1dc64-113">Upon seeing this flag, Outlook clears any internal bookkeeping information that indicated the folder hierarchy needed updating.</span></span> 
    
    - <span data-ttu-id="1dc64-114">Клиент передает значение HRESULT в случае неудачной отправки.</span><span class="sxs-lookup"><span data-stu-id="1dc64-114">The client passes the HRESULT if the upload was not successful.</span></span>
    
<span data-ttu-id="1dc64-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="1dc64-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="1dc64-116">вышли Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1dc64-116">[out] This member is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="1dc64-117">_Иент_</span><span class="sxs-lookup"><span data-stu-id="1dc64-117">_iEnt_</span></span>
  
> <span data-ttu-id="1dc64-118">вышли Индекс, отслеживающий синхронизацию числа папок, заданных \*\* с помощью цента.</span><span class="sxs-lookup"><span data-stu-id="1dc64-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span></span> 
    
<span data-ttu-id="1dc64-119">_Центов_</span><span class="sxs-lookup"><span data-stu-id="1dc64-119">_cEnt_</span></span>
  
> <span data-ttu-id="1dc64-120">вышли Количество папок, которые не синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="1dc64-120">[out] Number of folders that are out of sync.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1dc64-121">См. также</span><span class="sxs-lookup"><span data-stu-id="1dc64-121">See also</span></span>

- [<span data-ttu-id="1dc64-122">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="1dc64-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="1dc64-123">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="1dc64-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="1dc64-124">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="1dc64-124">MAPI Constants</span></span>](mapi-constants.md)

