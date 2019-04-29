---
title: Ипрофадминжетластеррор
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b6964ecde3a78bd1e9ce0ae1dcab0342c5a21a03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430775"
---
# <a name="iprofadmingetlasterror"></a><span data-ttu-id="5470c-103">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="5470c-103">IProfAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="5470c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5470c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5470c-105">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке, возникшей в объекте администрирования профиля.</span><span class="sxs-lookup"><span data-stu-id="5470c-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="5470c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5470c-106">Parameters</span></span>

 <span data-ttu-id="5470c-107">_Состав_</span><span class="sxs-lookup"><span data-stu-id="5470c-107">_hResult_</span></span>
  
> <span data-ttu-id="5470c-108">возврата Тип данных HRESULT, который содержит значение ошибки, возникшей при предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="5470c-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="5470c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5470c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5470c-110">возврата Битовая маска флагов, определяющих тип возвращаемых строк.</span><span class="sxs-lookup"><span data-stu-id="5470c-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="5470c-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="5470c-111">The following flag can be set:</span></span>
    
<span data-ttu-id="5470c-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5470c-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5470c-113">Строки в структуре [мапиеррор](mapierror.md) , возвращаемые в параметре _лппмапиеррор_ , представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="5470c-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="5470c-114">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="5470c-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="5470c-115">_Лппмапиеррор_</span><span class="sxs-lookup"><span data-stu-id="5470c-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="5470c-116">вышли Указатель на указатель на структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки.</span><span class="sxs-lookup"><span data-stu-id="5470c-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="5470c-117">Параметр _лппмапиеррор_ может иметь значение null, если структура **мапиеррор** для возврата отсутствует.</span><span class="sxs-lookup"><span data-stu-id="5470c-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5470c-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5470c-118">Return value</span></span>

<span data-ttu-id="5470c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="5470c-119">S_OK</span></span> 
  
> <span data-ttu-id="5470c-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="5470c-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="5470c-121">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="5470c-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="5470c-122">Установлен либо флаг МАПИ_УНИКОДЕ, либо реализация не поддерживает Юникод, или МАПИ_УНИКОДЕ не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="5470c-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5470c-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="5470c-123">Remarks</span></span>

<span data-ttu-id="5470c-124">Метод **ипрофадмин:: GetLastError** получает сведения о последней ошибке, возвращенной при вызове метода для объекта администрирования профиля.</span><span class="sxs-lookup"><span data-stu-id="5470c-124">The **IProfAdmin::GetLastError** method retrieves information about the last error returned from a method call for the profile administration object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5470c-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="5470c-125">Notes to callers</span></span>

<span data-ttu-id="5470c-126">Структуру **мапиеррор** можно использовать, если она предоставляет MAPI, на которую указывает параметр _лппмапиеррор_ , только если **GetLastError** возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="5470c-126">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="5470c-127">Иногда MAPI не может определить, какая ошибка прошла или больше не может сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5470c-127">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="5470c-128">В этом случае указатель на NULL возвращается в _лппмапиеррор_.</span><span class="sxs-lookup"><span data-stu-id="5470c-128">In this situation, a pointer to NULL is returned in  _lppMAPIError_.</span></span> 
  
<span data-ttu-id="5470c-129">Чтобы освободить всю память, выделенную MAPI для структуры **мапиеррор** , вызовите функцию [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="5470c-129">To release all the memory allocated by MAPI for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="5470c-130">Более подробную информацию о методе **GetLastError** можно узнать [в статье Использование расширенных ошибок](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="5470c-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5470c-131">См. также</span><span class="sxs-lookup"><span data-stu-id="5470c-131">See also</span></span>



[<span data-ttu-id="5470c-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="5470c-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="5470c-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5470c-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="5470c-134">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5470c-134">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

