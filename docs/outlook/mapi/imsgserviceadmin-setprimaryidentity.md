---
title: имсгсервицеадминсетпримаридентити
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
# <a name="imsgserviceadminsetprimaryidentity"></a><span data-ttu-id="059d9-103">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="059d9-103">IMsgServiceAdmin::SetPrimaryIdentity</span></span>

  
  
<span data-ttu-id="059d9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="059d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="059d9-105">Назначает службу сообщений поставщику основного удостоверения для профиля.</span><span class="sxs-lookup"><span data-stu-id="059d9-105">Designates a message service to be the supplier of the primary identity for the profile.</span></span>
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a><span data-ttu-id="059d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="059d9-106">Parameters</span></span>

 <span data-ttu-id="059d9-107">_лпуид_</span><span class="sxs-lookup"><span data-stu-id="059d9-107">_lpUID_</span></span>
  
> <span data-ttu-id="059d9-108">возврата Указатель на структуру [мапиуид](mapiuid.md) , которая содержит уникальный идентификатор для службы сообщений для предоставления основного удостоверения, или значение null, которое указывает на то, что **сетпримаридентити** должен очистить текущее удостоверение.</span><span class="sxs-lookup"><span data-stu-id="059d9-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to supply the primary identity, or NULL, which indicates that **SetPrimaryIdentity** should clear the current identity.</span></span> 
    
 <span data-ttu-id="059d9-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="059d9-109">_ulFlags_</span></span>
  
> <span data-ttu-id="059d9-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="059d9-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="059d9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="059d9-111">Return value</span></span>

<span data-ttu-id="059d9-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="059d9-112">S_OK</span></span> 
  
> <span data-ttu-id="059d9-113">Поставщику службы сообщений успешно назначен поставщик основного удостоверения.</span><span class="sxs-lookup"><span data-stu-id="059d9-113">The message service was successfully assigned the supplier of the primary identity.</span></span>
    
<span data-ttu-id="059d9-114">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="059d9-114">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="059d9-115">В **сетпримаридентити** предпринята попытка назначить службу сообщений с установленным флагом SERVICE_NO_PRIMARY_IDENTITY в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="059d9-115">**SetPrimaryIdentity** attempted to designate a message service that has the SERVICE_NO_PRIMARY_IDENTITY flag set in its **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="059d9-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="059d9-116">Remarks</span></span>

<span data-ttu-id="059d9-117">Метод **имсгсервицеадмин:: сетпримаридентити** устанавливает службу сообщений в качестве поставщика основного удостоверения для профиля.</span><span class="sxs-lookup"><span data-stu-id="059d9-117">The **IMsgServiceAdmin::SetPrimaryIdentity** method establishes a message service as the supplier of the primary identity for the profile.</span></span> <span data-ttu-id="059d9-118">Обычно основным удостоверением является пользователь, который вошел в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="059d9-118">The primary identity is typically the user who is logged on to the message service.</span></span> <span data-ttu-id="059d9-119">Он представлен тремя свойствами:</span><span class="sxs-lookup"><span data-stu-id="059d9-119">It is represented by three properties:</span></span> 
  
- <span data-ttu-id="059d9-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="059d9-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span>
    
- <span data-ttu-id="059d9-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="059d9-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="059d9-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="059d9-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span>
    
<span data-ttu-id="059d9-123">Каждый поставщик услуг в назначенной службе сообщений задает эти три свойства для отображаемого имени, идентификатора записи и ключа поиска пользователя обмена сообщениями, который предоставляет основное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="059d9-123">Every service provider in the designated message service sets these three properties to the display name, entry identifier, and search key of the messaging user that supplies the primary identity.</span></span> <span data-ttu-id="059d9-124">Клиенты могут получить идентификатор записи основного идентификатора, вызвав метод [IMAPISession:: куеридентити](imapisession-queryidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="059d9-124">Clients can retrieve the primary identity's entry identifier by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method.</span></span> 
  
<span data-ttu-id="059d9-125">Для свойства **PR_RESOURCE_FLAGS** задается значение STATUS_PRIMARY_IDENTITY для каждого поставщика, который является членом службы сообщений, предоставляющей основной идентификатор, и для SERVICE_PRIMARY_IDENTITY для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="059d9-125">The **PR_RESOURCE_FLAGS** property is set to STATUS_PRIMARY_IDENTITY for every provider that is a member of the message service that supplies the primary identity, and to SERVICE_PRIMARY_IDENTITY for the message service.</span></span> <span data-ttu-id="059d9-126">Если поставщик услуг не может предоставить основной идентификатор для своей службы сообщений, он устанавливает **PR_RESOURCE_FLAGS** в STATUS_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="059d9-126">When a service provider cannot supply the primary identity for its message service, it sets **PR_RESOURCE_FLAGS** to STATUS_NO_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="059d9-127">**Сетпримаридентити** задает свойство **PR_RESOURCE_FLAGS** для каждой службы сообщений, в которой не указывается основной идентификатор SERVICE_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="059d9-127">**SetPrimaryIdentity** sets the **PR_RESOURCE_FLAGS** property of each message service that is not supplying the primary identity to SERVICE_NO_PRIMARY_IDENTITY.</span></span> 
  
<span data-ttu-id="059d9-128">Каждый поставщик службы сообщений, сведения о котором имеют MAPI, может установить удостоверение для каждого из пользователей, когда клиент входит в систему службы.</span><span class="sxs-lookup"><span data-stu-id="059d9-128">Each message service provider that MAPI has information about can establish an identity for each of its users when a client logs on to the service.</span></span> <span data-ttu-id="059d9-129">Тем не менее, так как MAPI поддерживает подключения к нескольким поставщикам услуг для каждого сеанса MAPI, отсутствует определение удостоверения определенного пользователя для сеанса MAPI в целом; удостоверение пользователя зависит от того, какая служба задействована.</span><span class="sxs-lookup"><span data-stu-id="059d9-129">However, because MAPI supports connections to multiple service providers for each MAPI session, there is no firm definition of a particular user's identity for the MAPI session as a whole; a user's identity depends on which service is involved.</span></span> <span data-ttu-id="059d9-130">Клиенты могут вызывать **сетпримаридентити** для назначения одного из множества удостоверений, установленных для пользователя службами сообщений в качестве основного удостоверения для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="059d9-130">Clients can call **SetPrimaryIdentity** to designate one of the many identities established for a user by message services as the primary identity for that user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="059d9-131">См. также</span><span class="sxs-lookup"><span data-stu-id="059d9-131">See also</span></span>



[<span data-ttu-id="059d9-132">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="059d9-132">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
  
[<span data-ttu-id="059d9-133">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="059d9-133">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="059d9-134">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="059d9-134">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

