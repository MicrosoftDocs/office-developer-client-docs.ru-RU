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
# <a name="imslogonopenstatusentry"></a><span data-ttu-id="7d290-103">IMSLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="7d290-103">IMSLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="7d290-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d290-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d290-105">Открывает объект состояния.</span><span class="sxs-lookup"><span data-stu-id="7d290-105">Opens a status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="7d290-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="7d290-106">Parameters</span></span>

 <span data-ttu-id="7d290-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="7d290-107">_lpInterface_</span></span>
  
> <span data-ttu-id="7d290-108">[in] Указатель на идентификатор интерфейса (IID) для открытия объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="7d290-108">[in] A pointer to the interface identifier (IID) for the status object to open.</span></span> <span data-ttu-id="7d290-109">Передача NULL указывает, что возвращается стандартный интерфейс объекта (в данном случае интерфейс [IMAPIStatus).](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="7d290-109">Passing NULL indicates the standard interface for the object is returned (in this case, the [IMAPIStatus](imapistatusimapiprop.md) interface).</span></span> <span data-ttu-id="7d290-110">Параметр  _lpInterface_ также может быть задан идентификатору для соответствующего интерфейса объекта.</span><span class="sxs-lookup"><span data-stu-id="7d290-110">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="7d290-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7d290-111">_ulFlags_</span></span>
  
> <span data-ttu-id="7d290-112">[in] Битмашка флагов, контролируемая тем, как открывается объект состояния.</span><span class="sxs-lookup"><span data-stu-id="7d290-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="7d290-113">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="7d290-113">The following flag can be set:</span></span>
    
<span data-ttu-id="7d290-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="7d290-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="7d290-115">Запросы на чтение и написание разрешений.</span><span class="sxs-lookup"><span data-stu-id="7d290-115">Requests read/write permission.</span></span> <span data-ttu-id="7d290-116">По умолчанию объекты создаются с разрешения только для чтения, и клиентские приложения не должны работать на предположении, что разрешение на чтение и записи было предоставлено.</span><span class="sxs-lookup"><span data-stu-id="7d290-116">By default, objects are created with read-only permission, and client applications should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="7d290-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="7d290-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="7d290-118">[вышел] Указатель на тип открываемого объекта.</span><span class="sxs-lookup"><span data-stu-id="7d290-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="7d290-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="7d290-119">_lppEntry_</span></span>
  
> <span data-ttu-id="7d290-120">[вышел] Указатель на указатель на открытый объект.</span><span class="sxs-lookup"><span data-stu-id="7d290-120">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7d290-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d290-121">Return value</span></span>

<span data-ttu-id="7d290-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="7d290-122">S_OK</span></span> 
  
> <span data-ttu-id="7d290-123">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="7d290-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d290-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="7d290-124">Remarks</span></span>

<span data-ttu-id="7d290-125">Поставщики магазинов сообщений реализуют **метод IMSLogon::OpenStatusEntry** для открытия объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="7d290-125">Message store providers implement the **IMSLogon::OpenStatusEntry** method to open a status object.</span></span> <span data-ttu-id="7d290-126">Этот объект состояния затем используется для того, чтобы клиенты могли вызывать [методы IMAPIStatus.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="7d290-126">This status object is then used to enable clients to call [IMAPIStatus](imapistatusimapiprop.md) methods.</span></span> <span data-ttu-id="7d290-127">Например, клиенты могут использовать метод [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) для перенастройки сеанса логотипа магазина сообщений или метода [IMAPIStatus::ValidateState](imapistatus-validatestate.md) для проверки состояния сеанса логотипа магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="7d290-127">For example, clients can use the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method to reconfigure the message store logon session or the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method to validate the state of the message store logon session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7d290-128">См. также</span><span class="sxs-lookup"><span data-stu-id="7d290-128">See also</span></span>



[<span data-ttu-id="7d290-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7d290-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="7d290-130">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="7d290-130">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="7d290-131">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="7d290-131">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="7d290-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d290-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

