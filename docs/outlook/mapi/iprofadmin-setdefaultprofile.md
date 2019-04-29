---
title: Ипрофадминсетдефаултпрофиле
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.SetDefaultProfile
api_type:
- COM
ms.assetid: 58f50535-b0ed-4097-bda8-fd3ccc2d4b49
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 44be43864d943257520f27297e5754a4978c568d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439627"
---
# <a name="iprofadminsetdefaultprofile"></a><span data-ttu-id="fb2b6-103">IProfAdmin::SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb2b6-103">IProfAdmin::SetDefaultProfile</span></span>

  
  
<span data-ttu-id="fb2b6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb2b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb2b6-105">Задает или очищает профиль клиента, используемый по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-105">Sets or clears a client's default profile.</span></span>
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="fb2b6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb2b6-106">Parameters</span></span>

 <span data-ttu-id="fb2b6-107">_Лпсзпрофиленаме_</span><span class="sxs-lookup"><span data-stu-id="fb2b6-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="fb2b6-108">возврата Указатель на имя профиля, который будет служить значением по умолчанию, или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-108">[in] A pointer to the name of the profile that will become the default, or NULL.</span></span> <span data-ttu-id="fb2b6-109">Если для параметра _Лпсзпрофиленаме_ ЗАДАНО значение null, то **SetDefaultProfile** должен удалить существующий профиль по умолчанию, оставив клиент без значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-109">Setting  _lpszProfileName_ to NULL indicates that **SetDefaultProfile** should remove the existing default profile, leaving the client without a default.</span></span> 
    
 <span data-ttu-id="fb2b6-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fb2b6-110">_ulFlags_</span></span>
  
> <span data-ttu-id="fb2b6-111">возврата Битовая маска флагов, определяющая тип строки, на которую указывает _лпсзпрофиленаме_.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-111">[in] A bitmask of flags that controls the type of the string pointed to by  _lpszProfileName_.</span></span> <span data-ttu-id="fb2b6-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="fb2b6-112">The following flag can be set:</span></span>
    
<span data-ttu-id="fb2b6-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fb2b6-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fb2b6-114">Имя профиля имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-114">The profile name is in Unicode format.</span></span> <span data-ttu-id="fb2b6-115">Если флаг МАПИ_УНИКОДЕ не установлен, имя профиля будет иметь формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-115">If the MAPI_UNICODE flag is not set, the profile name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fb2b6-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb2b6-116">Return value</span></span>

<span data-ttu-id="fb2b6-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="fb2b6-117">S_OK</span></span> 
  
> <span data-ttu-id="fb2b6-118">Профиль по умолчанию успешно установлен или удален.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-118">A default profile was successfully established or removed.</span></span>
    
<span data-ttu-id="fb2b6-119">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="fb2b6-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="fb2b6-120">Указанный профиль не существует.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-120">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fb2b6-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="fb2b6-121">Remarks</span></span>

<span data-ttu-id="fb2b6-122">Метод **ипрофадмин:: SetDefaultProfile** устанавливает определенный профиль в качестве профиля клиента по умолчанию или очищает текущий профиль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-122">The **IProfAdmin::SetDefaultProfile** method either establishes a particular profile as the client's default profile or clears the current default profile.</span></span> <span data-ttu-id="fb2b6-123">Профиль по умолчанию — это профиль, который автоматически используется всякий раз, когда клиент начинает сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-123">The default profile is the profile that is automatically used whenever the client begins a MAPI session.</span></span> <span data-ttu-id="fb2b6-124">**SetDefaultProfile** также задает для нового свойства **пр_дефаулт_профиле** профиля по умолчанию ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) значение true.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-124">**SetDefaultProfile** also sets the new default profile's **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property to TRUE.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="fb2b6-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="fb2b6-125">Notes to callers</span></span>

<span data-ttu-id="fb2b6-126">Чтобы запустить сеанс с профилем по умолчанию, передайте в функцию [мапилогонекс](mapilogonex.md) флаг мапи_усе_дефаулт.</span><span class="sxs-lookup"><span data-stu-id="fb2b6-126">To start a session with the default profile, pass the MAPI_USE_DEFAULT flag to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fb2b6-127">См. также</span><span class="sxs-lookup"><span data-stu-id="fb2b6-127">See also</span></span>



[<span data-ttu-id="fb2b6-128">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="fb2b6-128">IProfAdmin::GetProfileTable</span></span>](iprofadmin-getprofiletable.md)
  
[<span data-ttu-id="fb2b6-129">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="fb2b6-129">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="fb2b6-130">Каноническое свойство PidTagDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb2b6-130">PidTagDefaultProfile Canonical Property</span></span>](pidtagdefaultprofile-canonical-property.md)
  
[<span data-ttu-id="fb2b6-131">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fb2b6-131">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

