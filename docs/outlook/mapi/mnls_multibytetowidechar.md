---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Последнее изменение: 21 февраля 2012 г.'
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389556"
---
# <a name="mnlsmultibytetowidechar"></a><span data-ttu-id="40c4c-103">MNLS_MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="40c4c-103">MNLS_MultiByteToWideChar</span></span>

  
  
<span data-ttu-id="40c4c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40c4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40c4c-105">Аналогично **MultiByteToWideChar**, которая соответствует строка символов строки UTF-16 (двухбайтовых знаков).</span><span class="sxs-lookup"><span data-stu-id="40c4c-105">Similar to **MultiByteToWideChar**, which maps a character string to a UTF-16 (wide character) string.</span></span> <span data-ttu-id="40c4c-106">Строку знаков не обязательно из многобайтовой задан.</span><span class="sxs-lookup"><span data-stu-id="40c4c-106">The character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a><span data-ttu-id="40c4c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="40c4c-107">Parameters</span></span>

 <span data-ttu-id="40c4c-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="40c4c-108">_uCodePage_</span></span>
  
> <span data-ttu-id="40c4c-109">[in] Кодовая страница следует использовать при выполнении преобразования.</span><span class="sxs-lookup"><span data-stu-id="40c4c-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="40c4c-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="40c4c-110">_dwFlags_</span></span>
  
> <span data-ttu-id="40c4c-111">[in] Флаги, указывающее тип преобразования.</span><span class="sxs-lookup"><span data-stu-id="40c4c-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="40c4c-112">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="40c4c-112">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="40c4c-113">[in] Указатель на строку знаков для преобразования.</span><span class="sxs-lookup"><span data-stu-id="40c4c-113">[in] Pointer to the character string to convert.</span></span>
    
 <span data-ttu-id="40c4c-114">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="40c4c-114">_cchMultiByte_</span></span>
  
> <span data-ttu-id="40c4c-115">[in] Размер, в байтах, указанное с помощью параметра _lpMultiByteStr_ строки.</span><span class="sxs-lookup"><span data-stu-id="40c4c-115">[in] Size, in bytes, of the string indicated by the  _lpMultiByteStr_ parameter.</span></span> 
    
 <span data-ttu-id="40c4c-116">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="40c4c-116">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="40c4c-117">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="40c4c-117">[out] Optional.</span></span> <span data-ttu-id="40c4c-118">Указатель на буфер, получающий Преобразованная строка.</span><span class="sxs-lookup"><span data-stu-id="40c4c-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="40c4c-119">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="40c4c-119">_cchWideChar_</span></span>
  
> <span data-ttu-id="40c4c-120">[in] Размер в знаков, указанный в параметре _lpWideCharStr_буфера.</span><span class="sxs-lookup"><span data-stu-id="40c4c-120">[in] Size, in characters, of the buffer indicated by  _lpWideCharStr_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="40c4c-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="40c4c-121">Return value</span></span>

<span data-ttu-id="40c4c-122">Возвращает число знаков в буфер, указанный в параметре _lpWideCharStr_ в случае успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="40c4c-122">Returns the number of characters written to the buffer indicated by  _lpWideCharStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="40c4c-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="40c4c-123">Remarks</span></span>

<span data-ttu-id="40c4c-124">Эта функция имеет функцию **MultiByteToWideChar** .</span><span class="sxs-lookup"><span data-stu-id="40c4c-124">This function wraps the **MultiByteToWideChar** function.</span></span> <span data-ttu-id="40c4c-125">Для получения дополнительных сведений см [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="40c4c-125">For more information, see [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).</span></span>
  

