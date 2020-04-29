---
title: имаписуппортжетсвкконфигсуппортобж
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
ms.openlocfilehash: 6de0fed4df9d23e67c3520ffb019a961b890f988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411311"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a><span data-ttu-id="66859-103">IMAPISupport::GetSvcConfigSupportObj</span><span class="sxs-lookup"><span data-stu-id="66859-103">IMAPISupport::GetSvcConfigSupportObj</span></span>

  
  
<span data-ttu-id="66859-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66859-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66859-105">Создает объект поддержки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="66859-105">Creates a message service support object.</span></span>
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a><span data-ttu-id="66859-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="66859-106">Parameters</span></span>

 <span data-ttu-id="66859-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="66859-107">_ulFlags_</span></span>
  
> <span data-ttu-id="66859-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="66859-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="66859-109">_лппсвксуппорт_</span><span class="sxs-lookup"><span data-stu-id="66859-109">_lppSvcSupport_</span></span>
  
> <span data-ttu-id="66859-110">вышли Указатель на указатель на новый объект поддержки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="66859-110">[out] A pointer to a pointer to the new message service support object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="66859-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66859-111">Return value</span></span>

<span data-ttu-id="66859-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="66859-112">S_OK</span></span> 
  
> <span data-ttu-id="66859-113">Объект поддержки конфигурации успешно создан.</span><span class="sxs-lookup"><span data-stu-id="66859-113">The configuration support object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="66859-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="66859-114">Remarks</span></span>

<span data-ttu-id="66859-115">Метод **имаписуппорт:: жетсвкконфигсуппортобж** реализован для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="66859-115">The **IMAPISupport::GetSvcConfigSupportObj** method is implemented for all support objects.</span></span> <span data-ttu-id="66859-116">Поставщики услуг вызывают **жетсвкконфигсуппортобж** , чтобы создать объект поддержки конфигурации для передачи в функцию точки входа службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="66859-116">Service providers call **GetSvcConfigSupportObj** to create a configuration support object to pass to a message service entry point function.</span></span> 
  
<span data-ttu-id="66859-117">Функция точки входа службы сообщений основана на прототипе [мсгсервицеентри](msgserviceentry.md) и вызывается методами интерфейса [имсгсервицеадмин](imsgserviceadminiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="66859-117">A message service entry point function is based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype and is called by methods of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) interface.</span></span> <span data-ttu-id="66859-118">Функция точки входа службы сообщений позволяет службам сообщений настраивать себя или выполнять другие действия при изменении профиля.</span><span class="sxs-lookup"><span data-stu-id="66859-118">A message service entry point function allows message services to configure themselves or perform other actions when the profile is changed.</span></span> <span data-ttu-id="66859-119">Функции точки входа службы сообщений могут поддерживать изменения конфигурации, отображая страницу свойств или массив значений свойства, переданный методу [имсгсервицеадмин:: конфигуремсгсервице](imsgserviceadmin-configuremsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="66859-119">Message service entry point functions can support configuration changes by displaying a property sheet or through a property value array passed to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="66859-120">См. также</span><span class="sxs-lookup"><span data-stu-id="66859-120">See also</span></span>



[<span data-ttu-id="66859-121">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="66859-121">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="66859-122">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="66859-122">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="66859-123">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="66859-123">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="66859-124">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="66859-124">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)
  
[<span data-ttu-id="66859-125">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="66859-125">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="66859-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="66859-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

