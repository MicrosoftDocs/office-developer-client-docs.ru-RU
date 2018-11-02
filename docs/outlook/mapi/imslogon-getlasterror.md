---
title: IMSLogonGetLastError
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
ms.openlocfilehash: 811be1f6506cee092e487af3bd43bdf6e136d4eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568898"
---
# <a name="imslogongetlasterror"></a><span data-ttu-id="f8a16-103">IMSLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f8a16-103">IMSLogon::GetLastError</span></span>

  
  
<span data-ttu-id="f8a16-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8a16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8a16-105">Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о последней ошибке, возникшей для объекта хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f8a16-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="f8a16-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8a16-106">Parameters</span></span>

 <span data-ttu-id="f8a16-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="f8a16-107">_hResult_</span></span>
  
> <span data-ttu-id="f8a16-108">[in] Тип данных HRESULT, которое содержит значение ошибки, созданный в предыдущем вызове метода для объекта хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f8a16-108">[in] An HRESULT data type that contains the error value generated in the previous method call for the message store object.</span></span>
    
 <span data-ttu-id="f8a16-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f8a16-109">_ulFlags_</span></span>
  
> <span data-ttu-id="f8a16-110">[in] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="f8a16-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="f8a16-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="f8a16-111">The following flag can be set:</span></span>
    
<span data-ttu-id="f8a16-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f8a16-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f8a16-113">Строки в структуре **MAPIERROR** , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="f8a16-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="f8a16-114">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="f8a16-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="f8a16-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="f8a16-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="f8a16-116">[out] Указатель на указатель на структуру возвращенные **MAPIERROR** , версии, компонент и контекста сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="f8a16-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="f8a16-117">Параметр _lppMAPIError_ может быть присвоено значение NULL, если нет **MAPIERROR** для возврата.</span><span class="sxs-lookup"><span data-stu-id="f8a16-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f8a16-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8a16-118">Return value</span></span>

<span data-ttu-id="f8a16-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8a16-119">S_OK</span></span> 
  
> <span data-ttu-id="f8a16-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="f8a16-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="f8a16-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f8a16-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f8a16-122">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="f8a16-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f8a16-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="f8a16-123">Remarks</span></span>

<span data-ttu-id="f8a16-124">Используйте метод **IMSLogon::GetLastError** для получения сведений для отображения в сообщении с пользователем относительно последней ошибки, возвращаемые при вызове метода для объекта хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f8a16-124">Use the **IMSLogon::GetLastError** method to retrieve information to display in a message to the user regarding the last error returned from a method call for the message store object.</span></span> 
  
<span data-ttu-id="f8a16-125">Для освобождения всех памяти, выделенной для возвращаемых структуры **MAPIERROR** MAPI, клиентские приложения нужно вызвать функцию [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="f8a16-125">To release all the memory allocated by MAPI for the returned **MAPIERROR** structure, client applications need to call only the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="f8a16-126">Значение, возвращаемое **GetLastError** значения S_OK для приложения для использования **MAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="f8a16-126">The return value from **GetLastError** must be S_OK for an application to use the **MAPIERROR**.</span></span> <span data-ttu-id="f8a16-127">Даже если возвращает значение S_OK, **MAPIERROR** не может быть возвращено.</span><span class="sxs-lookup"><span data-stu-id="f8a16-127">Even if the return value is S_OK, a **MAPIERROR** might not be returned.</span></span> <span data-ttu-id="f8a16-128">Если реализация не может определить последнюю ошибку был или **MAPIERROR** недоступен для **, что ошибки, код последней ошибки** возвращается указатель на значение NULL в _lppMAPIError_ вместо этого.</span><span class="sxs-lookup"><span data-stu-id="f8a16-128">If the implementation cannot determine what the last error was, or if a **MAPIERROR** is not available for that error, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f8a16-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f8a16-129">See also</span></span>



[<span data-ttu-id="f8a16-130">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="f8a16-130">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="f8a16-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f8a16-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f8a16-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f8a16-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

