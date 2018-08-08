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
ms.openlocfilehash: 0e96c0b99f0a5f7511ed59b483ab9409eafad882
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809626"
---
# <a name="ixplogonopenstatusentry"></a><span data-ttu-id="541c5-103">IXPLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="541c5-103">IXPLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="541c5-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="541c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="541c5-105">Открывает объект состояние поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="541c5-105">Opens the transport provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="541c5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="541c5-106">Parameters</span></span>

 <span data-ttu-id="541c5-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="541c5-107">_lpInterface_</span></span>
  
> <span data-ttu-id="541c5-108">[in] Указатель на идентификатор интерфейса (ИД интерфейса) для входа в систему объекта транспорта.</span><span class="sxs-lookup"><span data-stu-id="541c5-108">[in] A pointer to an interface identifier (IID) for the transport logon object.</span></span> <span data-ttu-id="541c5-109">Передача NULL возвращает интерфейс [IMAPIStatus](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="541c5-109">Passing NULL returns the [IMAPIStatus](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="541c5-110">Параметр _lpInterface_ можно также назначается идентификатор интерфейс для объекта.</span><span class="sxs-lookup"><span data-stu-id="541c5-110">The  _lpInterface_ parameter can also be set to an identifier for an interface for the object.</span></span> 
    
 <span data-ttu-id="541c5-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="541c5-111">_ulFlags_</span></span>
  
> <span data-ttu-id="541c5-112">[in] Битовая маска флаги, который определяет способ открытия объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="541c5-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="541c5-113">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="541c5-113">The following flag can be set:</span></span>
    
<span data-ttu-id="541c5-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="541c5-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="541c5-115">Запросы на разрешение чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="541c5-115">Requests read/write permission.</span></span> <span data-ttu-id="541c5-116">Интерфейс по умолчанию доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="541c5-116">The default interface is read-only.</span></span> 
    
 <span data-ttu-id="541c5-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="541c5-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="541c5-118">[out] Указатель на тип объекта открыт.</span><span class="sxs-lookup"><span data-stu-id="541c5-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="541c5-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="541c5-119">_lppEntry_</span></span>
  
> <span data-ttu-id="541c5-120">[out] Указатель на указатель на объект открыт состояние.</span><span class="sxs-lookup"><span data-stu-id="541c5-120">[out] A pointer to the pointer to the opened status object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="541c5-121">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="541c5-121">Return value</span></span>

<span data-ttu-id="541c5-122">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="541c5-122">S_OK</span></span> 
  
> <span data-ttu-id="541c5-123">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="541c5-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="541c5-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="541c5-124">Remarks</span></span>

<span data-ttu-id="541c5-125">Диспетчер очереди MAPI вызывает метод **IXPLogon::OpenStatusEntry** , когда клиентское приложение вызывает метод **OpenEntry** идентификатор записи поставщика транспорта состояние строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="541c5-125">The MAPI spooler calls the **IXPLogon::OpenStatusEntry** method when a client application calls an **OpenEntry** method for the entry identifier in the transport provider's status table row.</span></span> <span data-ttu-id="541c5-126">**OpenStatusEntry** открывает объект с помощью интерфейса **IMAPIStatus** , связанный с этой конкретной транспорта поставщика входа.</span><span class="sxs-lookup"><span data-stu-id="541c5-126">**OpenStatusEntry** opens an object with the **IMAPIStatus** interface associated with this particular transport provider logon.</span></span> <span data-ttu-id="541c5-127">Этот объект используется для включения клиентских приложений для вызова метода **IMAPIStatus** (например, чтобы снова настроить сеанса входа в систему с помощью метода [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) , или для проверки состояния сеанса входа в систему с помощью [ IMAPIStatus::ValidateState](imapistatus-validatestate.md) метод).</span><span class="sxs-lookup"><span data-stu-id="541c5-127">This object is then used to enable client applications to call **IMAPIStatus** methods (for example, to reconfigure the logon session by using the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method, or to validate the state of the logon session by using the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="541c5-128">См. также</span><span class="sxs-lookup"><span data-stu-id="541c5-128">See also</span></span>



[<span data-ttu-id="541c5-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="541c5-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="541c5-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="541c5-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

