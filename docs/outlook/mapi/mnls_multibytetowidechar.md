---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Last modified: February 21, 2012'
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338243"
---
# <a name="mnls_multibytetowidechar"></a><span data-ttu-id="05f1e-103">MNLS_MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="05f1e-103">MNLS_MultiByteToWideChar</span></span>

  
  
<span data-ttu-id="05f1e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05f1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05f1e-105">Аналогично **MultiByteToWideChar,** который соповедет строку символов со строкой UTF-16 (широкий символ).</span><span class="sxs-lookup"><span data-stu-id="05f1e-105">Similar to **MultiByteToWideChar**, which maps a character string to a UTF-16 (wide character) string.</span></span> <span data-ttu-id="05f1e-106">Строка символов не обязательно из многобайтового набора символов.</span><span class="sxs-lookup"><span data-stu-id="05f1e-106">The character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a><span data-ttu-id="05f1e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="05f1e-107">Parameters</span></span>

 <span data-ttu-id="05f1e-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="05f1e-108">_uCodePage_</span></span>
  
> <span data-ttu-id="05f1e-109">[in] Кодовая страница, используемая для выполнения преобразования.</span><span class="sxs-lookup"><span data-stu-id="05f1e-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="05f1e-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="05f1e-110">_dwFlags_</span></span>
  
> <span data-ttu-id="05f1e-111">[in] Флаги, указывающие тип преобразования.</span><span class="sxs-lookup"><span data-stu-id="05f1e-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="05f1e-112">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="05f1e-112">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="05f1e-113">[in] Указатель на строку символов для преобразования.</span><span class="sxs-lookup"><span data-stu-id="05f1e-113">[in] Pointer to the character string to convert.</span></span>
    
 <span data-ttu-id="05f1e-114">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="05f1e-114">_cchMultiByte_</span></span>
  
> <span data-ttu-id="05f1e-115">[in] Размер строки, заданной параметром  _lpMultiByteStr , в 1,6 в 600 000 000 000 000 000 000 000 000 000 000_ 0</span><span class="sxs-lookup"><span data-stu-id="05f1e-115">[in] Size, in bytes, of the string indicated by the  _lpMultiByteStr_ parameter.</span></span> 
    
 <span data-ttu-id="05f1e-116">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="05f1e-116">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="05f1e-117">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="05f1e-117">[out] Optional.</span></span> <span data-ttu-id="05f1e-118">Указатель на буфер, который получает преобразованную строку.</span><span class="sxs-lookup"><span data-stu-id="05f1e-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="05f1e-119">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="05f1e-119">_cchWideChar_</span></span>
  
> <span data-ttu-id="05f1e-120">[in] Размер буфера в символах, указанный _lpWideCharStr._</span><span class="sxs-lookup"><span data-stu-id="05f1e-120">[in] Size, in characters, of the buffer indicated by  _lpWideCharStr_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="05f1e-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05f1e-121">Return value</span></span>

<span data-ttu-id="05f1e-122">Возвращает количество символов, написанных в буфере,  _обозначенное lpWideCharStr в_ случае успешного успеха.</span><span class="sxs-lookup"><span data-stu-id="05f1e-122">Returns the number of characters written to the buffer indicated by  _lpWideCharStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="05f1e-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="05f1e-123">Remarks</span></span>

<span data-ttu-id="05f1e-124">Эта функция обтекает функцию **MultiByteToWideChar.**</span><span class="sxs-lookup"><span data-stu-id="05f1e-124">This function wraps the **MultiByteToWideChar** function.</span></span> <span data-ttu-id="05f1e-125">Дополнительные сведения см. в [подзагоду MultiByteToWideChar.](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05f1e-125">For more information, see [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).</span></span>
  

