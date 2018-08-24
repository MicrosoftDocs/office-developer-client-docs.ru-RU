---
title: IMAPISupportGetSvcConfigSupportObj
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetSvcConfigSupportObj
api_type:
- COM
ms.assetid: 56c3bdae-a3a8-4334-b6d2-a89c6820d72e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1c48ceefa84658b236b8dfa4e10df18c175d920e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595162"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a><span data-ttu-id="dad78-103">IMAPISupport::GetSvcConfigSupportObj</span><span class="sxs-lookup"><span data-stu-id="dad78-103">IMAPISupport::GetSvcConfigSupportObj</span></span>

  
  
<span data-ttu-id="dad78-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dad78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dad78-105">Создает объект сообщения службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="dad78-105">Creates a message service support object.</span></span>
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a><span data-ttu-id="dad78-106">���������</span><span class="sxs-lookup"><span data-stu-id="dad78-106">Parameters</span></span>

 <span data-ttu-id="dad78-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dad78-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dad78-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="dad78-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="dad78-109">_lppSvcSupport_</span><span class="sxs-lookup"><span data-stu-id="dad78-109">_lppSvcSupport_</span></span>
  
> <span data-ttu-id="dad78-110">[out] Указатель на указатель на новый объект сообщения службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="dad78-110">[out] A pointer to a pointer to the new message service support object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dad78-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="dad78-111">Return value</span></span>

<span data-ttu-id="dad78-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="dad78-112">S_OK</span></span> 
  
> <span data-ttu-id="dad78-113">Объект поддержки конфигурации успешно создан.</span><span class="sxs-lookup"><span data-stu-id="dad78-113">The configuration support object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dad78-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="dad78-114">Remarks</span></span>

<span data-ttu-id="dad78-115">Метод **IMAPISupport::GetSvcConfigSupportObj** применяется для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="dad78-115">The **IMAPISupport::GetSvcConfigSupportObj** method is implemented for all support objects.</span></span> <span data-ttu-id="dad78-116">Поставщики услуг вызова **GetSvcConfigSupportObj** для создания объекта поддержки конфигурации для передачи сообщений функции точки входа службы.</span><span class="sxs-lookup"><span data-stu-id="dad78-116">Service providers call **GetSvcConfigSupportObj** to create a configuration support object to pass to a message service entry point function.</span></span> 
  
<span data-ttu-id="dad78-117">Функция точки входа службы сообщений на основании прототип [MSGSERVICEENTRY](msgserviceentry.md) и вызывается методы интерфейса [IMsgServiceAdmin](imsgserviceadminiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="dad78-117">A message service entry point function is based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype and is called by methods of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) interface.</span></span> <span data-ttu-id="dad78-118">Функция точки входа службы сообщений позволяет службам сообщение настраиваться или другие действия при изменении профиля.</span><span class="sxs-lookup"><span data-stu-id="dad78-118">A message service entry point function allows message services to configure themselves or perform other actions when the profile is changed.</span></span> <span data-ttu-id="dad78-119">Точка входа службы сообщений поддержку функций можно изменения конфигурации, отображая свойств или с помощью массива значение свойства, переданной в метод [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="dad78-119">Message service entry point functions can support configuration changes by displaying a property sheet or through a property value array passed to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dad78-120">См. также</span><span class="sxs-lookup"><span data-stu-id="dad78-120">See also</span></span>



[<span data-ttu-id="dad78-121">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dad78-121">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="dad78-122">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="dad78-122">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="dad78-123">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="dad78-123">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="dad78-124">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dad78-124">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)
  
[<span data-ttu-id="dad78-125">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="dad78-125">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="dad78-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dad78-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

