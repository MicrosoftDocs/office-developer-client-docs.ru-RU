---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Дата последнего изменения: 21 февраля 2012 г.'
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338243"
---
# <a name="mnlsmultibytetowidechar"></a><span data-ttu-id="7e30f-103">MNLS_MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="7e30f-103">MNLS_MultiByteToWideChar</span></span>

  
  
<span data-ttu-id="7e30f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e30f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e30f-105">Аналогичен **мултибитетовидечар**, который сопоставляет строку символов со строкой UTF-16 (Wide знака).</span><span class="sxs-lookup"><span data-stu-id="7e30f-105">Similar to **MultiByteToWideChar**, which maps a character string to a UTF-16 (wide character) string.</span></span> <span data-ttu-id="7e30f-106">Строка символов не обязательно должна находиться в многобайтовой кодировке.</span><span class="sxs-lookup"><span data-stu-id="7e30f-106">The character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a><span data-ttu-id="7e30f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e30f-107">Parameters</span></span>

 <span data-ttu-id="7e30f-108">_Укодепаже_</span><span class="sxs-lookup"><span data-stu-id="7e30f-108">_uCodePage_</span></span>
  
> <span data-ttu-id="7e30f-109">возврата Кодовая страница, используемая для выполнения преобразования.</span><span class="sxs-lookup"><span data-stu-id="7e30f-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="7e30f-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="7e30f-110">_dwFlags_</span></span>
  
> <span data-ttu-id="7e30f-111">возврата Флаги, указывающие тип преобразования.</span><span class="sxs-lookup"><span data-stu-id="7e30f-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="7e30f-112">_Лпмултибитестр_</span><span class="sxs-lookup"><span data-stu-id="7e30f-112">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="7e30f-113">возврата Указатель на строку символов для преобразования.</span><span class="sxs-lookup"><span data-stu-id="7e30f-113">[in] Pointer to the character string to convert.</span></span>
    
 <span data-ttu-id="7e30f-114">_Кчмултибите_</span><span class="sxs-lookup"><span data-stu-id="7e30f-114">_cchMultiByte_</span></span>
  
> <span data-ttu-id="7e30f-115">возврата Размер (в байтах) строки, указанной параметром _лпмултибитестр_ .</span><span class="sxs-lookup"><span data-stu-id="7e30f-115">[in] Size, in bytes, of the string indicated by the  _lpMultiByteStr_ parameter.</span></span> 
    
 <span data-ttu-id="7e30f-116">_Лпвидечарстр_</span><span class="sxs-lookup"><span data-stu-id="7e30f-116">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="7e30f-117">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="7e30f-117">[out] Optional.</span></span> <span data-ttu-id="7e30f-118">Указатель на буфер, который получает преобразованную строку.</span><span class="sxs-lookup"><span data-stu-id="7e30f-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="7e30f-119">_Кчвидечар_</span><span class="sxs-lookup"><span data-stu-id="7e30f-119">_cchWideChar_</span></span>
  
> <span data-ttu-id="7e30f-120">возврата Размер буфера в символах, указанный в _лпвидечарстр_.</span><span class="sxs-lookup"><span data-stu-id="7e30f-120">[in] Size, in characters, of the buffer indicated by  _lpWideCharStr_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7e30f-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e30f-121">Return value</span></span>

<span data-ttu-id="7e30f-122">Возвращает число символов, записанных в буфер, указанный в _лпвидечарстр_ в случае успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="7e30f-122">Returns the number of characters written to the buffer indicated by  _lpWideCharStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7e30f-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e30f-123">Remarks</span></span>

<span data-ttu-id="7e30f-124">Эта функция заключает в оболочку функцию **мултибитетовидечар** .</span><span class="sxs-lookup"><span data-stu-id="7e30f-124">This function wraps the **MultiByteToWideChar** function.</span></span> <span data-ttu-id="7e30f-125">Дополнительные сведения см. в разделе [мултибитетовидечар](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7e30f-125">For more information, see [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).</span></span>
  

