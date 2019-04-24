---
title: Имсгсервицеадминкопимсгсервице
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CopyMsgService
api_type:
- COM
ms.assetid: a13c6757-358f-421a-9a76-de7483501613
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 72b4ab1fec10b2e91c7609af6644a54d29ed5e02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309970"
---
# <a name="imsgserviceadmincopymsgservice"></a><span data-ttu-id="08c59-103">IMsgServiceAdmin::CopyMsgService</span><span class="sxs-lookup"><span data-stu-id="08c59-103">IMsgServiceAdmin::CopyMsgService</span></span>

  
  
<span data-ttu-id="08c59-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08c59-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08c59-105">Копирует службу сообщений в профиль.</span><span class="sxs-lookup"><span data-stu-id="08c59-105">Copies a message service into a profile.</span></span> 
  
```cpp
HRESULT CopyMsgService(
  LPMAPIUID lpUID,
  LPSTR lpszDisplayName,
  LPCIID lpInterfaceToCopy,
  LPCIID lpInterfaceDst,
  LPVOID lpObjectDst,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="08c59-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="08c59-106">Parameters</span></span>

 <span data-ttu-id="08c59-107">_Лпуид_</span><span class="sxs-lookup"><span data-stu-id="08c59-107">_lpUID_</span></span>
  
> <span data-ttu-id="08c59-108">возврата Указатель на структуру [мапиуид](mapiuid.md) , которая содержит уникальный идентификатор службы сообщений для копирования.</span><span class="sxs-lookup"><span data-stu-id="08c59-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier of the message service to copy.</span></span> 
    
 <span data-ttu-id="08c59-109">_Лпсздисплайнаме_</span><span class="sxs-lookup"><span data-stu-id="08c59-109">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="08c59-110">возврата Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="08c59-110">[in] This parameter has been deprecated.</span></span> 
    
 <span data-ttu-id="08c59-111">_Лпинтерфацетокопи_</span><span class="sxs-lookup"><span data-stu-id="08c59-111">_lpInterfaceToCopy_</span></span>
  
> <span data-ttu-id="08c59-112">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к разделу профиля службы сообщений, который необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="08c59-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section of the message service to copy.</span></span> <span data-ttu-id="08c59-113">При передаче значений NULL в стандартный раздел профиля используется интерфейс [ипрофсект](iprofsectimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="08c59-113">Passing NULL results in the standard profile section interface, [IProfSect](iprofsectimapiprop.md), being used.</span></span>
    
 <span data-ttu-id="08c59-114">_Лпинтерфацедст_</span><span class="sxs-lookup"><span data-stu-id="08c59-114">_lpInterfaceDst_</span></span>
  
> <span data-ttu-id="08c59-115">возврата Указатель на идентификатор IID, представляющий интерфейс, который будет использоваться для доступа к объекту, на который указывает параметр _лпобжектдст_ .</span><span class="sxs-lookup"><span data-stu-id="08c59-115">[in] A pointer to the IID that represents the interface to be used to access the object pointed to by the  _lpObjectDst_ parameter.</span></span> <span data-ttu-id="08c59-116">Передача результатов NULL в интерфейс сеанса [IMAPISession](imapisessioniunknown.md)используется.</span><span class="sxs-lookup"><span data-stu-id="08c59-116">Passing NULL results in the session interface, [IMAPISession](imapisessioniunknown.md), being used.</span></span> <span data-ttu-id="08c59-117">Для параметра _лпинтерфацедст_ также можно задать значение иид_имсгсервицеадмин.</span><span class="sxs-lookup"><span data-stu-id="08c59-117">The  _lpInterfaceDst_ parameter can also be set to IID_IMsgServiceAdmin.</span></span> 
    
 <span data-ttu-id="08c59-118">_Лпобжектдст_</span><span class="sxs-lookup"><span data-stu-id="08c59-118">_lpObjectDst_</span></span>
  
> <span data-ttu-id="08c59-119">возврата Указатель на указатель на объект администрирования службы сеансов или службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="08c59-119">[in] A pointer to a pointer to a session or message service administration object.</span></span> <span data-ttu-id="08c59-120">Тип объекта должен соответствовать идентификатору интерфейса, переданному в _лпинтерфацедст_.</span><span class="sxs-lookup"><span data-stu-id="08c59-120">The type of object should correspond to the interface identifier passed in  _lpInterfaceDst_.</span></span> <span data-ttu-id="08c59-121">Допустимыми указателями объектов являются ЛПМАПИСЕССИОН и ЛПСЕРВИЦЕАДМИН.</span><span class="sxs-lookup"><span data-stu-id="08c59-121">Valid object pointers are LPMAPISESSION and LPSERVICEADMIN.</span></span>
    
 <span data-ttu-id="08c59-122">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="08c59-122">_ulUIParam_</span></span>
  
> <span data-ttu-id="08c59-123">возврата Дескриптор родительского окна любых диалоговых окон или окон, которые отображает этот метод.</span><span class="sxs-lookup"><span data-stu-id="08c59-123">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="08c59-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="08c59-124">_ulFlags_</span></span>
  
> <span data-ttu-id="08c59-125">возврата Битовая маска флагов, определяющих способ копирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="08c59-125">[in] A bitmask of flags that controls how the message service is copied.</span></span> <span data-ttu-id="08c59-126">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="08c59-126">The following flags can be set:</span></span>
    
<span data-ttu-id="08c59-127">СЕРВИЦЕ_УИ_АЛВАЙС</span><span class="sxs-lookup"><span data-stu-id="08c59-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="08c59-128">Запросы, которые служба сообщений всегда отображает страницу свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="08c59-128">Requests that the message service always display a configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="08c59-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08c59-129">Return value</span></span>

<span data-ttu-id="08c59-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="08c59-130">S_OK</span></span> 
  
> <span data-ttu-id="08c59-131">Служба сообщений успешно скопирована.</span><span class="sxs-lookup"><span data-stu-id="08c59-131">The message service was successfully copied.</span></span>
    
<span data-ttu-id="08c59-132">МАПИ_Е_НО_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="08c59-132">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="08c59-133">Служба сообщений уже включена в профиль и не поддерживает несколько экземпляров.</span><span class="sxs-lookup"><span data-stu-id="08c59-133">The message service is already in the profile and does not allow multiple instances of itself.</span></span>
    
<span data-ttu-id="08c59-134">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="08c59-134">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="08c59-135">**Мапиуид** , на который указывает _лпуид_ , не ссылается на существующую службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="08c59-135">The **MAPIUID** pointed to by  _lpUID_ does not refer to an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="08c59-136">Замечания</span><span class="sxs-lookup"><span data-stu-id="08c59-136">Remarks</span></span>

<span data-ttu-id="08c59-137">Метод **имсгсервицеадмин:: копимсгсервице** копирует службу сообщений в профиль, активный профиль или другой профиль.</span><span class="sxs-lookup"><span data-stu-id="08c59-137">The **IMsgServiceAdmin::CopyMsgService** method copies a message service into a profile, either the active profile or another profile.</span></span> <span data-ttu-id="08c59-138">Профиль, содержащий службу сообщений, которую необходимо скопировать, и конечное расположение не обязательно должно быть одним и тем же профилем, но это может быть.</span><span class="sxs-lookup"><span data-stu-id="08c59-138">The profile that contains the message service to be copied and the destination do not have to be the same profile, but they can be.</span></span> 
  
<span data-ttu-id="08c59-139">Функция точки входа службы сообщений не вызывается для операции копирования.</span><span class="sxs-lookup"><span data-stu-id="08c59-139">The message service's entry point function is not called for a copy operation.</span></span> <span data-ttu-id="08c59-140">Скопированная служба сообщений имеет те же параметры конфигурации, что и ее оригинал.</span><span class="sxs-lookup"><span data-stu-id="08c59-140">The copied message service has the same configuration settings as its original.</span></span> <span data-ttu-id="08c59-141">Чтобы изменить эти параметры, клиент должен вызвать метод [имсгсервицеадмин:: конфигуремсгсервице](imsgserviceadmin-configuremsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="08c59-141">To change these settings, a client should call the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="08c59-142">См. также</span><span class="sxs-lookup"><span data-stu-id="08c59-142">See also</span></span>



[<span data-ttu-id="08c59-143">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="08c59-143">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="08c59-144">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="08c59-144">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="08c59-145">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="08c59-145">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

