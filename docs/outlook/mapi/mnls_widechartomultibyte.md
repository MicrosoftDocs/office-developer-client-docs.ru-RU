---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Дата последнего изменения: 21 февраля 2012 г.'
ms.openlocfilehash: ad41f9b6060e5cfbabecfd9bb29a47815929d6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338733"
---
# <a name="mnls_widechartomultibyte"></a><span data-ttu-id="dc3d0-103">MNLS_WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="dc3d0-103">MNLS_WideCharToMultiByte</span></span>

  
  
<span data-ttu-id="dc3d0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc3d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc3d0-105">Эта функция аналогична **видечартомултибите**, которая СОПОСТАВЛЯЕТ строку UTF-16 (Wide знака) с новой строкой символов.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-105">This function is similar to **WideCharToMultiByte**, which maps a UTF-16 (wide character) string to a new character string.</span></span> <span data-ttu-id="dc3d0-106">Новая строка символов не обязательно должна быть из многобайтового набора символов.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-106">The new character string is not necessarily from a multibyte character set.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="dc3d0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc3d0-107">Parameters</span></span>

 <span data-ttu-id="dc3d0-108">_укодепаже_</span><span class="sxs-lookup"><span data-stu-id="dc3d0-108">_uCodePage_</span></span>
  
> <span data-ttu-id="dc3d0-109">возврата Кодовая страница, используемая для выполнения преобразования.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="dc3d0-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="dc3d0-110">_dwFlags_</span></span>
  
> <span data-ttu-id="dc3d0-111">возврата Флаги, указывающие тип преобразования.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="dc3d0-112">_лпвидечарстр_</span><span class="sxs-lookup"><span data-stu-id="dc3d0-112">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="dc3d0-113">возврата Указатель на строку Юникода для преобразования.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-113">[in] Pointer to the Unicode string to convert.</span></span>
    
 <span data-ttu-id="dc3d0-114">_кчвидечар_</span><span class="sxs-lookup"><span data-stu-id="dc3d0-114">_cchWideChar_</span></span>
  
> <span data-ttu-id="dc3d0-115">возврата Флаги, указывающие тип преобразования.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-115">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="dc3d0-116">_лпмултибитестр_</span><span class="sxs-lookup"><span data-stu-id="dc3d0-116">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="dc3d0-117">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-117">[out] Optional.</span></span> <span data-ttu-id="dc3d0-118">Указатель на буфер, который получает преобразованную строку.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="dc3d0-119">_кчмултибите_</span><span class="sxs-lookup"><span data-stu-id="dc3d0-119">_cchMultiByte_</span></span>
  
> <span data-ttu-id="dc3d0-120">возврата Размер буфера (в байтах), указанного в _лпмултибитестр_.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-120">[in] Size, in bytes, of the buffer indicated by  _lpMultiByteStr_.</span></span>
    
 <span data-ttu-id="dc3d0-121">_лпдефаултчар_</span><span class="sxs-lookup"><span data-stu-id="dc3d0-121">_lpDefaultChar_</span></span>
  
> <span data-ttu-id="dc3d0-122">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-122">[in] Optional.</span></span> <span data-ttu-id="dc3d0-123">Указатель на символ, который будет использоваться, если символ не может быть представлен на указанной кодовой странице.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-123">Pointer to the character to use if a character cannot be represented in the specified code page.</span></span>
    
 <span data-ttu-id="dc3d0-124">_лпфуседдефаултчар_</span><span class="sxs-lookup"><span data-stu-id="dc3d0-124">_lpfUsedDefaultChar_</span></span>
  
> <span data-ttu-id="dc3d0-125">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-125">[out] Optional.</span></span> <span data-ttu-id="dc3d0-126">Указатель на флаг, указывающий, использовался ли для функции символ по умолчанию в преобразовании.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-126">Pointer to a flag that indicates if the function has used a default character in the conversion.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dc3d0-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc3d0-127">Return value</span></span>

<span data-ttu-id="dc3d0-128">Возвращает число байтов, записанных в буфер, на который указывает _лпмултибитестр_ в случае успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="dc3d0-128">Returns the number of bytes written to the buffer pointed to by  _lpMultiByteStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dc3d0-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="dc3d0-129">Remarks</span></span>

<span data-ttu-id="dc3d0-130">Эта функция заключает в оболочку функцию **видечартомултибите** .</span><span class="sxs-lookup"><span data-stu-id="dc3d0-130">This function wraps the **WideCharToMultiByte** function.</span></span> <span data-ttu-id="dc3d0-131">Дополнительные сведения см. в разделе [видечартомултибите](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="dc3d0-131">For more information, see [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dc3d0-132">См. также</span><span class="sxs-lookup"><span data-stu-id="dc3d0-132">See also</span></span>



[<span data-ttu-id="dc3d0-133">видечартомултибите</span><span class="sxs-lookup"><span data-stu-id="dc3d0-133">WideCharToMultiByte</span></span>](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

