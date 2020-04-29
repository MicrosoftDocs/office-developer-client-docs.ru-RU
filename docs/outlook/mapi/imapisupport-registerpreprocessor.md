---
title: имаписуппортрегистерпрепроцессор
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
# <a name="imapisupportregisterpreprocessor"></a><span data-ttu-id="26a9b-103">IMAPISupport::RegisterPreprocessor</span><span class="sxs-lookup"><span data-stu-id="26a9b-103">IMAPISupport::RegisterPreprocessor</span></span>

  
  
<span data-ttu-id="26a9b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26a9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26a9b-105">Регистрирует функцию препроцессора поставщика транспорта (функцию, которая соответствует прототипу [препроцессмессаже](preprocessmessage.md) ).</span><span class="sxs-lookup"><span data-stu-id="26a9b-105">Registers a transport provider's preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="26a9b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="26a9b-106">Parameters</span></span>

 <span data-ttu-id="26a9b-107">_лпмуид_</span><span class="sxs-lookup"><span data-stu-id="26a9b-107">_lpMuid_</span></span>
  
> <span data-ttu-id="26a9b-108">возврата Указатель на структуру [мапиуид](mapiuid.md) , которая содержит идентификатор, который обрабатывает функция препроцессора.</span><span class="sxs-lookup"><span data-stu-id="26a9b-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the identifier that the preprocessor function handles.</span></span> <span data-ttu-id="26a9b-109">Параметр _лпмуид_ может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="26a9b-109">The  _lpMuid_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="26a9b-110">_лпсзадртипе_</span><span class="sxs-lookup"><span data-stu-id="26a9b-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="26a9b-111">возврата Указатель на тип адреса для сообщений, с которыми работает функция, например FAX, SMTP или X500.</span><span class="sxs-lookup"><span data-stu-id="26a9b-111">[in] A pointer to the address type for the messages the function operates on, such as FAX, SMTP, or X500.</span></span> <span data-ttu-id="26a9b-112">Параметр _лпсзадртипе_ может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="26a9b-112">The  _lpszAdrType_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="26a9b-113">_лпсздллнаме_</span><span class="sxs-lookup"><span data-stu-id="26a9b-113">_lpszDLLName_</span></span>
  
> <span data-ttu-id="26a9b-114">возврата Указатель на имя библиотеки динамической компоновки (DLL), которая содержит точку входа для функции предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="26a9b-114">[in] A pointer to the name of the dynamic-link library (DLL) that contains the entry point for the preprocessor function.</span></span>
    
 <span data-ttu-id="26a9b-115">_лпсзпрепроцесс_</span><span class="sxs-lookup"><span data-stu-id="26a9b-115">_lpszPreprocess_</span></span>
  
> <span data-ttu-id="26a9b-116">возврата Указатель на имя функции препроцессора.</span><span class="sxs-lookup"><span data-stu-id="26a9b-116">[in] A pointer to the name of the preprocessor function.</span></span> <span data-ttu-id="26a9b-117">Параметр _лпсзпрепроцесс_ может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="26a9b-117">The  _lpszPreprocess_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="26a9b-118">_лпсзремовепрепроцессинфо_</span><span class="sxs-lookup"><span data-stu-id="26a9b-118">_lpszRemovePreprocessInfo_</span></span>
  
> <span data-ttu-id="26a9b-119">возврата Указатель на имя функции, которая удаляет сведения о препроцессоре (функция, которая соответствует прототипу [ремовепрепроцессинфо](removepreprocessinfo.md) ).</span><span class="sxs-lookup"><span data-stu-id="26a9b-119">[in] A pointer to the name of the function that removes preprocessor information (a function that conforms to the [RemovePreprocessInfo](removepreprocessinfo.md) prototype).</span></span> <span data-ttu-id="26a9b-120">Параметр _лпсзремовепрепроцессинфо_ может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="26a9b-120">The  _lpszRemovePreprocessInfo_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="26a9b-121">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="26a9b-121">_ulFlags_</span></span>
  
> <span data-ttu-id="26a9b-122">Резервирования должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="26a9b-122">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="26a9b-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26a9b-123">Return value</span></span>

<span data-ttu-id="26a9b-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="26a9b-124">S_OK</span></span> 
  
> <span data-ttu-id="26a9b-125">Функция предварительной обработки была успешно зарегистрирована.</span><span class="sxs-lookup"><span data-stu-id="26a9b-125">The preprocessor function was successfully registered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="26a9b-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="26a9b-126">Remarks</span></span>

<span data-ttu-id="26a9b-127">Метод **имаписуппорт:: регистерпрепроцессор** реализован только для объектов поддержки транспортного поставщика.</span><span class="sxs-lookup"><span data-stu-id="26a9b-127">The **IMAPISupport::RegisterPreprocessor** method is implemented for transport provider support objects only.</span></span> <span data-ttu-id="26a9b-128">Поставщики транспорта вызывают **регистерпрепроцессор** для регистрации функции препроцессора (функции, которая соответствует прототипу [препроцессмессаже](preprocessmessage.md) ).</span><span class="sxs-lookup"><span data-stu-id="26a9b-128">Transport providers call **RegisterPreprocessor** to register a preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> <span data-ttu-id="26a9b-129">Функция предварительной обработки должна быть зарегистрирована, прежде чем диспетчер очереди MAPI сможет ее вызвать.</span><span class="sxs-lookup"><span data-stu-id="26a9b-129">A preprocessor function must be registered before the MAPI spooler can call it.</span></span> 
  
<span data-ttu-id="26a9b-130">Параметры _лпсзпрепроцесс_, _лпсзремовепрепроцессинфо_и _лпсздллнаме_ должны указывать на строки, которые можно использовать в сочетании с вызовами функции Win32 **GetProcAddress** , что позволяет правильно вызывать точку входа DLL препроцессора.</span><span class="sxs-lookup"><span data-stu-id="26a9b-130">The  _lpszPreprocess_,  _lpszRemovePreprocessInfo_, and  _lpszDLLName_ parameters should all point to strings that can be used in conjunction with calls to the Win32 **GetProcAddress** function, allowing the preprocessor's DLL entry point to be called correctly.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="26a9b-131">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="26a9b-131">Notes to callers</span></span>

<span data-ttu-id="26a9b-132">Вызовы предварительных процессоров относятся к порядку поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="26a9b-132">Calls to preprocessors are specific to transport provider order.</span></span> <span data-ttu-id="26a9b-133">Это означает, что если поставщик транспорта готов к обработке сообщения, функция препроцессора не будет вызываться для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="26a9b-133">This means that if another transport provider ahead of your provider is able to handle a message, your preprocessor function will not be called for that message.</span></span> <span data-ttu-id="26a9b-134">Функция препроцессора будет вызываться только для тех сообщений, которые будут обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="26a9b-134">Your preprocessor function will be called only for messages that you will handle.</span></span>
  
<span data-ttu-id="26a9b-135">Вы можете написать функции препроцессора для обработки определенного идентификатора, хранящегося в структуре [мапиуид](mapiuid.md) , или типе адреса.</span><span class="sxs-lookup"><span data-stu-id="26a9b-135">You can write preprocessor functions to handle either a specific identifier stored in a [MAPIUID](mapiuid.md) structure or a type of address.</span></span> <span data-ttu-id="26a9b-136">Если указать и структуру **мапиуид** в параметре _лпмуид_ , и тип адреса в параметре _лпсзадртипе_ , то функция будет вызываться для получателей сообщений, которые совпадают с **мапиуид** или типом адреса.</span><span class="sxs-lookup"><span data-stu-id="26a9b-136">If you specify both a **MAPIUID** structure in the  _lpMuid_ parameter and an address type in the  _lpszAdrType_ parameter, your function will be called for message recipients that match either the **MAPIUID** or the address type.</span></span> <span data-ttu-id="26a9b-137">Если _лпмуид_ имеет значение null, а _лпсзадртипе_ имеет значение, отличное от NULL, то функция будет вызываться только для тех получателей, адрес которых соответствует типу, на который указывает _лпсзадртипе_.</span><span class="sxs-lookup"><span data-stu-id="26a9b-137">If  _lpMuid_ is NULL and  _lpszAdrType_ is non-NULL, your function will be called only for recipients that have an address that matches the type pointed to by  _lpszAdrType_.</span></span> <span data-ttu-id="26a9b-138">Если _лпмуид_ не имеет значение NULL и _лпсзадртипе_ имеет значение null, функция будет вызываться для получателей, которые совпадают с **мапиуид**, независимо от их типа адреса.</span><span class="sxs-lookup"><span data-stu-id="26a9b-138">If  _lpMuid_ is non-NULL and  _lpszAdrType_ is NULL, your function will be called for recipients that match **MAPIUID**, regardless of their address type.</span></span> <span data-ttu-id="26a9b-139">Если оба значения равны NULL, функция вызывается для всех получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="26a9b-139">If both are NULL, your function is called for all recipients of the message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="26a9b-140">См. также</span><span class="sxs-lookup"><span data-stu-id="26a9b-140">See also</span></span>



[<span data-ttu-id="26a9b-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="26a9b-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="26a9b-142">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="26a9b-142">PreprocessMessage</span></span>](preprocessmessage.md)
  
[<span data-ttu-id="26a9b-143">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="26a9b-143">RemovePreprocessInfo</span></span>](removepreprocessinfo.md)
  
[<span data-ttu-id="26a9b-144">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="26a9b-144">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

