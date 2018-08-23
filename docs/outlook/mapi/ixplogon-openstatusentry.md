---
title: IXPLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 261d5f7c-bb61-4e1d-aa41-cca224c63f8e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7cb77308ebc7229adcab290fc8e1f9e11ce45065
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587021"
---
# <a name="ixplogonopenstatusentry"></a><span data-ttu-id="0bcbc-103">IXPLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="0bcbc-103">IXPLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="0bcbc-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0bcbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0bcbc-105">Открывает объект состояние поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="0bcbc-105">Opens the transport provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="0bcbc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bcbc-106">Parameters</span></span>

 <span data-ttu-id="0bcbc-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0bcbc-107">_lpInterface_</span></span>
  
> <span data-ttu-id="0bcbc-108">[in] Указатель на идентификатор интерфейса (ИД интерфейса) для входа в систему объекта транспорта.</span><span class="sxs-lookup"><span data-stu-id="0bcbc-108">[in] A pointer to an interface identifier (IID) for the transport logon object.</span></span> <span data-ttu-id="0bcbc-109">Передача NULL возвращает интерфейс [IMAPIStatus](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="0bcbc-109">Passing NULL returns the [IMAPIStatus](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="0bcbc-110">Параметр _lpInterface_ можно также назначается идентификатор интерфейс для объекта.</span><span class="sxs-lookup"><span data-stu-id="0bcbc-110">The  _lpInterface_ parameter can also be set to an identifier for an interface for the object.</span></span> 
    
 <span data-ttu-id="0bcbc-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0bcbc-111">_ulFlags_</span></span>
  
> <span data-ttu-id="0bcbc-112">[in] Битовая маска флаги, который определяет способ открытия объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="0bcbc-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="0bcbc-113">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="0bcbc-113">The following flag can be set:</span></span>
    
<span data-ttu-id="0bcbc-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="0bcbc-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="0bcbc-115">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0bcbc-115">Requests read/write permission.</span></span> <span data-ttu-id="0bcbc-116">Интерфейс по умолчанию доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0bcbc-116">The default interface is read-only.</span></span> 
    
 <span data-ttu-id="0bcbc-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="0bcbc-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="0bcbc-118">[out] Указатель на тип объекта открыт.</span><span class="sxs-lookup"><span data-stu-id="0bcbc-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="0bcbc-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="0bcbc-119">_lppEntry_</span></span>
  
> <span data-ttu-id="0bcbc-120">[out] Указатель на указатель на объект открыт состояние.</span><span class="sxs-lookup"><span data-stu-id="0bcbc-120">[out] A pointer to the pointer to the opened status object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0bcbc-121">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0bcbc-121">Return value</span></span>

<span data-ttu-id="0bcbc-122">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="0bcbc-122">S_OK</span></span> 
  
> <span data-ttu-id="0bcbc-123">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="0bcbc-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0bcbc-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="0bcbc-124">Remarks</span></span>

<span data-ttu-id="0bcbc-125">Диспетчер очереди MAPI вызывает метод **IXPLogon::OpenStatusEntry** , когда клиентское приложение вызывает метод **OpenEntry** идентификатор записи поставщика транспорта состояние строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="0bcbc-125">The MAPI spooler calls the **IXPLogon::OpenStatusEntry** method when a client application calls an **OpenEntry** method for the entry identifier in the transport provider's status table row.</span></span> <span data-ttu-id="0bcbc-126">**OpenStatusEntry** открывает объект с помощью интерфейса **IMAPIStatus** , связанный с этой конкретной транспорта поставщика входа.</span><span class="sxs-lookup"><span data-stu-id="0bcbc-126">**OpenStatusEntry** opens an object with the **IMAPIStatus** interface associated with this particular transport provider logon.</span></span> <span data-ttu-id="0bcbc-127">Этот объект используется для включения клиентских приложений для вызова метода **IMAPIStatus** (например, чтобы снова настроить сеанса входа в систему с помощью метода [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) , или для проверки состояния сеанса входа в систему с помощью [ IMAPIStatus::ValidateState](imapistatus-validatestate.md) метод).</span><span class="sxs-lookup"><span data-stu-id="0bcbc-127">This object is then used to enable client applications to call **IMAPIStatus** methods (for example, to reconfigure the logon session by using the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method, or to validate the state of the logon session by using the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0bcbc-128">См. также</span><span class="sxs-lookup"><span data-stu-id="0bcbc-128">See also</span></span>



[<span data-ttu-id="0bcbc-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0bcbc-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="0bcbc-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0bcbc-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

