---
title: Иолкаккаунтманажеринит
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Инициализирует Диспетчер учетных записей для использования.
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322038"
---
# <a name="iolkaccountmanagerinit"></a><span data-ttu-id="dda32-103">IOlkAccountManager::Init</span><span class="sxs-lookup"><span data-stu-id="dda32-103">IOlkAccountManager::Init</span></span>

<span data-ttu-id="dda32-104">Инициализирует Диспетчер учетных записей для использования.</span><span class="sxs-lookup"><span data-stu-id="dda32-104">Initializes the account manager for use.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dda32-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="dda32-105">Quick info</span></span>

<span data-ttu-id="dda32-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="dda32-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="dda32-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="dda32-107">Parameters</span></span>

<span data-ttu-id="dda32-108">_Паккселпер_</span><span class="sxs-lookup"><span data-stu-id="dda32-108">_pAcctHelper_</span></span>
  
> <span data-ttu-id="dda32-109">возврата Интерфейс [иолкаккаунселпер](iolkaccounthelper.md) , который предоставляет вспомогательные функции учетной записи.</span><span class="sxs-lookup"><span data-stu-id="dda32-109">[in] An [IOlkAccountHelper](iolkaccounthelper.md) interface that provides account helper functionality.</span></span> 
    
<span data-ttu-id="dda32-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="dda32-110">_dwFlags_</span></span>
  
> <span data-ttu-id="dda32-111">[in] Flags to modify behavior.</span><span class="sxs-lookup"><span data-stu-id="dda32-111">[in] Flags to modify behavior.</span></span>
    
   - <span data-ttu-id="dda32-112">**Аккт_инит_но_сторес_чекк** — предотвращает синхронизацию учетной записи (например, учетной записи IMAP) с соответствующим хранилищем.</span><span class="sxs-lookup"><span data-stu-id="dda32-112">**ACCT_INIT_NO_STORES_CHECK** —Prevents an account (such as an IMAP account) from synchronizing with an associated store.</span></span> 
    
   - <span data-ttu-id="dda32-113">**Аккт_инит_носинч_мапи_акктс** — предотвращает синхронизацию служб MAPI с учетными записями.</span><span class="sxs-lookup"><span data-stu-id="dda32-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** —Prevents MAPI services from synchronizing with accounts.</span></span> 
   
   - <span data-ttu-id="dda32-114">**Аккт_инит_но_нотификатионс** — запрещает диспетчеру учетных записей перехватывать широковещательные сообщения, предназначенные для других приложений.</span><span class="sxs-lookup"><span data-stu-id="dda32-114">**ACCT_INIT_NO_NOTIFICATIONS** —Prevents the Account Manager from intercepting broadcast messages intended for other applications.</span></span> 
   
   - <span data-ttu-id="dda32-115">**Олк_аккаунт_но_флагс** — СИНХРОНИЗИРУЕТ службы MAPI с учетными записями.</span><span class="sxs-lookup"><span data-stu-id="dda32-115">**OLK_ACCOUNT_NO_FLAGS** —Synchronizes MAPI services with accounts.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="dda32-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="dda32-116">Return values</span></span>

|<span data-ttu-id="dda32-117">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dda32-117">**HRESULT**</span></span>|<span data-ttu-id="dda32-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="dda32-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dda32-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="dda32-119">S_OK</span></span>  <br/> |<span data-ttu-id="dda32-120">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="dda32-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="dda32-121">Е_ОЛК_АЛРЕАДИ_ИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="dda32-121">E_OLK_ALREADY_INITIALIZED</span></span>  <br/> |<span data-ttu-id="dda32-122">**Инициализация** уже вызвана.</span><span class="sxs-lookup"><span data-stu-id="dda32-122">**Init** has already been called.</span></span>  <br/> |
|<span data-ttu-id="dda32-123">Е_ОЛК_РЕГИСТРИ</span><span class="sxs-lookup"><span data-stu-id="dda32-123">E_OLK_REGISTRY</span></span>  <br/> |<span data-ttu-id="dda32-124">Диспетчеру учетных записей не удалось получить доступ к необходимым параметрам реестра.</span><span class="sxs-lookup"><span data-stu-id="dda32-124">The account manager could not access the required registry settings.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dda32-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="dda32-125">Remarks</span></span>

<span data-ttu-id="dda32-126">Клиент должен вызвать **иолкаккаунтманажер:: init** для инициализации диспетчера учетных записей перед использованием диспетчера учетных записей для доступа к учетным записям или настройки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="dda32-126">The client must call **IOlkAccountManager::Init** to initialize the account manager before using the account manager to access accounts or set up notifications.</span></span> <span data-ttu-id="dda32-127">Так как Outlook автоматически синхронизирует службы MAPI с учетными записями при запуске, используйте **аккт_инит_носинч_мапи_акктс** , если не существует определенной причины для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="dda32-127">Because Outlook automatically synchronizes MAPI services with accounts on startup, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** unless there is a specific cause to synchronize.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dda32-128">См. также</span><span class="sxs-lookup"><span data-stu-id="dda32-128">See also</span></span>

- [<span data-ttu-id="dda32-129">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="dda32-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

