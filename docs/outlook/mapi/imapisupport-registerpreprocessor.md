---
title: IMAPISupportRegisterPreprocessor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.RegisterPreprocessor
api_type:
- COM
ms.assetid: 9b5659ab-2b49-41ab-92ce-ca343e35d670
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 87f5e3f159542359f614a6ab698e6f06a2faf41a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567918"
---
# <a name="imapisupportregisterpreprocessor"></a><span data-ttu-id="12714-103">IMAPISupport::RegisterPreprocessor</span><span class="sxs-lookup"><span data-stu-id="12714-103">IMAPISupport::RegisterPreprocessor</span></span>

  
  
<span data-ttu-id="12714-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12714-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12714-105">Регистрация поставщика транспорта препроцессору функция (функция, которая соответствует прототип [PreprocessMessage](preprocessmessage.md) ).</span><span class="sxs-lookup"><span data-stu-id="12714-105">Registers a transport provider's preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> 
  
```cpp
HRESULT RegisterPreprocessor(
LPMAPIUID lpMuid,
LPSTR lpszAdrType,
LPSTR lpszDLLName,
LPSTR lpszPreprocess,
LPSTR lpszRemovePreprocessInfo,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="12714-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="12714-106">Parameters</span></span>

 <span data-ttu-id="12714-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="12714-107">_lpMuid_</span></span>
  
> <span data-ttu-id="12714-108">[in] Указатель на структуру [MAPIUID](mapiuid.md) , содержащую идентификатор, который обрабатывает препроцессору функции.</span><span class="sxs-lookup"><span data-stu-id="12714-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the identifier that the preprocessor function handles.</span></span> <span data-ttu-id="12714-109">Параметр _lpMuid_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="12714-109">The  _lpMuid_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="12714-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="12714-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="12714-111">[in] Указатель на тип адреса для сообщений, функция применяется, например, ФАКС, SMTP или X500.</span><span class="sxs-lookup"><span data-stu-id="12714-111">[in] A pointer to the address type for the messages the function operates on, such as FAX, SMTP, or X500.</span></span> <span data-ttu-id="12714-112">Параметр _lpszAdrType_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="12714-112">The  _lpszAdrType_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="12714-113">_lpszDLLName_</span><span class="sxs-lookup"><span data-stu-id="12714-113">_lpszDLLName_</span></span>
  
> <span data-ttu-id="12714-114">[in] Указатель на имя библиотеки динамической компоновки (DLL), которая содержит точка входа для функции предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="12714-114">[in] A pointer to the name of the dynamic-link library (DLL) that contains the entry point for the preprocessor function.</span></span>
    
 <span data-ttu-id="12714-115">_lpszPreprocess_</span><span class="sxs-lookup"><span data-stu-id="12714-115">_lpszPreprocess_</span></span>
  
> <span data-ttu-id="12714-116">[in] Указатель на имя функции предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="12714-116">[in] A pointer to the name of the preprocessor function.</span></span> <span data-ttu-id="12714-117">Параметр _lpszPreprocess_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="12714-117">The  _lpszPreprocess_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="12714-118">_lpszRemovePreprocessInfo_</span><span class="sxs-lookup"><span data-stu-id="12714-118">_lpszRemovePreprocessInfo_</span></span>
  
> <span data-ttu-id="12714-119">[in] Указатель на имя функции, удаляющий препроцессору данные (функция, которая соответствует прототип [RemovePreprocessInfo](removepreprocessinfo.md) ).</span><span class="sxs-lookup"><span data-stu-id="12714-119">[in] A pointer to the name of the function that removes preprocessor information (a function that conforms to the [RemovePreprocessInfo](removepreprocessinfo.md) prototype).</span></span> <span data-ttu-id="12714-120">Параметр _lpszRemovePreprocessInfo_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="12714-120">The  _lpszRemovePreprocessInfo_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="12714-121">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="12714-121">_ulFlags_</span></span>
  
> <span data-ttu-id="12714-122">Зарезервировано; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="12714-122">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="12714-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12714-123">Return value</span></span>

<span data-ttu-id="12714-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="12714-124">S_OK</span></span> 
  
> <span data-ttu-id="12714-125">Функция препроцессору успешно зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="12714-125">The preprocessor function was successfully registered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="12714-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="12714-126">Remarks</span></span>

<span data-ttu-id="12714-127">Метод **IMAPISupport::RegisterPreprocessor** реализуется для поддержки объектов на транспортном поставщика.</span><span class="sxs-lookup"><span data-stu-id="12714-127">The **IMAPISupport::RegisterPreprocessor** method is implemented for transport provider support objects only.</span></span> <span data-ttu-id="12714-128">Поставщики транспорта вызов **RegisterPreprocessor** для регистрации препроцессору функции (функция, которая соответствует прототип [PreprocessMessage](preprocessmessage.md) ).</span><span class="sxs-lookup"><span data-stu-id="12714-128">Transport providers call **RegisterPreprocessor** to register a preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> <span data-ttu-id="12714-129">Диспетчер очереди MAPI можно вызвать препроцессору функция должна быть зарегистрирована.</span><span class="sxs-lookup"><span data-stu-id="12714-129">A preprocessor function must be registered before the MAPI spooler can call it.</span></span> 
  
<span data-ttu-id="12714-130">Параметры _lpszPreprocess_, _lpszRemovePreprocessInfo_и _lpszDLLName_ должен указывать на строк, которые можно использовать в сочетании с вызова функции Win32 **GetProcAddress** , позволяя препроцессор DLL точка входа для вызова правильно.</span><span class="sxs-lookup"><span data-stu-id="12714-130">The  _lpszPreprocess_,  _lpszRemovePreprocessInfo_, and  _lpszDLLName_ parameters should all point to strings that can be used in conjunction with calls to the Win32 **GetProcAddress** function, allowing the preprocessor's DLL entry point to be called correctly.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="12714-131">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="12714-131">Notes to callers</span></span>

<span data-ttu-id="12714-132">Вызовы preprocessors относятся только к порядке поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="12714-132">Calls to preprocessors are specific to transport provider order.</span></span> <span data-ttu-id="12714-133">Это означает, что если обрабатывать сообщения другого поставщика транспорта раньше, чем у поставщика, препроцессору функции не вызываются для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="12714-133">This means that if another transport provider ahead of your provider is able to handle a message, your preprocessor function will not be called for that message.</span></span> <span data-ttu-id="12714-134">Препроцессору функция будет вызываться только для сообщений, которые будет обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="12714-134">Your preprocessor function will be called only for messages that you will handle.</span></span>
  
<span data-ttu-id="12714-135">Вы можете использовать препроцессору функции для обработки любого из конкретного идентификатора, хранящиеся в структуре [MAPIUID](mapiuid.md) или тип адреса.</span><span class="sxs-lookup"><span data-stu-id="12714-135">You can write preprocessor functions to handle either a specific identifier stored in a [MAPIUID](mapiuid.md) structure or a type of address.</span></span> <span data-ttu-id="12714-136">При указании структуру **MAPIUID** в параметр _lpMuid_ и тип адреса с помощью параметра _lpszAdrType_ , функция будет вызываться для получателей сообщения, которые соответствуют **MAPIUID** или тип адреса.</span><span class="sxs-lookup"><span data-stu-id="12714-136">If you specify both a **MAPIUID** structure in the  _lpMuid_ parameter and an address type in the  _lpszAdrType_ parameter, your function will be called for message recipients that match either the **MAPIUID** or the address type.</span></span> <span data-ttu-id="12714-137">Если _lpMuid_ имеет значение NULL и _lpszAdrType_ не равно NULL, функция будет вызываться только для получателей, имеющих адрес, соответствующий тип, на который указывает _lpszAdrType_.</span><span class="sxs-lookup"><span data-stu-id="12714-137">If  _lpMuid_ is NULL and  _lpszAdrType_ is non-NULL, your function will be called only for recipients that have an address that matches the type pointed to by  _lpszAdrType_.</span></span> <span data-ttu-id="12714-138">Если _lpMuid_ не равно NULL и _lpszAdrType_ имеет значение NULL, функция будет вызываться для получателей, которые соответствуют **MAPIUID**, независимо от их типа адреса.</span><span class="sxs-lookup"><span data-stu-id="12714-138">If  _lpMuid_ is non-NULL and  _lpszAdrType_ is NULL, your function will be called for recipients that match **MAPIUID**, regardless of their address type.</span></span> <span data-ttu-id="12714-139">Если оба значения NULL, функция вызывается для всех получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="12714-139">If both are NULL, your function is called for all recipients of the message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="12714-140">См. также</span><span class="sxs-lookup"><span data-stu-id="12714-140">See also</span></span>



[<span data-ttu-id="12714-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="12714-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="12714-142">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="12714-142">PreprocessMessage</span></span>](preprocessmessage.md)
  
[<span data-ttu-id="12714-143">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="12714-143">RemovePreprocessInfo</span></span>](removepreprocessinfo.md)
  
[<span data-ttu-id="12714-144">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="12714-144">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

