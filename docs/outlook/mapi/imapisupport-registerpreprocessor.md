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
ms.openlocfilehash: 58215de6cc4e9e68386f8f017839752acc6e1753
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404899"
---
# <a name="imapisupportregisterpreprocessor"></a><span data-ttu-id="791e6-103">IMAPISupport::RegisterPreprocessor</span><span class="sxs-lookup"><span data-stu-id="791e6-103">IMAPISupport::RegisterPreprocessor</span></span>

  
  
<span data-ttu-id="791e6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="791e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="791e6-105">Регистрирует функцию препроцессора транспортного поставщика (функцию, которая соответствует прототипу [PreprocessMessage).](preprocessmessage.md)</span><span class="sxs-lookup"><span data-stu-id="791e6-105">Registers a transport provider's preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="791e6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="791e6-106">Parameters</span></span>

 <span data-ttu-id="791e6-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="791e6-107">_lpMuid_</span></span>
  
> <span data-ttu-id="791e6-108">[in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит идентификатор, который обрабатывает функцию препроцессора.</span><span class="sxs-lookup"><span data-stu-id="791e6-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the identifier that the preprocessor function handles.</span></span> <span data-ttu-id="791e6-109">Параметр  _lpMuid_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="791e6-109">The  _lpMuid_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="791e6-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="791e6-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="791e6-111">[in] Указатель на тип адреса для сообщений, на которые выполняется функция, таких как ФАКС, SMTP или X500.</span><span class="sxs-lookup"><span data-stu-id="791e6-111">[in] A pointer to the address type for the messages the function operates on, such as FAX, SMTP, or X500.</span></span> <span data-ttu-id="791e6-112">Параметр  _lpszAdrType_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="791e6-112">The  _lpszAdrType_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="791e6-113">_lpszDLLName_</span><span class="sxs-lookup"><span data-stu-id="791e6-113">_lpszDLLName_</span></span>
  
> <span data-ttu-id="791e6-114">[in] Указатель на имя библиотеки динамических ссылок (DLL), которая содержит точку входа для функции препроцессора.</span><span class="sxs-lookup"><span data-stu-id="791e6-114">[in] A pointer to the name of the dynamic-link library (DLL) that contains the entry point for the preprocessor function.</span></span>
    
 <span data-ttu-id="791e6-115">_lpszPreprocess_</span><span class="sxs-lookup"><span data-stu-id="791e6-115">_lpszPreprocess_</span></span>
  
> <span data-ttu-id="791e6-116">[in] Указатель на имя функции preprocessor.</span><span class="sxs-lookup"><span data-stu-id="791e6-116">[in] A pointer to the name of the preprocessor function.</span></span> <span data-ttu-id="791e6-117">Параметр  _lpszPreprocess может_ быть NULL.</span><span class="sxs-lookup"><span data-stu-id="791e6-117">The  _lpszPreprocess_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="791e6-118">_lpszRemovePreprocessInfo_</span><span class="sxs-lookup"><span data-stu-id="791e6-118">_lpszRemovePreprocessInfo_</span></span>
  
> <span data-ttu-id="791e6-119">[in] Указатель на имя функции, удаляемой предпроцессорной информации (функции, соответствующей прототипу [RemovePreprocessInfo).](removepreprocessinfo.md)</span><span class="sxs-lookup"><span data-stu-id="791e6-119">[in] A pointer to the name of the function that removes preprocessor information (a function that conforms to the [RemovePreprocessInfo](removepreprocessinfo.md) prototype).</span></span> <span data-ttu-id="791e6-120">Параметр  _lpszRemovePreprocessInfo_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="791e6-120">The  _lpszRemovePreprocessInfo_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="791e6-121">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="791e6-121">_ulFlags_</span></span>
  
> <span data-ttu-id="791e6-122">Зарезервировано; должно быть нулевой.</span><span class="sxs-lookup"><span data-stu-id="791e6-122">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="791e6-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="791e6-123">Return value</span></span>

<span data-ttu-id="791e6-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="791e6-124">S_OK</span></span> 
  
> <span data-ttu-id="791e6-125">Функция preprocessor успешно зарегистрирована.</span><span class="sxs-lookup"><span data-stu-id="791e6-125">The preprocessor function was successfully registered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="791e6-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="791e6-126">Remarks</span></span>

<span data-ttu-id="791e6-127">Метод **IMAPISupport::RegisterPreprocessor** реализован только для объектов поддержки поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="791e6-127">The **IMAPISupport::RegisterPreprocessor** method is implemented for transport provider support objects only.</span></span> <span data-ttu-id="791e6-128">Поставщики транспорта звонят **в RegisterPreprocessor** для регистрации функции препроцессора (функции, соответствующей прототипу [PreprocessMessage).](preprocessmessage.md)</span><span class="sxs-lookup"><span data-stu-id="791e6-128">Transport providers call **RegisterPreprocessor** to register a preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> <span data-ttu-id="791e6-129">Перед вызовом пулера MAPI необходимо зарегистрировать функцию препроцессора.</span><span class="sxs-lookup"><span data-stu-id="791e6-129">A preprocessor function must be registered before the MAPI spooler can call it.</span></span> 
  
<span data-ttu-id="791e6-130">Параметры  _lpszPreprocess,_  _lpszRemovePreprocessInfo_ и  _lpszDLLName_ должны указать на строки, которые можно использовать в сочетании с вызовами к функции **Win32 GetProcAddress,** что позволяет правильно называть точку входа в DLL препроцессора.</span><span class="sxs-lookup"><span data-stu-id="791e6-130">The  _lpszPreprocess_,  _lpszRemovePreprocessInfo_, and  _lpszDLLName_ parameters should all point to strings that can be used in conjunction with calls to the Win32 **GetProcAddress** function, allowing the preprocessor's DLL entry point to be called correctly.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="791e6-131">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="791e6-131">Notes to callers</span></span>

<span data-ttu-id="791e6-132">Вызовы к препроцессорам специфическ к заказу поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="791e6-132">Calls to preprocessors are specific to transport provider order.</span></span> <span data-ttu-id="791e6-133">Это означает, что если другой поставщик транспорта, опережая поставщика, сможет обрабатывать сообщение, функция препроцессора не будет вызвана для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="791e6-133">This means that if another transport provider ahead of your provider is able to handle a message, your preprocessor function will not be called for that message.</span></span> <span data-ttu-id="791e6-134">Функция препроцессора будет вызвана только для сообщений, которые будут обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="791e6-134">Your preprocessor function will be called only for messages that you will handle.</span></span>
  
<span data-ttu-id="791e6-135">Можно написать функции препроцессора для обработки определенного идентификатора, хранимого в структуре [MAPIUID,](mapiuid.md) или типа адреса.</span><span class="sxs-lookup"><span data-stu-id="791e6-135">You can write preprocessor functions to handle either a specific identifier stored in a [MAPIUID](mapiuid.md) structure or a type of address.</span></span> <span data-ttu-id="791e6-136">Если в параметре _lpMuid_ указана как структура **MAPIUID,** так и тип адреса в параметре _lpszAdrType,_ ваша функция будет вызвана для получателей сообщений, которые соответствуют **типу MAPIUID** или типу адреса.</span><span class="sxs-lookup"><span data-stu-id="791e6-136">If you specify both a **MAPIUID** structure in the  _lpMuid_ parameter and an address type in the  _lpszAdrType_ parameter, your function will be called for message recipients that match either the **MAPIUID** or the address type.</span></span> <span data-ttu-id="791e6-137">Если _lpMuid_ является NULL, а _lpszAdrType_ — не NULL, ваша функция будет вызвана только для получателей с адресом, который соответствует типу, на который указывает _lpszAdrType._</span><span class="sxs-lookup"><span data-stu-id="791e6-137">If  _lpMuid_ is NULL and  _lpszAdrType_ is non-NULL, your function will be called only for recipients that have an address that matches the type pointed to by  _lpszAdrType_.</span></span> <span data-ttu-id="791e6-138">Если  _lpMuid_ не является NULL и  _lpszAdrType_ является NULL, ваша функция будет вызвана для получателей, которые соответствуют **MAPIUID,** независимо от их типа адреса.</span><span class="sxs-lookup"><span data-stu-id="791e6-138">If  _lpMuid_ is non-NULL and  _lpszAdrType_ is NULL, your function will be called for recipients that match **MAPIUID**, regardless of their address type.</span></span> <span data-ttu-id="791e6-139">Если оба являются NULL, ваша функция вызвана для всех получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="791e6-139">If both are NULL, your function is called for all recipients of the message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="791e6-140">См. также</span><span class="sxs-lookup"><span data-stu-id="791e6-140">See also</span></span>



[<span data-ttu-id="791e6-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="791e6-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="791e6-142">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="791e6-142">PreprocessMessage</span></span>](preprocessmessage.md)
  
[<span data-ttu-id="791e6-143">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="791e6-143">RemovePreprocessInfo</span></span>](removepreprocessinfo.md)
  
[<span data-ttu-id="791e6-144">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="791e6-144">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

