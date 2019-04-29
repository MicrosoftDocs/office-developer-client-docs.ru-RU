---
title: Ипровидерадминжетластеррор
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetLastError
api_type:
- COM
ms.assetid: 853ddee5-24d6-423d-b483-6a07a12de51f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4fc4867d5ca20f8e770afa239b0dffbd8ab1c480
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439851"
---
# <a name="iprovideradmingetlasterror"></a><span data-ttu-id="3a4b2-103">IProviderAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="3a4b2-103">IProviderAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="3a4b2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a4b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a4b2-105">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке, произошедшей для объекта администрирования поставщика.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="3a4b2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a4b2-106">Parameters</span></span>

 <span data-ttu-id="3a4b2-107">_Состав_</span><span class="sxs-lookup"><span data-stu-id="3a4b2-107">_hResult_</span></span>
  
> <span data-ttu-id="3a4b2-108">возврата Тип данных HRESULT, который содержит значение ошибки, возникшей при предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="3a4b2-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3a4b2-109">_ulFlags_</span></span>
  
> <span data-ttu-id="3a4b2-110">возврата Битовая маска флагов, определяющих тип возвращаемых строк.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="3a4b2-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="3a4b2-111">The following flag can be set:</span></span>
    
<span data-ttu-id="3a4b2-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3a4b2-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3a4b2-113">Строки в **мапиеррор** , возвращаемые в параметре _лппмапиеррор_ , представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-113">The strings in the **MAPIERROR** returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="3a4b2-114">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="3a4b2-115">_Лппмапиеррор_</span><span class="sxs-lookup"><span data-stu-id="3a4b2-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="3a4b2-116">вышли Указатель на указатель на возвращаемую структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="3a4b2-117">Параметр _лппмапиеррор_ может иметь значение null, если нет возвращаемых **мапиеррор** .</span><span class="sxs-lookup"><span data-stu-id="3a4b2-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3a4b2-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a4b2-118">Return value</span></span>

<span data-ttu-id="3a4b2-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="3a4b2-119">S_OK</span></span> 
  
> <span data-ttu-id="3a4b2-120">Вызов выполнен успешно и вернул ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="3a4b2-121">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="3a4b2-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="3a4b2-122">Установлен либо флаг МАПИ_УНИКОДЕ, либо **GetLastError** не поддерживает Юникод, или мапи_уникоде не задано, а **GetLastError** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3a4b2-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="3a4b2-123">Remarks</span></span>

<span data-ttu-id="3a4b2-124">Метод **ипровидерадмин:: GetLastError** предоставляет сведения о предыдущем вызове метода, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-124">The **IProviderAdmin::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="3a4b2-125">Вызывающие абоненты могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры **мапиеррор** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3a4b2-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="3a4b2-126">Notes to callers</span></span>

<span data-ttu-id="3a4b2-127">Структуру **мапиеррор** можно использовать, если MAPI предоставляет один элемент, который указывает на то, что параметр _лппмапиеррор_ указывает, только если **GetLastError** возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-127">You can use the **MAPIERROR** structure, if MAPI supplies one, that the  _lppMAPIError_ parameter points to only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="3a4b2-128">Иногда MAPI не может определить, какая ошибка прошла или больше не может сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="3a4b2-129">В этом случае указатель на NULL возвращается в _лппмапиеррор_ .</span><span class="sxs-lookup"><span data-stu-id="3a4b2-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="3a4b2-130">Более подробную информацию о методе **GetLastError** можно узнать [в статье Использование расширенных ошибок](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="3a4b2-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3a4b2-131">См. также</span><span class="sxs-lookup"><span data-stu-id="3a4b2-131">See also</span></span>



[<span data-ttu-id="3a4b2-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="3a4b2-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="3a4b2-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3a4b2-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3a4b2-134">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3a4b2-134">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

