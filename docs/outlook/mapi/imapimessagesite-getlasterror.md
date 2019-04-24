---
title: Имапимессажеситежетластеррор
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetLastError
api_type:
- COM
ms.assetid: 7ea282d7-388a-4f05-9780-f8dbc5c5d395
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cc4de8aa21d4b3b27bf757389b663ebeff69a9cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321380"
---
# <a name="imapimessagesitegetlasterror"></a><span data-ttu-id="feae3-103">IMAPIMessageSite::GetLastError</span><span class="sxs-lookup"><span data-stu-id="feae3-103">IMAPIMessageSite::GetLastError</span></span>

  
  
<span data-ttu-id="feae3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="feae3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="feae3-105">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке, возникшей в объекте сайта сообщения.</span><span class="sxs-lookup"><span data-stu-id="feae3-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="feae3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="feae3-106">Parameters</span></span>

 <span data-ttu-id="feae3-107">_Состав_</span><span class="sxs-lookup"><span data-stu-id="feae3-107">_hResult_</span></span>
  
> <span data-ttu-id="feae3-108">возврата Значение HRESULT, содержащее значение ошибки, созданное в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="feae3-108">[in] An HRESULT that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="feae3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="feae3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="feae3-110">возврата Битовая маска флагов, определяющих тип возвращаемых строк.</span><span class="sxs-lookup"><span data-stu-id="feae3-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="feae3-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="feae3-111">The following flag can be set:</span></span>
    
<span data-ttu-id="feae3-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="feae3-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="feae3-113">Строки в структуре **мапиеррор** , возвращаемые в параметре _лппмапиеррор_ , представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="feae3-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="feae3-114">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="feae3-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="feae3-115">_Лппмапиеррор_</span><span class="sxs-lookup"><span data-stu-id="feae3-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="feae3-116">вышли Указатель на указатель на возвращаемую структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки.</span><span class="sxs-lookup"><span data-stu-id="feae3-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="feae3-117">Этот параметр может иметь значение NULL, если структура **мапиеррор** для возврата отсутствует.</span><span class="sxs-lookup"><span data-stu-id="feae3-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="feae3-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="feae3-118">Return value</span></span>

<span data-ttu-id="feae3-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="feae3-119">S_OK</span></span>
  
> <span data-ttu-id="feae3-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="feae3-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="feae3-121">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="feae3-121">MAPI_E_BAD_CHARWIDTH</span></span>
  
> <span data-ttu-id="feae3-122">Установлен либо флаг МАПИ_УНИКОДЕ, либо **GetLastError** не поддерживает Юникод, или мапи_уникоде не задано, а **GetLastError** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="feae3-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="feae3-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="feae3-123">Remarks</span></span>

<span data-ttu-id="feae3-124">Метод **имапимессажесите:: GetLastError** предоставляет сведения о предыдущем вызове метода, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="feae3-124">The **IMAPIMessageSite::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="feae3-125">Вызывающие абоненты могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры **мапиеррор** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="feae3-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="feae3-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="feae3-126">Notes to callers</span></span>

<span data-ttu-id="feae3-127">Вы можете использовать структуру **мапиеррор** , на которую указывает параметр _ЛППМАПИЕРРОР_ , если MAPI предоставляет один, только если **GetLastError** возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="feae3-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="feae3-128">Иногда MAPI не может определить, в чем последняя ошибка, или больше не сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="feae3-128">Sometimes MAPI cannot determine what the last error was, or has nothing more to report about the error.</span></span> <span data-ttu-id="feae3-129">В этом случае указатель на NULL возвращается в _лппмапиеррор_ .</span><span class="sxs-lookup"><span data-stu-id="feae3-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="feae3-130">Более подробную информацию о методе **GetLastError** можно узнать [в статье Использование расширенных ошибок](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="feae3-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="feae3-131">См. также</span><span class="sxs-lookup"><span data-stu-id="feae3-131">See also</span></span>



[<span data-ttu-id="feae3-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="feae3-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="feae3-133">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="feae3-133">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)

