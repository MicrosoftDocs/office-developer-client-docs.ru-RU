---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Last modified: February 21, 2012'
ms.openlocfilehash: ad41f9b6060e5cfbabecfd9bb29a47815929d6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338733"
---
# <a name="mnls_widechartomultibyte"></a><span data-ttu-id="3cdd3-103">MNLS_WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="3cdd3-103">MNLS_WideCharToMultiByte</span></span>

  
  
<span data-ttu-id="3cdd3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cdd3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cdd3-105">Эта функция похожа на **WideCharToMultiByte,** которая соповедет строку UTF-16 (широкий символ) с новой строкой символов.</span><span class="sxs-lookup"><span data-stu-id="3cdd3-105">This function is similar to **WideCharToMultiByte**, which maps a UTF-16 (wide character) string to a new character string.</span></span> <span data-ttu-id="3cdd3-106">Новая строка символов не обязательно из многобайтового набора символов.</span><span class="sxs-lookup"><span data-stu-id="3cdd3-106">The new character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_WideCharToMultiByte(
  UINT uCodePage,
  DWORD dwFlags,
  LPCWSTR lpWideCharStr,
  int cchWideChar,
  LPSTR lpMultiByteStr,
  int cchMultiByte,
  LPCSTR lpDefaultChar,
  BOOL FAR *lpfUsedDefaultChar);
```

## <a name="parameters"></a><span data-ttu-id="3cdd3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cdd3-107">Parameters</span></span>

 <span data-ttu-id="3cdd3-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="3cdd3-108">_uCodePage_</span></span>
  
> <span data-ttu-id="3cdd3-109">[in] Кодовая страница, используемая для выполнения преобразования.</span><span class="sxs-lookup"><span data-stu-id="3cdd3-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="3cdd3-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="3cdd3-110">_dwFlags_</span></span>
  
> <span data-ttu-id="3cdd3-111">[in] Флаги, указывающие тип преобразования.</span><span class="sxs-lookup"><span data-stu-id="3cdd3-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="3cdd3-112">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="3cdd3-112">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="3cdd3-113">[in] Указатель на строку Юникода для преобразования.</span><span class="sxs-lookup"><span data-stu-id="3cdd3-113">[in] Pointer to the Unicode string to convert.</span></span>
    
 <span data-ttu-id="3cdd3-114">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="3cdd3-114">_cchWideChar_</span></span>
  
> <span data-ttu-id="3cdd3-115">[in] Флаги, указывающие тип преобразования.</span><span class="sxs-lookup"><span data-stu-id="3cdd3-115">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="3cdd3-116">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="3cdd3-116">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="3cdd3-117">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="3cdd3-117">[out] Optional.</span></span> <span data-ttu-id="3cdd3-118">Указатель на буфер, который получает преобразованную строку.</span><span class="sxs-lookup"><span data-stu-id="3cdd3-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="3cdd3-119">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="3cdd3-119">_cchMultiByte_</span></span>
  
> <span data-ttu-id="3cdd3-120">[in] Размер буфера, указанный  _lpMultiByteStr_( в bytes).</span><span class="sxs-lookup"><span data-stu-id="3cdd3-120">[in] Size, in bytes, of the buffer indicated by  _lpMultiByteStr_.</span></span>
    
 <span data-ttu-id="3cdd3-121">_lpDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="3cdd3-121">_lpDefaultChar_</span></span>
  
> <span data-ttu-id="3cdd3-122">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="3cdd3-122">[in] Optional.</span></span> <span data-ttu-id="3cdd3-123">Указатель на символ, который следует использовать, если символ не может быть представлен на указанной кодовой странице.</span><span class="sxs-lookup"><span data-stu-id="3cdd3-123">Pointer to the character to use if a character cannot be represented in the specified code page.</span></span>
    
 <span data-ttu-id="3cdd3-124">_lpfUsedDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="3cdd3-124">_lpfUsedDefaultChar_</span></span>
  
> <span data-ttu-id="3cdd3-125">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="3cdd3-125">[out] Optional.</span></span> <span data-ttu-id="3cdd3-126">Указатель на флаг, который указывает, использовала ли функция символ по умолчанию в преобразовании.</span><span class="sxs-lookup"><span data-stu-id="3cdd3-126">Pointer to a flag that indicates if the function has used a default character in the conversion.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3cdd3-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3cdd3-127">Return value</span></span>

<span data-ttu-id="3cdd3-128">В случае успешного успешного с помощью lpMultiByteStr возвращается количество в буфере, на которые указывает _lpMultiByteStr._</span><span class="sxs-lookup"><span data-stu-id="3cdd3-128">Returns the number of bytes written to the buffer pointed to by  _lpMultiByteStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3cdd3-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="3cdd3-129">Remarks</span></span>

<span data-ttu-id="3cdd3-130">Эта функция обтекает **функцию WideCharToMultiByte.**</span><span class="sxs-lookup"><span data-stu-id="3cdd3-130">This function wraps the **WideCharToMultiByte** function.</span></span> <span data-ttu-id="3cdd3-131">Дополнительные сведения [см. в подзаголовке WideCharToMultiByte.](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cdd3-131">For more information, see [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3cdd3-132">См. также</span><span class="sxs-lookup"><span data-stu-id="3cdd3-132">See also</span></span>



[<span data-ttu-id="3cdd3-133">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="3cdd3-133">WideCharToMultiByte</span></span>](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

