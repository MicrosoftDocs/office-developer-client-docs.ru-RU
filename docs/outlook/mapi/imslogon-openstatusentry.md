---
title: IMSLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 850e256b-6b50-428c-aede-287edaf7b005
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f50c0eb9e3af68e206eaa5bcc51cefa923c30f72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413180"
---
# <a name="imslogonopenstatusentry"></a><span data-ttu-id="a8a2a-103">IMSLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="a8a2a-103">IMSLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="a8a2a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8a2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8a2a-105">Открывает объект состояния.</span><span class="sxs-lookup"><span data-stu-id="a8a2a-105">Opens a status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="a8a2a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8a2a-106">Parameters</span></span>

 <span data-ttu-id="a8a2a-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a8a2a-107">_lpInterface_</span></span>
  
> <span data-ttu-id="a8a2a-108">[in] Указатель на идентификатор интерфейса (IID) для открываемого объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="a8a2a-108">[in] A pointer to the interface identifier (IID) for the status object to open.</span></span> <span data-ttu-id="a8a2a-109">Передача NULL означает, что возвращается стандартный интерфейс для объекта (в данном случае интерфейс [IMAPIStatus).](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="a8a2a-109">Passing NULL indicates the standard interface for the object is returned (in this case, the [IMAPIStatus](imapistatusimapiprop.md) interface).</span></span> <span data-ttu-id="a8a2a-110">Параметр  _lpInterface_ также может быть задан в качестве идентификатора для соответствующего интерфейса объекта.</span><span class="sxs-lookup"><span data-stu-id="a8a2a-110">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="a8a2a-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a8a2a-111">_ulFlags_</span></span>
  
> <span data-ttu-id="a8a2a-112">[in] Битоваяmas флагов, которая управляет открытием объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="a8a2a-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="a8a2a-113">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a8a2a-113">The following flag can be set:</span></span>
    
<span data-ttu-id="a8a2a-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="a8a2a-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="a8a2a-115">Запрашивает разрешение на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="a8a2a-115">Requests read/write permission.</span></span> <span data-ttu-id="a8a2a-116">По умолчанию объекты создаются с разрешением только на чтение, и клиентские приложения не должны работать при предположении, что разрешение на чтение и записи было предоставлено.</span><span class="sxs-lookup"><span data-stu-id="a8a2a-116">By default, objects are created with read-only permission, and client applications should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="a8a2a-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="a8a2a-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="a8a2a-118">[out] Указатель на тип открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="a8a2a-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="a8a2a-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="a8a2a-119">_lppEntry_</span></span>
  
> <span data-ttu-id="a8a2a-120">[out] Указатель на указатель на открытый объект.</span><span class="sxs-lookup"><span data-stu-id="a8a2a-120">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a8a2a-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8a2a-121">Return value</span></span>

<span data-ttu-id="a8a2a-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8a2a-122">S_OK</span></span> 
  
> <span data-ttu-id="a8a2a-123">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="a8a2a-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a8a2a-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="a8a2a-124">Remarks</span></span>

<span data-ttu-id="a8a2a-125">Поставщики store сообщений реализуют метод **IMSLogon::OpenStatusEntry** для открытия объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="a8a2a-125">Message store providers implement the **IMSLogon::OpenStatusEntry** method to open a status object.</span></span> <span data-ttu-id="a8a2a-126">Этот объект состояния затем используется для того, чтобы клиенты могли вызывать методы [IMAPIStatus.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="a8a2a-126">This status object is then used to enable clients to call [IMAPIStatus](imapistatusimapiprop.md) methods.</span></span> <span data-ttu-id="a8a2a-127">Например, клиенты могут использовать метод [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) для перенастройки сеанса работы с хранилищем сообщений или метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) для проверки состояния сеанса для сеанса для работы с хранилищем сообщений.</span><span class="sxs-lookup"><span data-stu-id="a8a2a-127">For example, clients can use the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method to reconfigure the message store logon session or the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method to validate the state of the message store logon session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8a2a-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a8a2a-128">See also</span></span>



[<span data-ttu-id="a8a2a-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a8a2a-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="a8a2a-130">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="a8a2a-130">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="a8a2a-131">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="a8a2a-131">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="a8a2a-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a8a2a-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

