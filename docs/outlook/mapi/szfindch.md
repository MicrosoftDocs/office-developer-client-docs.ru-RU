---
title: SzFindCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindCh
api_type:
- COM
ms.assetid: 3406d060-bfea-4cea-8253-2a9aeb9e8147
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b517eaffa56001d8c414888ee6cbc8ec4f49cf66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812451"
---
# <a name="szfindch"></a><span data-ttu-id="06048-103">SzFindCh</span><span class="sxs-lookup"><span data-stu-id="06048-103">SzFindCh</span></span>
 
<span data-ttu-id="06048-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06048-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06048-105">Выполняет поиск первого вхождения знака в string символом null.</span><span class="sxs-lookup"><span data-stu-id="06048-105">Searches for the first occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06048-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="06048-106">Header file:</span></span>  <br/> |<span data-ttu-id="06048-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06048-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="06048-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="06048-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="06048-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="06048-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="06048-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="06048-110">Called by:</span></span>  <br/> |<span data-ttu-id="06048-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="06048-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="06048-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="06048-112">Parameters</span></span>

<span data-ttu-id="06048-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="06048-113">_lpsz_</span></span>
  
> <span data-ttu-id="06048-114">[in] Указатель на строку символом null для поиска.</span><span class="sxs-lookup"><span data-stu-id="06048-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
<span data-ttu-id="06048-115">_Кан_</span><span class="sxs-lookup"><span data-stu-id="06048-115">_ch_</span></span>
  
> <span data-ttu-id="06048-116">[in] Знак для поиска.</span><span class="sxs-lookup"><span data-stu-id="06048-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="06048-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="06048-117">Return value</span></span>

<span data-ttu-id="06048-118">**SzFindCh** возвращает указатель на первого появления знаков в строке.</span><span class="sxs-lookup"><span data-stu-id="06048-118">**SzFindCh** returns a pointer to the first occurrence of the character in the string.</span></span> <span data-ttu-id="06048-119">Если кодировка не происходит в любом месте в строке или параметр _lpsz_ имеет значение NULL, возвращается значение NULL.</span><span class="sxs-lookup"><span data-stu-id="06048-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="06048-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="06048-120">Remarks</span></span>

<span data-ttu-id="06048-121">Функция **SzFindCh** выполняется поиск точного совпадения. Это зависит от регистра и диакритических различия.</span><span class="sxs-lookup"><span data-stu-id="06048-121">The **SzFindCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="06048-122">Поиск в формате Юникод и DBCS поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="06048-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

