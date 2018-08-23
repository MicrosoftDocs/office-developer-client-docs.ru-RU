---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Последнее изменение: 21 февраля 2012 г.'
ms.openlocfilehash: 6957888f6727175d73d277cf4f5b84dc234d22ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570039"
---
# <a name="mnlswidechartomultibyte"></a><span data-ttu-id="1a9fb-103">MNLS_WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="1a9fb-103">MNLS_WideCharToMultiByte</span></span>

  
  
<span data-ttu-id="1a9fb-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a9fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a9fb-105">Эта функция аналогична **WideCharToMultiByte**, которая соответствует строка UTF-16 (двухбайтовых знаков) новую строку знаков.</span><span class="sxs-lookup"><span data-stu-id="1a9fb-105">This function is similar to **WideCharToMultiByte**, which maps a UTF-16 (wide character) string to a new character string.</span></span> <span data-ttu-id="1a9fb-106">Создать строку знаков не обязательно из многобайтовой задан.</span><span class="sxs-lookup"><span data-stu-id="1a9fb-106">The new character string is not necessarily from a multibyte character set.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="1a9fb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a9fb-107">Parameters</span></span>

 <span data-ttu-id="1a9fb-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="1a9fb-108">_uCodePage_</span></span>
  
> <span data-ttu-id="1a9fb-109">[in] Кодовая страница следует использовать при выполнении преобразования.</span><span class="sxs-lookup"><span data-stu-id="1a9fb-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="1a9fb-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="1a9fb-110">_dwFlags_</span></span>
  
> <span data-ttu-id="1a9fb-111">[in] Флаги, указывающее тип преобразования.</span><span class="sxs-lookup"><span data-stu-id="1a9fb-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="1a9fb-112">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="1a9fb-112">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="1a9fb-113">[in] Указатель на строку Юникод для преобразования.</span><span class="sxs-lookup"><span data-stu-id="1a9fb-113">[in] Pointer to the Unicode string to convert.</span></span>
    
 <span data-ttu-id="1a9fb-114">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="1a9fb-114">_cchWideChar_</span></span>
  
> <span data-ttu-id="1a9fb-115">[in] Флаги, указывающее тип преобразования.</span><span class="sxs-lookup"><span data-stu-id="1a9fb-115">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="1a9fb-116">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="1a9fb-116">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="1a9fb-117">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="1a9fb-117">[out] Optional.</span></span> <span data-ttu-id="1a9fb-118">Указатель на буфер, получающий Преобразованная строка.</span><span class="sxs-lookup"><span data-stu-id="1a9fb-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="1a9fb-119">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="1a9fb-119">_cchMultiByte_</span></span>
  
> <span data-ttu-id="1a9fb-120">[in] Размер, в байтах, указанный в параметре _lpMultiByteStr_буфера.</span><span class="sxs-lookup"><span data-stu-id="1a9fb-120">[in] Size, in bytes, of the buffer indicated by  _lpMultiByteStr_.</span></span>
    
 <span data-ttu-id="1a9fb-121">_lpDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="1a9fb-121">_lpDefaultChar_</span></span>
  
> <span data-ttu-id="1a9fb-122">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="1a9fb-122">[in] Optional.</span></span> <span data-ttu-id="1a9fb-123">Указатель на символ для использования, если указанная кодовая страница не может быть представлена знак.</span><span class="sxs-lookup"><span data-stu-id="1a9fb-123">Pointer to the character to use if a character cannot be represented in the specified code page.</span></span>
    
 <span data-ttu-id="1a9fb-124">_lpfUsedDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="1a9fb-124">_lpfUsedDefaultChar_</span></span>
  
> <span data-ttu-id="1a9fb-125">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="1a9fb-125">[out] Optional.</span></span> <span data-ttu-id="1a9fb-126">Указатель на флаг, указывающий, если функция использовал знаков по умолчанию для преобразования.</span><span class="sxs-lookup"><span data-stu-id="1a9fb-126">Pointer to a flag that indicates if the function has used a default character in the conversion.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1a9fb-127">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="1a9fb-127">Return value</span></span>

<span data-ttu-id="1a9fb-128">Возвращает число байт, записанных в буфере, _lpMultiByteStr_ в случае успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="1a9fb-128">Returns the number of bytes written to the buffer pointed to by  _lpMultiByteStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1a9fb-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="1a9fb-129">Remarks</span></span>

<span data-ttu-id="1a9fb-130">Эта функция является функция **WideCharToMultiByte** .</span><span class="sxs-lookup"><span data-stu-id="1a9fb-130">This function wraps the **WideCharToMultiByte** function.</span></span> <span data-ttu-id="1a9fb-131">Для получения дополнительных сведений см [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1a9fb-131">For more information, see [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1a9fb-132">См. также</span><span class="sxs-lookup"><span data-stu-id="1a9fb-132">See also</span></span>



[<span data-ttu-id="1a9fb-133">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="1a9fb-133">WideCharToMultiByte</span></span>](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx)

