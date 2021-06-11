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
ms.openlocfilehash: d9e09de1064a0ae034bb3618f0e5b3719a82c163
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435903"
---
# <a name="ixplogonopenstatusentry"></a><span data-ttu-id="098c2-103">IXPLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="098c2-103">IXPLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="098c2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="098c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="098c2-105">Открывает объект состояния поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="098c2-105">Opens the transport provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="098c2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="098c2-106">Parameters</span></span>

 <span data-ttu-id="098c2-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="098c2-107">_lpInterface_</span></span>
  
> <span data-ttu-id="098c2-108">[in] Указатель на идентификатор интерфейса (IID) для объекта транспортного логотипа.</span><span class="sxs-lookup"><span data-stu-id="098c2-108">[in] A pointer to an interface identifier (IID) for the transport logon object.</span></span> <span data-ttu-id="098c2-109">Передача NULL возвращает [интерфейс IMAPIStatus.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="098c2-109">Passing NULL returns the [IMAPIStatus](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="098c2-110">Параметр  _lpInterface_ также может быть задан идентификатору интерфейса объекта.</span><span class="sxs-lookup"><span data-stu-id="098c2-110">The  _lpInterface_ parameter can also be set to an identifier for an interface for the object.</span></span> 
    
 <span data-ttu-id="098c2-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="098c2-111">_ulFlags_</span></span>
  
> <span data-ttu-id="098c2-112">[in] Битмашка флагов, контролируемая тем, как открывается объект состояния.</span><span class="sxs-lookup"><span data-stu-id="098c2-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="098c2-113">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="098c2-113">The following flag can be set:</span></span>
    
<span data-ttu-id="098c2-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="098c2-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="098c2-115">Запросы на чтение и написание разрешений.</span><span class="sxs-lookup"><span data-stu-id="098c2-115">Requests read/write permission.</span></span> <span data-ttu-id="098c2-116">Интерфейс по умолчанию только для чтения.</span><span class="sxs-lookup"><span data-stu-id="098c2-116">The default interface is read-only.</span></span> 
    
 <span data-ttu-id="098c2-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="098c2-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="098c2-118">[вышел] Указатель на тип открываемого объекта.</span><span class="sxs-lookup"><span data-stu-id="098c2-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="098c2-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="098c2-119">_lppEntry_</span></span>
  
> <span data-ttu-id="098c2-120">[вышел] Указатель на указатель на открытый объект состояния.</span><span class="sxs-lookup"><span data-stu-id="098c2-120">[out] A pointer to the pointer to the opened status object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="098c2-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="098c2-121">Return value</span></span>

<span data-ttu-id="098c2-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="098c2-122">S_OK</span></span> 
  
> <span data-ttu-id="098c2-123">Вызов удался и возвращает ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="098c2-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="098c2-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="098c2-124">Remarks</span></span>

<span data-ttu-id="098c2-125">Spooler MAPI вызывает метод **IXPLogon::OpenStatusEntry,** когда клиентская заявка вызывает метод **OpenEntry** для идентификатора входа в строке таблицы состояния поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="098c2-125">The MAPI spooler calls the **IXPLogon::OpenStatusEntry** method when a client application calls an **OpenEntry** method for the entry identifier in the transport provider's status table row.</span></span> <span data-ttu-id="098c2-126">**OpenStatusEntry** открывает объект с интерфейсом **IMAPIStatus,** связанным с этим логотипом поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="098c2-126">**OpenStatusEntry** opens an object with the **IMAPIStatus** interface associated with this particular transport provider logon.</span></span> <span data-ttu-id="098c2-127">Этот объект затем используется для того, чтобы клиентские приложения могли вызывать методы **IMAPIStatus** (например, для перенастройки сеанса логотипа с помощью метода [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) или проверки состояния сеанса логона с помощью метода [IMAPIStatus::ValidateState).](imapistatus-validatestate.md)</span><span class="sxs-lookup"><span data-stu-id="098c2-127">This object is then used to enable client applications to call **IMAPIStatus** methods (for example, to reconfigure the logon session by using the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method, or to validate the state of the logon session by using the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="098c2-128">См. также</span><span class="sxs-lookup"><span data-stu-id="098c2-128">See also</span></span>



[<span data-ttu-id="098c2-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="098c2-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="098c2-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="098c2-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

