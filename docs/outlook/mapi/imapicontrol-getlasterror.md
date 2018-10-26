---
title: IMAPIControlGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetLastError
api_type:
- COM
ms.assetid: 83290b8e-fffc-41c8-a01e-578d130b65c5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ef5fee7a2e84133f88a00703f7602831d26e3d3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594728"
---
# <a name="imapicontrolgetlasterror"></a><span data-ttu-id="69fa7-103">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="69fa7-103">IMAPIControl::GetLastError</span></span>

  
  
<span data-ttu-id="69fa7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69fa7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69fa7-105">Возвращает структуру [MAPIERROR](mapierror.md) , которая содержит сведения об ошибке предыдущего элемента управления кнопка.</span><span class="sxs-lookup"><span data-stu-id="69fa7-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="69fa7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="69fa7-106">Parameters</span></span>

 <span data-ttu-id="69fa7-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="69fa7-107">_hResult_</span></span>
  
> <span data-ttu-id="69fa7-108">[in] Дескриптор значение ошибки, созданный в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="69fa7-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="69fa7-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="69fa7-109">_ulFlags_</span></span>
  
> <span data-ttu-id="69fa7-110">[in] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="69fa7-110">[in] A bitmask of flags that controls the type of the strings returned.</span></span> <span data-ttu-id="69fa7-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="69fa7-111">The following flag can be set:</span></span>
    
<span data-ttu-id="69fa7-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="69fa7-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="69fa7-113">Строки в структуре **MAPIERROR** , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="69fa7-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="69fa7-114">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="69fa7-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="69fa7-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="69fa7-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="69fa7-116">[out] Указатель на указатель на структуру **MAPIERROR** , который содержит сведения о версии, компонент и контекста для ошибки.</span><span class="sxs-lookup"><span data-stu-id="69fa7-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="69fa7-117">Параметр _lppMAPIError_ может быть присвоено значение NULL, если поставщик не может предоставить структуру **MAPIERROR** , используя соответствующие сведения.</span><span class="sxs-lookup"><span data-stu-id="69fa7-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="69fa7-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69fa7-118">Return value</span></span>

<span data-ttu-id="69fa7-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="69fa7-119">S_OK</span></span> 
  
> <span data-ttu-id="69fa7-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="69fa7-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="69fa7-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="69fa7-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="69fa7-122">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="69fa7-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="69fa7-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="69fa7-123">Remarks</span></span>

<span data-ttu-id="69fa7-124">Поставщики услуг реализуйте метод **IMAPIControl::GetLastError** для предоставления сведений о предыдущий вызов, завершившихся сбоем.</span><span class="sxs-lookup"><span data-stu-id="69fa7-124">Service providers implement the **IMAPIControl::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="69fa7-125">MAPI могут предоставить пользователям подробные сведения об ошибке, отображая данные из структуры **MAPIERROR** в окне сообщения или диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="69fa7-125">MAPI can give users detailed information about the error by displaying the data from the **MAPIERROR** structure in a message or dialog box.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="69fa7-126">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="69fa7-126">Notes to implementers</span></span>

<span data-ttu-id="69fa7-127">Необходимо иметь сведения для включения в структуре **MAPIERROR** для каждой ошибки.</span><span class="sxs-lookup"><span data-stu-id="69fa7-127">You do not need to have information to include in the **MAPIERROR** structure for every error.</span></span> <span data-ttu-id="69fa7-128">Не может быть невозможно определить, был предыдущей ошибки.</span><span class="sxs-lookup"><span data-stu-id="69fa7-128">It may not be possible to determine what the previous error was.</span></span> <span data-ttu-id="69fa7-129">Если у вас есть сведения, возвращает значение S_OK и требуемые данные в структуре **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="69fa7-129">If you have information, return S_OK and the appropriate data in the **MAPIERROR** structure.</span></span> <span data-ttu-id="69fa7-130">Если доступные данные не возвращает значение S_OK и указатель значение NULL для параметра _lppMAPIError_ .</span><span class="sxs-lookup"><span data-stu-id="69fa7-130">If no information is available, return S_OK and a pointer to NULL for the  _lppMAPIError_ parameter.</span></span> 
  
<span data-ttu-id="69fa7-131">Дополнительные сведения о методе **GetLastError** отображаются [Ошибки расширенного MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="69fa7-131">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="69fa7-132">См. также</span><span class="sxs-lookup"><span data-stu-id="69fa7-132">See also</span></span>



[<span data-ttu-id="69fa7-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="69fa7-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="69fa7-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="69fa7-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="69fa7-135">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="69fa7-135">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

