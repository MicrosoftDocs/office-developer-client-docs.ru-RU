---
title: Иксплогонопенстатусентри
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356030"
---
# <a name="ixplogonopenstatusentry"></a><span data-ttu-id="746b6-103">IXPLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="746b6-103">IXPLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="746b6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="746b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="746b6-105">Открывает объект состояния поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="746b6-105">Opens the transport provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="746b6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="746b6-106">Parameters</span></span>

 <span data-ttu-id="746b6-107">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="746b6-107">_lpInterface_</span></span>
  
> <span data-ttu-id="746b6-108">возврата Указатель на идентификатор интерфейса (IID) для объекта входа в систему.</span><span class="sxs-lookup"><span data-stu-id="746b6-108">[in] A pointer to an interface identifier (IID) for the transport logon object.</span></span> <span data-ttu-id="746b6-109">При передаче значения NULL возвращается интерфейс [имапистатус](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="746b6-109">Passing NULL returns the [IMAPIStatus](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="746b6-110">Для параметра _лпинтерфаце_ также можно задать идентификатор для интерфейса для объекта.</span><span class="sxs-lookup"><span data-stu-id="746b6-110">The  _lpInterface_ parameter can also be set to an identifier for an interface for the object.</span></span> 
    
 <span data-ttu-id="746b6-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="746b6-111">_ulFlags_</span></span>
  
> <span data-ttu-id="746b6-112">возврата Битовая маска флагов, которые управляют способом открытия объекта Status.</span><span class="sxs-lookup"><span data-stu-id="746b6-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="746b6-113">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="746b6-113">The following flag can be set:</span></span>
    
<span data-ttu-id="746b6-114">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="746b6-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="746b6-115">ЗаПрашивает разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="746b6-115">Requests read/write permission.</span></span> <span data-ttu-id="746b6-116">Интерфейс по умолчанию доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="746b6-116">The default interface is read-only.</span></span> 
    
 <span data-ttu-id="746b6-117">_Лпулобжтипе_</span><span class="sxs-lookup"><span data-stu-id="746b6-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="746b6-118">вышли Указатель на тип открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="746b6-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="746b6-119">_Лппентри_</span><span class="sxs-lookup"><span data-stu-id="746b6-119">_lppEntry_</span></span>
  
> <span data-ttu-id="746b6-120">вышли Указатель на указатель на объект состояния Opened.</span><span class="sxs-lookup"><span data-stu-id="746b6-120">[out] A pointer to the pointer to the opened status object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="746b6-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="746b6-121">Return value</span></span>

<span data-ttu-id="746b6-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="746b6-122">S_OK</span></span> 
  
> <span data-ttu-id="746b6-123">Вызов выполнен успешно и вернул ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="746b6-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="746b6-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="746b6-124">Remarks</span></span>

<span data-ttu-id="746b6-125">Диспетчер очереди MAPI вызывает метод **иксплогон:: опенстатусентри** , когда клиентское приложение вызывает метод **OpenEntry** для идентификатора записи в строке таблицы состояний поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="746b6-125">The MAPI spooler calls the **IXPLogon::OpenStatusEntry** method when a client application calls an **OpenEntry** method for the entry identifier in the transport provider's status table row.</span></span> <span data-ttu-id="746b6-126">**Опенстатусентри** открывает объект с интерфейсом **имапистатус** , связанным с этим конкретным входным поставщиком транспорта.</span><span class="sxs-lookup"><span data-stu-id="746b6-126">**OpenStatusEntry** opens an object with the **IMAPIStatus** interface associated with this particular transport provider logon.</span></span> <span data-ttu-id="746b6-127">Затем этот объект используется, чтобы разрешить клиентским приложениям вызывать методы **имапистатус** (например, для перенастройки сеанса входа с помощью метода [Имапистатус:: сеттингсдиалог](imapistatus-settingsdialog.md) или для проверки состояния сеанса входа с помощью [ Имапистатус:: метод Валидатестате](imapistatus-validatestate.md) ).</span><span class="sxs-lookup"><span data-stu-id="746b6-127">This object is then used to enable client applications to call **IMAPIStatus** methods (for example, to reconfigure the logon session by using the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method, or to validate the state of the logon session by using the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="746b6-128">См. также</span><span class="sxs-lookup"><span data-stu-id="746b6-128">See also</span></span>



[<span data-ttu-id="746b6-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="746b6-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="746b6-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="746b6-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

