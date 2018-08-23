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
ms.openlocfilehash: 66e8c3b61caac6fb8d8b57d74ade6fa8aac3a9dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571709"
---
# <a name="mnlsmultibytetowidechar"></a><span data-ttu-id="8c73b-103">MNLS_MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="8c73b-103">MNLS_MultiByteToWideChar</span></span>

  
  
<span data-ttu-id="8c73b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c73b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c73b-105">Аналогично **MultiByteToWideChar**, которая соответствует строка символов строки UTF-16 (двухбайтовых знаков).</span><span class="sxs-lookup"><span data-stu-id="8c73b-105">Similar to **MultiByteToWideChar**, which maps a character string to a UTF-16 (wide character) string.</span></span> <span data-ttu-id="8c73b-106">Строку знаков не обязательно из многобайтовой задан.</span><span class="sxs-lookup"><span data-stu-id="8c73b-106">The character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a><span data-ttu-id="8c73b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c73b-107">Parameters</span></span>

 <span data-ttu-id="8c73b-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="8c73b-108">_uCodePage_</span></span>
  
> <span data-ttu-id="8c73b-109">[in] Кодовая страница следует использовать при выполнении преобразования.</span><span class="sxs-lookup"><span data-stu-id="8c73b-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="8c73b-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="8c73b-110">_dwFlags_</span></span>
  
> <span data-ttu-id="8c73b-111">[in] Флаги, указывающее тип преобразования.</span><span class="sxs-lookup"><span data-stu-id="8c73b-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="8c73b-112">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="8c73b-112">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="8c73b-113">[in] Указатель на строку знаков для преобразования.</span><span class="sxs-lookup"><span data-stu-id="8c73b-113">[in] Pointer to the character string to convert.</span></span>
    
 <span data-ttu-id="8c73b-114">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="8c73b-114">_cchMultiByte_</span></span>
  
> <span data-ttu-id="8c73b-115">[in] Размер, в байтах, указанное с помощью параметра _lpMultiByteStr_ строки.</span><span class="sxs-lookup"><span data-stu-id="8c73b-115">[in] Size, in bytes, of the string indicated by the  _lpMultiByteStr_ parameter.</span></span> 
    
 <span data-ttu-id="8c73b-116">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="8c73b-116">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="8c73b-117">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="8c73b-117">[out] Optional.</span></span> <span data-ttu-id="8c73b-118">Указатель на буфер, получающий Преобразованная строка.</span><span class="sxs-lookup"><span data-stu-id="8c73b-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="8c73b-119">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="8c73b-119">_cchWideChar_</span></span>
  
> <span data-ttu-id="8c73b-120">[in] Размер в знаков, указанный в параметре _lpWideCharStr_буфера.</span><span class="sxs-lookup"><span data-stu-id="8c73b-120">[in] Size, in characters, of the buffer indicated by  _lpWideCharStr_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8c73b-121">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="8c73b-121">Return value</span></span>

<span data-ttu-id="8c73b-122">Возвращает число знаков в буфер, указанный в параметре _lpWideCharStr_ в случае успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="8c73b-122">Returns the number of characters written to the buffer indicated by  _lpWideCharStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8c73b-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="8c73b-123">Remarks</span></span>

<span data-ttu-id="8c73b-124">Эта функция имеет функцию **MultiByteToWideChar** .</span><span class="sxs-lookup"><span data-stu-id="8c73b-124">This function wraps the **MultiByteToWideChar** function.</span></span> <span data-ttu-id="8c73b-125">Для получения дополнительных сведений см [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/dd319072%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8c73b-125">For more information, see [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/dd319072%28VS.85%29.aspx).</span></span>
  

