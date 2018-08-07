---
title: IABLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetLastError
api_type:
- COM
ms.assetid: d157e29e-7731-4e47-b4a7-e8622b223001
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bead72ab2b394634217c9ae219a03a98752ef27d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808712"
---
# <a name="iablogongetlasterror"></a><span data-ttu-id="3e7b5-103">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="3e7b5-103">IABLogon::GetLastError</span></span>

  
  
<span data-ttu-id="3e7b5-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3e7b5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3e7b5-105">Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем Ошибка поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3e7b5-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="3e7b5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e7b5-106">Parameters</span></span>

 <span data-ttu-id="3e7b5-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="3e7b5-107">_hResult_</span></span>
  
> <span data-ttu-id="3e7b5-108">[in] Дескриптор значение ошибки, созданный в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="3e7b5-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="3e7b5-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3e7b5-109">_ulFlags_</span></span>
  
> <span data-ttu-id="3e7b5-110">[in] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="3e7b5-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="3e7b5-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="3e7b5-111">The following flag can be set:</span></span>
    
<span data-ttu-id="3e7b5-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3e7b5-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3e7b5-113">Строки в структуре **MAPIERROR** , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="3e7b5-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="3e7b5-114">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="3e7b5-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="3e7b5-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="3e7b5-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="3e7b5-116">[out] Указатель на указатель на структуру **MAPIERROR** , который содержит сведения о версии, компонент и контекста для ошибки.</span><span class="sxs-lookup"><span data-stu-id="3e7b5-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="3e7b5-117">Параметр _lppMAPIError_ может быть присвоено значение NULL, если поставщик не может предоставить структуру **MAPIERROR** , используя соответствующие сведения.</span><span class="sxs-lookup"><span data-stu-id="3e7b5-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3e7b5-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="3e7b5-118">Return value</span></span>

<span data-ttu-id="3e7b5-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="3e7b5-119">S_OK</span></span> 
  
> <span data-ttu-id="3e7b5-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="3e7b5-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="3e7b5-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="3e7b5-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="3e7b5-122">Либо был установлен флажок MAPI_UNICODE и поставщик адресной книги не поддерживает Юникод, или MAPI_UNICODE не было установлено и поддерживает только Юникод в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="3e7b5-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3e7b5-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="3e7b5-123">Remarks</span></span>

<span data-ttu-id="3e7b5-124">Метод **GetLastError** для предоставления сведений о предыдущий вызов, завершившихся сбоем, реализуемые поставщиками адресных книг.</span><span class="sxs-lookup"><span data-stu-id="3e7b5-124">Address book providers implement the **GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="3e7b5-125">Вызывающие объекты можно предоставить своим пользователям подробные сведения об ошибке, включая данные из структуры **MAPIERROR** в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3e7b5-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3e7b5-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="3e7b5-126">Notes to callers</span></span>

<span data-ttu-id="3e7b5-127">Можно использовать структуры **MAPIERROR** , на который указывает параметр _lppMAPIError_ , если поставщик адресной книги предоставляет структуру и **код последней ошибки** возвращается значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="3e7b5-127">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if the address book provider supplies the structure and only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="3e7b5-128">В некоторых случаях поставщик адресной книги не может определить, что последнее сообщение об ошибке была или Дополнительно, чтобы сообщить об ошибке не содержит.</span><span class="sxs-lookup"><span data-stu-id="3e7b5-128">Sometimes the address book provider cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="3e7b5-129">В этом случае поставщик адресной книги возвращает указатель на значение NULL в _lppMAPIError_ вместо этого.</span><span class="sxs-lookup"><span data-stu-id="3e7b5-129">In this situation, the address book provider returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="3e7b5-130">Дополнительные сведения о методе **GetLastError** отображаются [Ошибки расширенного MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="3e7b5-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3e7b5-131">См. также</span><span class="sxs-lookup"><span data-stu-id="3e7b5-131">See also</span></span>



[<span data-ttu-id="3e7b5-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="3e7b5-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="3e7b5-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3e7b5-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3e7b5-134">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3e7b5-134">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

