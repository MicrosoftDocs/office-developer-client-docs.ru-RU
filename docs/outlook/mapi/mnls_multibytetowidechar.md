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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338243"
---
# <a name="mnls_multibytetowidechar"></a><span data-ttu-id="cbbe9-103">MNLS_MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="cbbe9-103">MNLS_MultiByteToWideChar</span></span>

  
  
<span data-ttu-id="cbbe9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbbe9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbbe9-105">Как и **MultiByteToWideChar,** которая сопоповедет строку символов со строкой UTF-16 (широкий символ).</span><span class="sxs-lookup"><span data-stu-id="cbbe9-105">Similar to **MultiByteToWideChar**, which maps a character string to a UTF-16 (wide character) string.</span></span> <span data-ttu-id="cbbe9-106">Строка символов не обязательно из набора многобайтных символов.</span><span class="sxs-lookup"><span data-stu-id="cbbe9-106">The character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a><span data-ttu-id="cbbe9-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="cbbe9-107">Parameters</span></span>

 <span data-ttu-id="cbbe9-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="cbbe9-108">_uCodePage_</span></span>
  
> <span data-ttu-id="cbbe9-109">[in] Страница кода, используемая для выполнения преобразования.</span><span class="sxs-lookup"><span data-stu-id="cbbe9-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="cbbe9-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="cbbe9-110">_dwFlags_</span></span>
  
> <span data-ttu-id="cbbe9-111">[in] Флаги, указывающие тип преобразования.</span><span class="sxs-lookup"><span data-stu-id="cbbe9-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="cbbe9-112">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="cbbe9-112">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="cbbe9-113">[in] Указатель на строку символов для преобразования.</span><span class="sxs-lookup"><span data-stu-id="cbbe9-113">[in] Pointer to the character string to convert.</span></span>
    
 <span data-ttu-id="cbbe9-114">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="cbbe9-114">_cchMultiByte_</span></span>
  
> <span data-ttu-id="cbbe9-115">[in] Размер в bytes строки, обозначенной параметром _lpMultiByteStr._</span><span class="sxs-lookup"><span data-stu-id="cbbe9-115">[in] Size, in bytes, of the string indicated by the  _lpMultiByteStr_ parameter.</span></span> 
    
 <span data-ttu-id="cbbe9-116">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="cbbe9-116">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="cbbe9-117">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="cbbe9-117">[out] Optional.</span></span> <span data-ttu-id="cbbe9-118">Указатель на буфер, который получает преобразованную строку.</span><span class="sxs-lookup"><span data-stu-id="cbbe9-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="cbbe9-119">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="cbbe9-119">_cchWideChar_</span></span>
  
> <span data-ttu-id="cbbe9-120">[in] Размер буфера в символах, указанный  _lpWideCharStr_.</span><span class="sxs-lookup"><span data-stu-id="cbbe9-120">[in] Size, in characters, of the buffer indicated by  _lpWideCharStr_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cbbe9-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbbe9-121">Return value</span></span>

<span data-ttu-id="cbbe9-122">Возвращает количество символов, написанных в буфер, указанный  _lpWideCharStr_ в случае успешного сбоя.</span><span class="sxs-lookup"><span data-stu-id="cbbe9-122">Returns the number of characters written to the buffer indicated by  _lpWideCharStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cbbe9-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="cbbe9-123">Remarks</span></span>

<span data-ttu-id="cbbe9-124">Эта функция завершает функцию **MultiByteToWideChar.**</span><span class="sxs-lookup"><span data-stu-id="cbbe9-124">This function wraps the **MultiByteToWideChar** function.</span></span> <span data-ttu-id="cbbe9-125">Дополнительные сведения см. [в см. в фотогаракте MultiByteToWideChar.](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbbe9-125">For more information, see [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).</span></span>
  

