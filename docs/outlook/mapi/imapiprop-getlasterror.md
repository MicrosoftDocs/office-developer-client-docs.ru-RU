---
title: Имапипропжетластеррор
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8c31cbf0472d3d64c7327fcfc80480ef27a1638e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435833"
---
# <a name="imapipropgetlasterror"></a><span data-ttu-id="4d821-103">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="4d821-103">IMAPIProp::GetLastError</span></span>

  
  
<span data-ttu-id="4d821-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d821-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d821-105">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущем сообщении об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4d821-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="4d821-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d821-106">Parameters</span></span>

 <span data-ttu-id="4d821-107">_Состав_</span><span class="sxs-lookup"><span data-stu-id="4d821-107">_hResult_</span></span>
  
> <span data-ttu-id="4d821-108">возврата Дескриптор кода ошибки, созданного при предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="4d821-108">[in] A handle to the error code generated in the previous method call.</span></span>
    
 <span data-ttu-id="4d821-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4d821-109">_ulFlags_</span></span>
  
> <span data-ttu-id="4d821-110">возврата Битовая маска флагов, указывающая формат текста, возвращаемого в структуре **мапиеррор** , на которую указывает _лппмапиеррор_.</span><span class="sxs-lookup"><span data-stu-id="4d821-110">[in] A bitmask of flags that indicates the format for the text returned in the **MAPIERROR** structure pointed to by  _lppMAPIError_.</span></span> <span data-ttu-id="4d821-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="4d821-111">The following flag can be set:</span></span>
    
<span data-ttu-id="4d821-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4d821-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4d821-113">Строки должны быть в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="4d821-113">The strings should be in Unicode format.</span></span> <span data-ttu-id="4d821-114">Если флаг МАПИ_УНИКОДЕ не установлен, строки должны быть в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="4d821-114">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="4d821-115">_Лппмапиеррор_</span><span class="sxs-lookup"><span data-stu-id="4d821-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="4d821-116">вышли Указатель на указатель на структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки.</span><span class="sxs-lookup"><span data-stu-id="4d821-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="4d821-117">Параметр _лппмапиеррор_ может иметь значение null, если сведения об ошибке не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="4d821-117">The  _lppMAPIError_ parameter can be set to NULL if there is no error information to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4d821-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d821-118">Return value</span></span>

<span data-ttu-id="4d821-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="4d821-119">S_OK</span></span> 
  
> <span data-ttu-id="4d821-120">Возвращены сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4d821-120">The error information was returned.</span></span>
    
<span data-ttu-id="4d821-121">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="4d821-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="4d821-122">Установлен либо флаг МАПИ_УНИКОДЕ, либо реализация не поддерживает Юникод, или МАПИ_УНИКОДЕ не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="4d821-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4d821-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="4d821-123">Remarks</span></span>

<span data-ttu-id="4d821-124">Метод **IMAPIProp:: GetLastError** предоставляет сведения о предыдущем вызове метода, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="4d821-124">The **IMAPIProp::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="4d821-125">Клиенты могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры **мапиеррор** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="4d821-125">Clients can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
<span data-ttu-id="4d821-126">Все реализации **GetLastError** , ПРЕДОСТАВЛЯЕМые MAPI, являются реализациями ANSI, за исключением реализации [IAddrBook](iaddrbookimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="4d821-126">All of the implementations of **GetLastError** provided by MAPI are ANSI implementations, except for the [IAddrBook](iaddrbookimapiprop.md) implementation.</span></span> <span data-ttu-id="4d821-127">Метод **GetLastError** , включенный в **IAddrBook** , поддерживает Юникод.</span><span class="sxs-lookup"><span data-stu-id="4d821-127">The **GetLastError** method included with **IAddrBook** supports Unicode.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4d821-128">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="4d821-128">Notes to implementers</span></span>

<span data-ttu-id="4d821-129">Сведения о реализации этого метода для поставщика удаленного транспорта, а также о том, какие сообщения этот метод возвращает поставщику транспорта, так как определенные условия ошибок, ведущие к различным значениям HRESULT, будут отличаться для разных транспортных данных доступа.</span><span class="sxs-lookup"><span data-stu-id="4d821-129">The details of a remote transport provider's implementation of this method and what messages this method returns are up to the transport provider, because the particular error conditions that lead to various HRESULT values will be different for different transport providers.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="4d821-130">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="4d821-130">Notes to callers</span></span>

<span data-ttu-id="4d821-131">Можно использовать структуру **мапиеррор** , на которую указывает параметр _Лппмапиеррор_ , если **GetLastError** содержит один, только если возвращаемое значение равно S_OK.</span><span class="sxs-lookup"><span data-stu-id="4d821-131">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter, if **GetLastError** supplies one, only if the return value is S_OK.</span></span> <span data-ttu-id="4d821-132">Иногда **GetLastError** не может определить, что последняя ошибка или больше не содержит ничего больше, чтобы сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4d821-132">Sometimes **GetLastError** cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="4d821-133">В этом случае указатель на NULL возвращается в _лппмапиеррор_ .</span><span class="sxs-lookup"><span data-stu-id="4d821-133">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="4d821-134">Чтобы освободить память для структуры **мапиеррор** , вызовите функцию [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="4d821-134">To release the memory for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="4d821-135">Дополнительные сведения о методе **GetLastError** приведены в разделе [Расширенные ошибки MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="4d821-135">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4d821-136">См. также</span><span class="sxs-lookup"><span data-stu-id="4d821-136">See also</span></span>



[<span data-ttu-id="4d821-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4d821-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="4d821-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="4d821-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="4d821-139">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4d821-139">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4d821-140">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d821-140">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="4d821-141">Расширенные ошибки MAPI</span><span class="sxs-lookup"><span data-stu-id="4d821-141">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

