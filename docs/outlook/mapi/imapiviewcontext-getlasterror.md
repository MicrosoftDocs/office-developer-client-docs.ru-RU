---
title: Имапивиевконтекстжетластеррор
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetLastError
api_type:
- COM
ms.assetid: 3306e37a-2500-4281-96c3-ca0d5c81909d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bcd8e977d924bae170dcad27c672b963189cfa94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351400"
---
# <a name="imapiviewcontextgetlasterror"></a><span data-ttu-id="71244-103">IMAPIViewContext::GetLastError</span><span class="sxs-lookup"><span data-stu-id="71244-103">IMAPIViewContext::GetLastError</span></span>

  
  
<span data-ttu-id="71244-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71244-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71244-105">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке, возникшей в объекте контекста представления.</span><span class="sxs-lookup"><span data-stu-id="71244-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the view context object.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="71244-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="71244-106">Parameters</span></span>

 <span data-ttu-id="71244-107">_Состав_</span><span class="sxs-lookup"><span data-stu-id="71244-107">_hResult_</span></span>
  
> <span data-ttu-id="71244-108">возврата Тип данных HRESULT, который содержит значение ошибки, возникшей при предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="71244-108">[in] HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="71244-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="71244-109">_ulFlags_</span></span>
  
> <span data-ttu-id="71244-110">возврата Битовая маска флагов, определяющих тип возвращаемых строк.</span><span class="sxs-lookup"><span data-stu-id="71244-110">[in] Bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="71244-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="71244-111">The following flag can be set:</span></span>
    
<span data-ttu-id="71244-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="71244-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="71244-113">Строки в структуре **мапиеррор** , возвращаемые в параметре _лппмапиеррор_ , представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="71244-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="71244-114">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="71244-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="71244-115">_Лппмапиеррор_</span><span class="sxs-lookup"><span data-stu-id="71244-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="71244-116">вышли Указатель на указатель на возвращаемую структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки.</span><span class="sxs-lookup"><span data-stu-id="71244-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="71244-117">Этот параметр может иметь значение NULL, если структура **мапиеррор** для возврата отсутствует.</span><span class="sxs-lookup"><span data-stu-id="71244-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="71244-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71244-118">Return value</span></span>

<span data-ttu-id="71244-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="71244-119">S_OK</span></span> 
  
> <span data-ttu-id="71244-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="71244-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="71244-121">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="71244-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="71244-122">Установлен либо флаг МАПИ_УНИКОДЕ, либо **GetLastError** не поддерживает Юникод, или мапи_уникоде не задано, а **GetLastError** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="71244-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** only supports Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="71244-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="71244-123">Remarks</span></span>

<span data-ttu-id="71244-124">Метод **имапивиевконтекст:: GetLastError** предоставляет сведения о предыдущем вызове метода, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="71244-124">The **IMAPIViewContext::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="71244-125">Вызывающие абоненты могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры **мапиеррор** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="71244-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="71244-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="71244-126">Notes to callers</span></span>

<span data-ttu-id="71244-127">Вы можете использовать структуру **мапиеррор** , на которую указывает параметр _ЛППМАПИЕРРОР_ , если MAPI предоставляет один, только если **GetLastError** возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="71244-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="71244-128">Иногда MAPI не может определить, какая ошибка прошла или больше не может сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="71244-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="71244-129">В этом случае указатель на NULL возвращается в _лппмапиеррор_ .</span><span class="sxs-lookup"><span data-stu-id="71244-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="71244-130">Дополнительные сведения о методе **GetLastError** приведены в разделе [Расширенные ошибки MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="71244-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="71244-131">См. также</span><span class="sxs-lookup"><span data-stu-id="71244-131">See also</span></span>



[<span data-ttu-id="71244-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="71244-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="71244-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="71244-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="71244-134">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="71244-134">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

