---
title: Функция "Прочее" (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Вставляет текстовую строку в другую текстовую строку. Он удаляет указанную длину символов в первой строке в начальной позиции и вставляет вторую строку в первую строку в начальной позиции.
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311027"
---
# <a name="stuff-function-access-custom-web-app"></a><span data-ttu-id="bdaac-104">Функция "Прочее" (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="bdaac-104">Stuff Function (Access custom web app)</span></span>

<span data-ttu-id="bdaac-105">Вставляет текстовую строку в другую текстовую строку.</span><span class="sxs-lookup"><span data-stu-id="bdaac-105">Inserts a text string into another text string.</span></span> <span data-ttu-id="bdaac-106">Он удаляет указанную длину символов в первой строке в начальной позиции и вставляет вторую строку в первую строку в начальной позиции.</span><span class="sxs-lookup"><span data-stu-id="bdaac-106">It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="bdaac-107">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="bdaac-107">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="bdaac-108">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="bdaac-108">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bdaac-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bdaac-109">Syntax</span></span>

 <span data-ttu-id="bdaac-110">**Материалы** (*Интотекстекспрессион*, *Start*, *length*, *систекстекспрессион*)</span><span class="sxs-lookup"><span data-stu-id="bdaac-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span></span> 
  
<span data-ttu-id="bdaac-111">Функция \*\*\*\* сведения содержит указанные ниже аргументы.</span><span class="sxs-lookup"><span data-stu-id="bdaac-111">The **Stuff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="bdaac-112">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="bdaac-112">**Argument name**</span></span>|<span data-ttu-id="bdaac-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bdaac-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bdaac-114">*Интотекстекспрессион*</span><span class="sxs-lookup"><span data-stu-id="bdaac-114">*IntoTextExpression*</span></span>  <br/> |<span data-ttu-id="bdaac-115">Текстовое выражение, задающее текст, в который будет вставлен текст, заданный параметром *систекстекспрессион* .</span><span class="sxs-lookup"><span data-stu-id="bdaac-115">A text expression that specifies the text into which the text specified by the  *ThisTextExpression*  will be inserted.</span></span>  <br/> |
| <span data-ttu-id="bdaac-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="bdaac-116">*Start*</span></span>  <br/> |<span data-ttu-id="bdaac-117">Целое значение, задающее расположение для начала удаления и вставки.</span><span class="sxs-lookup"><span data-stu-id="bdaac-117">An integer value that specifies the location to start deletion and insertion.</span></span> <span data-ttu-id="bdaac-118">Если значение Start или length отрицательно, возвращается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="bdaac-118">If start or length is negative, a null string is returned.</span></span> <span data-ttu-id="bdaac-119">Если Start длиннее первого *интотекстекспрессион* , возвращается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="bdaac-119">If start is longer than the first  *IntoTextExpression*  , a null string is returned.</span></span>  <br/> |
| <span data-ttu-id="bdaac-120">*Length*</span><span class="sxs-lookup"><span data-stu-id="bdaac-120">*Length*</span></span>  <br/> |<span data-ttu-id="bdaac-121">Целое число, определяющее количество удаляемых символов.</span><span class="sxs-lookup"><span data-stu-id="bdaac-121">An integer that specifies the number of characters to delete.</span></span> <span data-ttu-id="bdaac-122">Если длина превышает первый *интотекстекспрессион* , удаление происходит до последнего символа в последнем *интотекстекспрессион* .</span><span class="sxs-lookup"><span data-stu-id="bdaac-122">If length is longer than the first  *IntoTextExpression*  , deletion occurs up to the last character in the last  *IntoTextExpression*  .</span></span>  <br/> |
| <span data-ttu-id="bdaac-123">*Систекстекспрессион*</span><span class="sxs-lookup"><span data-stu-id="bdaac-123">*ThisTextExpression*</span></span>  <br/> |<span data-ttu-id="bdaac-124">Текстовое выражение Hat указывает текст, который необходимо вставить в *интотекстекспрессион* .</span><span class="sxs-lookup"><span data-stu-id="bdaac-124">A text expression hat specifies the text to insert into  *IntoTextExpression*  .</span></span> <span data-ttu-id="bdaac-125">Это выражение заменит длину символов *интотекстекспрессион* , начиная с *Start* .</span><span class="sxs-lookup"><span data-stu-id="bdaac-125">This expression will replace length characters of  *IntoTextExpression*  beginning at  *Start*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bdaac-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="bdaac-126">Remarks</span></span>

<span data-ttu-id="bdaac-127">Если аргументы *начала* или *длины* отрицательны или если начальная позиция превышает длину первой строки, возвращается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="bdaac-127">If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned.</span></span> <span data-ttu-id="bdaac-128">Если начальная позиция равна 0, возвращается значение null.</span><span class="sxs-lookup"><span data-stu-id="bdaac-128">If the start position is 0, a null value is returned.</span></span> <span data-ttu-id="bdaac-129">Если длина, которую требуется удалить, больше, чем первая строка, она будет удалена до первого символа в первой строке.</span><span class="sxs-lookup"><span data-stu-id="bdaac-129">If the length to delete is longer than the first string, it is deleted to the first character in the first string.</span></span> 
  

