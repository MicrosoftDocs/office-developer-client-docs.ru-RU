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
ms.openlocfilehash: 92807cb216e8a7f4eef6b4d95a8d12826b176e6e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564670"
---
# <a name="imsgserviceadminsetprimaryidentity"></a><span data-ttu-id="68b60-103">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="68b60-103">IMsgServiceAdmin::SetPrimaryIdentity</span></span>

  
  
<span data-ttu-id="68b60-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68b60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68b60-105">Назначает службы сообщений быть поставщика основной идентификатор профиля.</span><span class="sxs-lookup"><span data-stu-id="68b60-105">Designates a message service to be the supplier of the primary identity for the profile.</span></span>
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a><span data-ttu-id="68b60-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="68b60-106">Parameters</span></span>

 <span data-ttu-id="68b60-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="68b60-107">_lpUID_</span></span>
  
> <span data-ttu-id="68b60-108">[in] Указатель на структуру [MAPIUID](mapiuid.md) , который содержит уникальный идентификатор для службы сообщений для предоставления основной идентификатор или значение NULL, это означает, что **SetPrimaryIdentity** , необходимо очистить удостоверения текущего.</span><span class="sxs-lookup"><span data-stu-id="68b60-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to supply the primary identity, or NULL, which indicates that **SetPrimaryIdentity** should clear the current identity.</span></span> 
    
 <span data-ttu-id="68b60-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="68b60-109">_ulFlags_</span></span>
  
> <span data-ttu-id="68b60-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="68b60-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="68b60-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="68b60-111">Return value</span></span>

<span data-ttu-id="68b60-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="68b60-112">S_OK</span></span> 
  
> <span data-ttu-id="68b60-113">Служба сообщений успешно назначен поставщик основного удостоверения.</span><span class="sxs-lookup"><span data-stu-id="68b60-113">The message service was successfully assigned the supplier of the primary identity.</span></span>
    
<span data-ttu-id="68b60-114">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="68b60-114">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="68b60-115">**SetPrimaryIdentity** предпринята попытка указать службы сообщений, которая имеет флаг SERVICE_NO_PRIMARY_IDENTITY в своем свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="68b60-115">**SetPrimaryIdentity** attempted to designate a message service that has the SERVICE_NO_PRIMARY_IDENTITY flag set in its **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="68b60-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="68b60-116">Remarks</span></span>

<span data-ttu-id="68b60-117">Метод **IMsgServiceAdmin::SetPrimaryIdentity** устанавливает службы сообщений в качестве поставщика основной идентификатор профиля.</span><span class="sxs-lookup"><span data-stu-id="68b60-117">The **IMsgServiceAdmin::SetPrimaryIdentity** method establishes a message service as the supplier of the primary identity for the profile.</span></span> <span data-ttu-id="68b60-118">Основной идентификатор обычно имеет пользователя, выполнившего вход в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="68b60-118">The primary identity is typically the user who is logged on to the message service.</span></span> <span data-ttu-id="68b60-119">Они представляют три свойства:</span><span class="sxs-lookup"><span data-stu-id="68b60-119">It is represented by three properties:</span></span> 
  
- <span data-ttu-id="68b60-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="68b60-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span>
    
- <span data-ttu-id="68b60-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="68b60-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="68b60-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="68b60-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span>
    
<span data-ttu-id="68b60-123">Каждые поставщика услуг в службе назначенного сообщения задает эти три свойства отображаемое имя, идентификатор записи и ключа поиска сообщений пользователя, который предоставляет основного удостоверения.</span><span class="sxs-lookup"><span data-stu-id="68b60-123">Every service provider in the designated message service sets these three properties to the display name, entry identifier, and search key of the messaging user that supplies the primary identity.</span></span> <span data-ttu-id="68b60-124">Клиенты могут принимать идентификатор записи основной идентификатор путем вызова метода [IMAPISession::QueryIdentity](imapisession-queryidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="68b60-124">Clients can retrieve the primary identity's entry identifier by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method.</span></span> 
  
<span data-ttu-id="68b60-125">Свойство **PR_RESOURCE_FLAGS** имеет значение STATUS_PRIMARY_IDENTITY для каждого поставщика, который является членом службы сообщений, которая предоставляет основного удостоверения и SERVICE_PRIMARY_IDENTITY для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="68b60-125">The **PR_RESOURCE_FLAGS** property is set to STATUS_PRIMARY_IDENTITY for every provider that is a member of the message service that supplies the primary identity, and to SERVICE_PRIMARY_IDENTITY for the message service.</span></span> <span data-ttu-id="68b60-126">Если поставщик службы нельзя указывать основного удостоверения для его службы сообщений, STATUS_NO_PRIMARY_IDENTITY устанавливает **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="68b60-126">When a service provider cannot supply the primary identity for its message service, it sets **PR_RESOURCE_FLAGS** to STATUS_NO_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="68b60-127">**SetPrimaryIdentity** задает свойство **PR_RESOURCE_FLAGS** каждой службы сообщений, не предоставляющий основной идентификатор для SERVICE_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="68b60-127">**SetPrimaryIdentity** sets the **PR_RESOURCE_FLAGS** property of each message service that is not supplying the primary identity to SERVICE_NO_PRIMARY_IDENTITY.</span></span> 
  
<span data-ttu-id="68b60-128">Каждый поставщик услуг сообщение со сведениями о MAPI могут устанавливать удостоверение для каждого из пользователей при входе клиента в службу.</span><span class="sxs-lookup"><span data-stu-id="68b60-128">Each message service provider that MAPI has information about can establish an identity for each of its users when a client logs on to the service.</span></span> <span data-ttu-id="68b60-129">Тем не менее так как MAPI поддерживает соединения с несколькими поставщиками услуг для каждого сеанса MAPI, нет нет утвержденных определения удостоверение конкретного пользователя для сеанса MAPI как на единое целое; удостоверения пользователя зависит от того, какие службы участвует.</span><span class="sxs-lookup"><span data-stu-id="68b60-129">However, because MAPI supports connections to multiple service providers for each MAPI session, there is no firm definition of a particular user's identity for the MAPI session as a whole; a user's identity depends on which service is involved.</span></span> <span data-ttu-id="68b60-130">Клиенты могут вызывать **SetPrimaryIdentity** назначение одного из многих удостоверений, установленные для пользователя службы сообщений как основной идентификатор для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="68b60-130">Clients can call **SetPrimaryIdentity** to designate one of the many identities established for a user by message services as the primary identity for that user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="68b60-131">См. также</span><span class="sxs-lookup"><span data-stu-id="68b60-131">See also</span></span>



[<span data-ttu-id="68b60-132">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="68b60-132">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
  
[<span data-ttu-id="68b60-133">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="68b60-133">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="68b60-134">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="68b60-134">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

