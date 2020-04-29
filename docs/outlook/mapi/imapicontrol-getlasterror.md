---
title: имапиконтролжетластеррор
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
ms.openlocfilehash: 10ac4e33b3f734ec2ce3205aa1897e0418cb563d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421153"
---
# <a name="imapicontrolgetlasterror"></a><span data-ttu-id="6ae40-103">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6ae40-103">IMAPIControl::GetLastError</span></span>

  
  
<span data-ttu-id="6ae40-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ae40-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ae40-105">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке элемента управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="6ae40-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="6ae40-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ae40-106">Parameters</span></span>

 <span data-ttu-id="6ae40-107">_Состав_</span><span class="sxs-lookup"><span data-stu-id="6ae40-107">_hResult_</span></span>
  
> <span data-ttu-id="6ae40-108">возврата Дескриптор значения ошибки, возникшей при предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="6ae40-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="6ae40-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6ae40-109">_ulFlags_</span></span>
  
> <span data-ttu-id="6ae40-110">возврата Битовая маска флагов, определяющая тип возвращаемых строк.</span><span class="sxs-lookup"><span data-stu-id="6ae40-110">[in] A bitmask of flags that controls the type of the strings returned.</span></span> <span data-ttu-id="6ae40-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="6ae40-111">The following flag can be set:</span></span>
    
<span data-ttu-id="6ae40-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6ae40-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6ae40-113">Строки в структуре **мапиеррор** , возвращаемые в параметре _лппмапиеррор_ , представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="6ae40-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="6ae40-114">Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="6ae40-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="6ae40-115">_лппмапиеррор_</span><span class="sxs-lookup"><span data-stu-id="6ae40-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="6ae40-116">вышли Указатель на указатель на структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки.</span><span class="sxs-lookup"><span data-stu-id="6ae40-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="6ae40-117">Параметр _лппмапиеррор_ может иметь значение null, если поставщик не может предоставить структуру **мапиеррор** с соответствующей информацией.</span><span class="sxs-lookup"><span data-stu-id="6ae40-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6ae40-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ae40-118">Return value</span></span>

<span data-ttu-id="6ae40-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="6ae40-119">S_OK</span></span> 
  
> <span data-ttu-id="6ae40-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="6ae40-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6ae40-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="6ae40-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="6ae40-122">Установлен флаг MAPI_UNICODE, а реализация не поддерживает Юникод, или MAPI_UNICODE не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="6ae40-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6ae40-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="6ae40-123">Remarks</span></span>

<span data-ttu-id="6ae40-124">Поставщики услуг реализуют метод **имапиконтрол:: GetLastError** для предоставления сведений о предыдущем вызове метода, который завершился неудачно.</span><span class="sxs-lookup"><span data-stu-id="6ae40-124">Service providers implement the **IMAPIControl::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="6ae40-125">MAPI может предоставить пользователям подробные сведения об ошибке, выполнив отображение данных из структуры **мапиеррор** в сообщении или диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="6ae40-125">MAPI can give users detailed information about the error by displaying the data from the **MAPIERROR** structure in a message or dialog box.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6ae40-126">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="6ae40-126">Notes to implementers</span></span>

<span data-ttu-id="6ae40-127">Для каждой ошибки не требуется наличие информации для включения в структуру **мапиеррор** .</span><span class="sxs-lookup"><span data-stu-id="6ae40-127">You do not need to have information to include in the **MAPIERROR** structure for every error.</span></span> <span data-ttu-id="6ae40-128">Невозможность определить предыдущую ошибку.</span><span class="sxs-lookup"><span data-stu-id="6ae40-128">It may not be possible to determine what the previous error was.</span></span> <span data-ttu-id="6ae40-129">Если у вас есть сведения, возвращайте S_OK и соответствующие данные в структуре **мапиеррор** .</span><span class="sxs-lookup"><span data-stu-id="6ae40-129">If you have information, return S_OK and the appropriate data in the **MAPIERROR** structure.</span></span> <span data-ttu-id="6ae40-130">Если сведения недоступны, возвращается S_OK и указатель на NULL для параметра _лппмапиеррор_ .</span><span class="sxs-lookup"><span data-stu-id="6ae40-130">If no information is available, return S_OK and a pointer to NULL for the  _lppMAPIError_ parameter.</span></span> 
  
<span data-ttu-id="6ae40-131">Дополнительные сведения о методе **GetLastError** приведены в разделе [Расширенные ошибки MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="6ae40-131">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6ae40-132">См. также</span><span class="sxs-lookup"><span data-stu-id="6ae40-132">See also</span></span>



[<span data-ttu-id="6ae40-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="6ae40-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="6ae40-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6ae40-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="6ae40-135">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6ae40-135">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

