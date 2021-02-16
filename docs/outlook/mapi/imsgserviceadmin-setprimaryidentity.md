---
title: IMsgServiceAdminSetPrimaryIdentity
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.SetPrimaryIdentity
api_type:
- COM
ms.assetid: 763cab41-f6f6-4cb0-8cb8-170fdf2a92e6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b237a57dfea020c7bfcb66d49d43428c1f6506c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430366"
---
# <a name="imsgserviceadminsetprimaryidentity"></a><span data-ttu-id="8ba8b-103">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="8ba8b-103">IMsgServiceAdmin::SetPrimaryIdentity</span></span>

  
  
<span data-ttu-id="8ba8b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ba8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ba8b-105">Назначает службу сообщений поставщиком основного удостоверения для профиля.</span><span class="sxs-lookup"><span data-stu-id="8ba8b-105">Designates a message service to be the supplier of the primary identity for the profile.</span></span>
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a><span data-ttu-id="8ba8b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ba8b-106">Parameters</span></span>

 <span data-ttu-id="8ba8b-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="8ba8b-107">_lpUID_</span></span>
  
> <span data-ttu-id="8ba8b-108">[in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор для службы сообщений, чтобы предоставить основное удостоверение, или NULL, которое указывает, **что SetPrimaryIdentity** должен очистить текущее удостоверение.</span><span class="sxs-lookup"><span data-stu-id="8ba8b-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to supply the primary identity, or NULL, which indicates that **SetPrimaryIdentity** should clear the current identity.</span></span> 
    
 <span data-ttu-id="8ba8b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8ba8b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="8ba8b-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="8ba8b-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8ba8b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ba8b-111">Return value</span></span>

<span data-ttu-id="8ba8b-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="8ba8b-112">S_OK</span></span> 
  
> <span data-ttu-id="8ba8b-113">Службе сообщений успешно назначен поставщик основного удостоверения.</span><span class="sxs-lookup"><span data-stu-id="8ba8b-113">The message service was successfully assigned the supplier of the primary identity.</span></span>
    
<span data-ttu-id="8ba8b-114">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8ba8b-114">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="8ba8b-115">**SetPrimaryIdentity** попытался назначить службу сообщений с флагом SERVICE_NO_PRIMARY_IDENTITY в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags).](pidtagresourceflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8ba8b-115">**SetPrimaryIdentity** attempted to designate a message service that has the SERVICE_NO_PRIMARY_IDENTITY flag set in its **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8ba8b-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ba8b-116">Remarks</span></span>

<span data-ttu-id="8ba8b-117">Метод **IMsgServiceAdmin::SetPrimaryIdentity** устанавливает службу сообщений в качестве поставщика основного удостоверения для профиля.</span><span class="sxs-lookup"><span data-stu-id="8ba8b-117">The **IMsgServiceAdmin::SetPrimaryIdentity** method establishes a message service as the supplier of the primary identity for the profile.</span></span> <span data-ttu-id="8ba8b-118">Как правило, основным удостоверением является пользователь, который вошел в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="8ba8b-118">The primary identity is typically the user who is logged on to the message service.</span></span> <span data-ttu-id="8ba8b-119">Он представлен тремя свойствами:</span><span class="sxs-lookup"><span data-stu-id="8ba8b-119">It is represented by three properties:</span></span> 
  
- <span data-ttu-id="8ba8b-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay)](pidtagidentitydisplay-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8ba8b-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span>
    
- <span data-ttu-id="8ba8b-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId)](pidtagidentityentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8ba8b-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="8ba8b-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey)](pidtagidentitysearchkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8ba8b-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span>
    
<span data-ttu-id="8ba8b-123">Каждый поставщик услуг в назначенной службе сообщений задает эти три свойства в качестве отображаемого имени, идентификатора записи и ключа поиска пользователя обмена сообщениями, который указывает основное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="8ba8b-123">Every service provider in the designated message service sets these three properties to the display name, entry identifier, and search key of the messaging user that supplies the primary identity.</span></span> <span data-ttu-id="8ba8b-124">Клиенты могут получить идентификатор записи основного удостоверения, вызывая метод [IMAPISession::QueryIdentity.](imapisession-queryidentity.md)</span><span class="sxs-lookup"><span data-stu-id="8ba8b-124">Clients can retrieve the primary identity's entry identifier by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method.</span></span> 
  
<span data-ttu-id="8ba8b-125">Свойство **PR_RESOURCE_FLAGS** устанавливается STATUS_PRIMARY_IDENTITY для каждого поставщика, который является членом службы сообщений, который обеспечивает основное удостоверение, и SERVICE_PRIMARY_IDENTITY для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="8ba8b-125">The **PR_RESOURCE_FLAGS** property is set to STATUS_PRIMARY_IDENTITY for every provider that is a member of the message service that supplies the primary identity, and to SERVICE_PRIMARY_IDENTITY for the message service.</span></span> <span data-ttu-id="8ba8b-126">Если поставщик службы не может предоставить основное  удостоверение для службы сообщений, он PR_RESOURCE_FLAGS STATUS_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="8ba8b-126">When a service provider cannot supply the primary identity for its message service, it sets **PR_RESOURCE_FLAGS** to STATUS_NO_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="8ba8b-127">**SetPrimaryIdentity** задает **PR_RESOURCE_FLAGS** службы сообщений, которая не задает основное удостоверение для SERVICE_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="8ba8b-127">**SetPrimaryIdentity** sets the **PR_RESOURCE_FLAGS** property of each message service that is not supplying the primary identity to SERVICE_NO_PRIMARY_IDENTITY.</span></span> 
  
<span data-ttu-id="8ba8b-128">Каждый поставщик услуг сообщений, сведения о которых есть в MAPI, может установить удостоверение для каждого из своих пользователей при входе клиента в службу.</span><span class="sxs-lookup"><span data-stu-id="8ba8b-128">Each message service provider that MAPI has information about can establish an identity for each of its users when a client logs on to the service.</span></span> <span data-ttu-id="8ba8b-129">Однако поскольку MAPI поддерживает подключения к нескольким поставщикам услуг для каждого сеанса MAPI, нет четкого определения удостоверения конкретного пользователя для сеанса MAPI в целом; Удостоверение пользователя зависит от того, какая служба задействована.</span><span class="sxs-lookup"><span data-stu-id="8ba8b-129">However, because MAPI supports connections to multiple service providers for each MAPI session, there is no firm definition of a particular user's identity for the MAPI session as a whole; a user's identity depends on which service is involved.</span></span> <span data-ttu-id="8ba8b-130">Клиенты могут вызывать **SetPrimaryIdentity,** чтобы назначить одно из множества удостоверений, установленных для пользователя службами сообщений, в качестве основного удостоверения для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ba8b-130">Clients can call **SetPrimaryIdentity** to designate one of the many identities established for a user by message services as the primary identity for that user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8ba8b-131">См. также</span><span class="sxs-lookup"><span data-stu-id="8ba8b-131">See also</span></span>



[<span data-ttu-id="8ba8b-132">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="8ba8b-132">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
  
[<span data-ttu-id="8ba8b-133">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="8ba8b-133">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="8ba8b-134">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8ba8b-134">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

