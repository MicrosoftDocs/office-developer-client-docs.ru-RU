---
title: имаписуппортжетластеррор
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c34c175c43ada03e982f08a27f675448ea24a567
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438549"
---
# <a name="imapisupportgetlasterror"></a><span data-ttu-id="e0f23-103">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e0f23-103">IMAPISupport::GetLastError</span></span>

  
  
<span data-ttu-id="e0f23-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0f23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0f23-105">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения об ошибке предыдущего объекта поддержки.</span><span class="sxs-lookup"><span data-stu-id="e0f23-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous support object error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="e0f23-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0f23-106">Parameters</span></span>

 <span data-ttu-id="e0f23-107">_Состав_</span><span class="sxs-lookup"><span data-stu-id="e0f23-107">_hResult_</span></span>
  
> <span data-ttu-id="e0f23-108">возврата Дескриптор значения ошибки, созданной в предыдущем вызове метода для объекта support.</span><span class="sxs-lookup"><span data-stu-id="e0f23-108">[in] A handle to the error value generated in the previous method call for the support object.</span></span>
    
 <span data-ttu-id="e0f23-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e0f23-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e0f23-110">возврата Битовая маска флагов, определяющих тип возвращаемых строк.</span><span class="sxs-lookup"><span data-stu-id="e0f23-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="e0f23-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="e0f23-111">The following flag can be set:</span></span>
    
<span data-ttu-id="e0f23-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e0f23-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e0f23-113">Строки в структуре **мапиеррор** , возвращаемые в параметре _лппмапиеррор_ , представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="e0f23-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="e0f23-114">Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="e0f23-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="e0f23-115">_лппмапиеррор_</span><span class="sxs-lookup"><span data-stu-id="e0f23-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="e0f23-116">вышли Указатель на указатель на структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки.</span><span class="sxs-lookup"><span data-stu-id="e0f23-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="e0f23-117">Параметр _лппмапиеррор_ может иметь значение null, если не удается предоставить структуру **мапиеррор** с соответствующими сведениями об ошибках.</span><span class="sxs-lookup"><span data-stu-id="e0f23-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate error information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e0f23-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0f23-118">Return value</span></span>

<span data-ttu-id="e0f23-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0f23-119">S_OK</span></span> 
  
> <span data-ttu-id="e0f23-120">Вызов выполнен успешно и вернул ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="e0f23-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="e0f23-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="e0f23-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="e0f23-122">Установлен флаг MAPI_UNICODE, а MAPI не поддерживает Юникод или MAPI_UNICODE не задан, а MAPI поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="e0f23-122">Either the MAPI_UNICODE flag was set and MAPI does not support Unicode, or MAPI_UNICODE was not set and MAPI supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e0f23-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="e0f23-123">Remarks</span></span>

<span data-ttu-id="e0f23-124">Метод **имаписуппорт:: GetLastError** реализован для всех объектов support.</span><span class="sxs-lookup"><span data-stu-id="e0f23-124">The **IMAPISupport::GetLastError** method is implemented for all support objects.</span></span> <span data-ttu-id="e0f23-125">Вызывающие абоненты могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры **мапиеррор** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="e0f23-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e0f23-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e0f23-126">Notes to callers</span></span>

<span data-ttu-id="e0f23-127">Можно использовать указатель на структуру **мапиеррор** , если MAPI предоставляет один из параметров _лппмапиеррор_ , только если **GetLastError** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="e0f23-127">You can use the pointer to the **MAPIERROR** structure, if MAPI supplies one, in the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="e0f23-128">Иногда MAPI не может определить, в чем последняя ошибка, или сообщение об ошибке больше не содержит ничего.</span><span class="sxs-lookup"><span data-stu-id="e0f23-128">Sometimes MAPI cannot determine what the last error was or it has nothing more to report about the error.</span></span> <span data-ttu-id="e0f23-129">В этом случае _лппмапиеррор_ возвращает указатель на null вместо него.</span><span class="sxs-lookup"><span data-stu-id="e0f23-129">In this situation,  _lppMAPIError_ returns a pointer to NULL instead.</span></span> 
  
<span data-ttu-id="e0f23-130">Дополнительные сведения о методе **GetLastError** приведены в разделе [Расширенные ошибки MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="e0f23-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
<span data-ttu-id="e0f23-131">Чтобы освободить всю память, выделенную MAPI, вызовите функцию [мапифрибуффер](mapifreebuffer.md) для возвращенной структуры **мапиеррор** .</span><span class="sxs-lookup"><span data-stu-id="e0f23-131">To release all the memory allocated by MAPI, call the [MAPIFreeBuffer](mapifreebuffer.md) function for the returned **MAPIERROR** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e0f23-132">См. также</span><span class="sxs-lookup"><span data-stu-id="e0f23-132">See also</span></span>



[<span data-ttu-id="e0f23-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="e0f23-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="e0f23-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e0f23-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e0f23-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0f23-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="e0f23-136">Расширенные ошибки MAPI</span><span class="sxs-lookup"><span data-stu-id="e0f23-136">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

