---
title: имслогонжетластеррор
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.GetLastError
api_type:
- COM
ms.assetid: 3e296f6d-4833-4c68-9b84-df0b09878474
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 472502d0f033370b06a69596944350152ab794f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425878"
---
# <a name="imslogongetlasterror"></a><span data-ttu-id="0aba9-103">IMSLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0aba9-103">IMSLogon::GetLastError</span></span>

  
  
<span data-ttu-id="0aba9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0aba9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0aba9-105">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о последней ошибке, произошедшей для объекта хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="0aba9-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="0aba9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0aba9-106">Parameters</span></span>

 <span data-ttu-id="0aba9-107">_Состав_</span><span class="sxs-lookup"><span data-stu-id="0aba9-107">_hResult_</span></span>
  
> <span data-ttu-id="0aba9-108">возврата Тип данных HRESULT, который содержит значение ошибки, созданное в предыдущем вызове метода для объекта хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="0aba9-108">[in] An HRESULT data type that contains the error value generated in the previous method call for the message store object.</span></span>
    
 <span data-ttu-id="0aba9-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0aba9-109">_ulFlags_</span></span>
  
> <span data-ttu-id="0aba9-110">возврата Битовая маска флагов, определяющих тип возвращаемых строк.</span><span class="sxs-lookup"><span data-stu-id="0aba9-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="0aba9-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="0aba9-111">The following flag can be set:</span></span>
    
<span data-ttu-id="0aba9-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0aba9-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0aba9-113">Строки в структуре **мапиеррор** , возвращаемые в параметре _лппмапиеррор_ , представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="0aba9-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="0aba9-114">Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="0aba9-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="0aba9-115">_лппмапиеррор_</span><span class="sxs-lookup"><span data-stu-id="0aba9-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="0aba9-116">вышли Указатель на указатель на возвращаемую структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки.</span><span class="sxs-lookup"><span data-stu-id="0aba9-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="0aba9-117">Параметр _лппмапиеррор_ может иметь значение null, если нет возвращаемых **мапиеррор** .</span><span class="sxs-lookup"><span data-stu-id="0aba9-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0aba9-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0aba9-118">Return value</span></span>

<span data-ttu-id="0aba9-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="0aba9-119">S_OK</span></span> 
  
> <span data-ttu-id="0aba9-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="0aba9-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0aba9-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0aba9-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0aba9-122">Установлен флаг MAPI_UNICODE, а реализация не поддерживает Юникод, или MAPI_UNICODE не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="0aba9-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0aba9-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="0aba9-123">Remarks</span></span>

<span data-ttu-id="0aba9-124">Используйте метод **имслогон:: GetLastError** для получения сведений, отображаемых в сообщении для пользователя о последней ошибке, возвращенной при вызове метода для объекта хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="0aba9-124">Use the **IMSLogon::GetLastError** method to retrieve information to display in a message to the user regarding the last error returned from a method call for the message store object.</span></span> 
  
<span data-ttu-id="0aba9-125">Чтобы освободить всю память, выделенную MAPI для возвращенной структуры **мапиеррор** , клиентским приложениям необходимо вызвать только функцию [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="0aba9-125">To release all the memory allocated by MAPI for the returned **MAPIERROR** structure, client applications need to call only the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="0aba9-126">Возвращаемое значение из **GetLastError** должно быть S_OK, чтобы приложение использовало **мапиеррор**.</span><span class="sxs-lookup"><span data-stu-id="0aba9-126">The return value from **GetLastError** must be S_OK for an application to use the **MAPIERROR**.</span></span> <span data-ttu-id="0aba9-127">Даже если возвращаемое значение равно S_OK, **мапиеррор** не может быть возвращен.</span><span class="sxs-lookup"><span data-stu-id="0aba9-127">Even if the return value is S_OK, a **MAPIERROR** might not be returned.</span></span> <span data-ttu-id="0aba9-128">Если реализация не может определить, какая Последняя ошибка, или если **мапиеррор** недоступен для этой ошибки, **GetLastError** возвращает указатель на значение NULL в _лппмапиеррор_ вместо этого.</span><span class="sxs-lookup"><span data-stu-id="0aba9-128">If the implementation cannot determine what the last error was, or if a **MAPIERROR** is not available for that error, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0aba9-129">См. также</span><span class="sxs-lookup"><span data-stu-id="0aba9-129">See also</span></span>



[<span data-ttu-id="0aba9-130">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="0aba9-130">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="0aba9-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="0aba9-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="0aba9-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0aba9-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

