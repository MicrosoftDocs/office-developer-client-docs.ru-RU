---
title: IMAPITableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetLastError
api_type:
- COM
ms.assetid: 832e2c18-ddba-4d18-a391-710d21fe23e6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8b7b1db5bcc718858b01f122f53406c885998741
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593818"
---
# <a name="imapitablegetlasterror"></a><span data-ttu-id="09ec4-103">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="09ec4-103">IMAPITable::GetLastError</span></span>

  
  
<span data-ttu-id="09ec4-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09ec4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09ec4-105">Возвращает структуру [MAPIERROR](mapierror.md) , содержащий сведения о предыдущем ошибки в таблице.</span><span class="sxs-lookup"><span data-stu-id="09ec4-105">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="09ec4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="09ec4-106">Parameters</span></span>

 <span data-ttu-id="09ec4-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="09ec4-107">_hResult_</span></span>
  
> <span data-ttu-id="09ec4-108">[in] Значение HRESULT, содержащий ошибку, созданный в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="09ec4-108">[in] HRESULT containing the error generated in the previous method call.</span></span>
    
 <span data-ttu-id="09ec4-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="09ec4-109">_ulFlags_</span></span>
  
> <span data-ttu-id="09ec4-110">[in] Битовая маска флаги, определяющее тип возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="09ec4-110">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="09ec4-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="09ec4-111">The following flag can be set:</span></span>
    
<span data-ttu-id="09ec4-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="09ec4-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="09ec4-113">Строки в структуре **MAPIERROR** , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="09ec4-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="09ec4-114">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="09ec4-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="09ec4-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="09ec4-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="09ec4-116">[out] Указатель на указатель на структуру возвращенные **MAPIERROR** , содержащий версии, компонент и контекста сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="09ec4-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="09ec4-117">Параметр _lppMAPIError_ может быть присвоено значение NULL, если структуру **MAPIERROR** , используя соответствующие сведения.</span><span class="sxs-lookup"><span data-stu-id="09ec4-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="09ec4-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="09ec4-118">Return value</span></span>

<span data-ttu-id="09ec4-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="09ec4-119">S_OK</span></span> 
  
> <span data-ttu-id="09ec4-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="09ec4-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="09ec4-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="09ec4-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="09ec4-122">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="09ec4-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="09ec4-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="09ec4-123">Remarks</span></span>

<span data-ttu-id="09ec4-124">Метод **IMAPITable::GetLastError** возвращает подробные сведения, если он доступен, о вызов предыдущего метода, который не удалось.</span><span class="sxs-lookup"><span data-stu-id="09ec4-124">The **IMAPITable::GetLastError** method returns detailed information, if available, about a prior method call that failed.</span></span> <span data-ttu-id="09ec4-125">Эти сведения могут отображаться в сообщении или диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="09ec4-125">This information can be displayed in a message or a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="09ec4-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="09ec4-126">Notes to callers</span></span>

<span data-ttu-id="09ec4-127">Вызов **GetLastError** каждый раз, когда необходимо отобразить сведения об ошибке для пользователя.</span><span class="sxs-lookup"><span data-stu-id="09ec4-127">Call **GetLastError** whenever you need to display information about an error to the user.</span></span> 
  
<span data-ttu-id="09ec4-128">Чтобы использовать [MAPIERROR](mapierror.md) структуры, на который указывает с помощью параметра _lppMAPIError_ Если объект таблицы его предоставляет только в том случае, если **код последней ошибки** возвращается значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="09ec4-128">You can make use of the [MAPIERROR](mapierror.md) structure pointed to by the  _lppMAPIError_ parameter if the table object supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="09ec4-129">В некоторых случаях реализации таблицы не может определить, что последнее сообщение об ошибке была или Дополнительно, чтобы сообщить об ошибке не содержит.</span><span class="sxs-lookup"><span data-stu-id="09ec4-129">Sometimes the table implementation cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="09ec4-130">В этом случае указатель мыши в _lppMAPIError_ имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="09ec4-130">In this situation, the pointer at  _lppMAPIError_ is set to NULL.</span></span> 
  
<span data-ttu-id="09ec4-131">Для освобождения всех памяти, выделенный для структуры **MAPIERROR** , вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="09ec4-131">To release all the memory allocated for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="09ec4-132">Дополнительные сведения о методе **GetLastError** отображаются [Ошибки расширенного MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="09ec4-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="09ec4-133">См. также</span><span class="sxs-lookup"><span data-stu-id="09ec4-133">See also</span></span>



[<span data-ttu-id="09ec4-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="09ec4-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="09ec4-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="09ec4-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="09ec4-136">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="09ec4-136">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

