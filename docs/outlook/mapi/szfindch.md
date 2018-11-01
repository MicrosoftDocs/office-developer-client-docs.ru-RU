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
ms.openlocfilehash: 8426f782eb5fbf8a125833c51b25ccd605acbd64
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573525"
---
# <a name="szfindch"></a><span data-ttu-id="f7fb1-103">SzFindCh</span><span class="sxs-lookup"><span data-stu-id="f7fb1-103">SzFindCh</span></span>
 
<span data-ttu-id="f7fb1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7fb1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7fb1-105">Выполняет поиск первого вхождения знака в string символом null.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-105">Searches for the first occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7fb1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f7fb1-106">Header file:</span></span>  <br/> |<span data-ttu-id="f7fb1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7fb1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f7fb1-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="f7fb1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f7fb1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f7fb1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f7fb1-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="f7fb1-110">Called by:</span></span>  <br/> |<span data-ttu-id="f7fb1-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="f7fb1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="f7fb1-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7fb1-112">Parameters</span></span>

<span data-ttu-id="f7fb1-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="f7fb1-113">_lpsz_</span></span>
  
> <span data-ttu-id="f7fb1-114">[in] Указатель на строку символом null для поиска.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
<span data-ttu-id="f7fb1-115">_Кан_</span><span class="sxs-lookup"><span data-stu-id="f7fb1-115">_ch_</span></span>
  
> <span data-ttu-id="f7fb1-116">[in] Знак для поиска.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f7fb1-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7fb1-117">Return value</span></span>

<span data-ttu-id="f7fb1-118">**SzFindCh** возвращает указатель на первого появления знаков в строке.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-118">**SzFindCh** returns a pointer to the first occurrence of the character in the string.</span></span> <span data-ttu-id="f7fb1-119">Если кодировка не происходит в любом месте в строке или параметр _lpsz_ имеет значение NULL, возвращается значение NULL.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f7fb1-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="f7fb1-120">Remarks</span></span>

<span data-ttu-id="f7fb1-121">Функция **SzFindCh** выполняется поиск точного совпадения. Это зависит от регистра и диакритических различия.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-121">The **SzFindCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="f7fb1-122">Поиск в формате Юникод и DBCS поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

