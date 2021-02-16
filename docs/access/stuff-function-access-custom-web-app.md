---
title: Функция Stuff (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Вставляет текстовую строку в другую текстовую строку. Он удаляет указанную длину символов в первой строке в начале, а затем вставляет вторую строку в первую строку в начале.
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427677"
---
# <a name="stuff-function-access-custom-web-app"></a><span data-ttu-id="e3884-104">Функция Stuff (пользовательское веб-приложение Access)</span><span class="sxs-lookup"><span data-stu-id="e3884-104">Stuff Function (Access custom web app)</span></span>

<span data-ttu-id="e3884-105">Вставляет текстовую строку в другую текстовую строку.</span><span class="sxs-lookup"><span data-stu-id="e3884-105">Inserts a text string into another text string.</span></span> <span data-ttu-id="e3884-106">Он удаляет указанную длину символов в первой строке в начале, а затем вставляет вторую строку в первую строку в начале.</span><span class="sxs-lookup"><span data-stu-id="e3884-106">It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e3884-107">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e3884-107">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="e3884-108">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="e3884-108">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e3884-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3884-109">Syntax</span></span>

 <span data-ttu-id="e3884-110">**Stuff** (*IntoTextExpression,* *Start*, *Length*, *ThisTextExpression*)</span><span class="sxs-lookup"><span data-stu-id="e3884-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span></span> 
  
<span data-ttu-id="e3884-111">Функция **Stuff** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="e3884-111">The **Stuff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="e3884-112">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="e3884-112">**Argument name**</span></span>|<span data-ttu-id="e3884-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e3884-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e3884-114">*IntoTextExpression*</span><span class="sxs-lookup"><span data-stu-id="e3884-114">*IntoTextExpression*</span></span>  <br/> |<span data-ttu-id="e3884-115">Текстовое выражение, которое указывает текст, в который будет вставлен текст, указанный *в ThisTextExpression.*</span><span class="sxs-lookup"><span data-stu-id="e3884-115">A text expression that specifies the text into which the text specified by the  *ThisTextExpression*  will be inserted.</span></span>  <br/> |
| <span data-ttu-id="e3884-116">*Начало*</span><span class="sxs-lookup"><span data-stu-id="e3884-116">*Start*</span></span>  <br/> |<span data-ttu-id="e3884-117">Это значение указывает расположение для начала удаления и вставки.</span><span class="sxs-lookup"><span data-stu-id="e3884-117">An integer value that specifies the location to start deletion and insertion.</span></span> <span data-ttu-id="e3884-118">Если начало или длина отрицательные, возвращается строка null.</span><span class="sxs-lookup"><span data-stu-id="e3884-118">If start or length is negative, a null string is returned.</span></span> <span data-ttu-id="e3884-119">Если начало больше, чем первый  *IntoTextExpression,*  возвращается строка null.</span><span class="sxs-lookup"><span data-stu-id="e3884-119">If start is longer than the first  *IntoTextExpression*  , a null string is returned.</span></span>  <br/> |
| <span data-ttu-id="e3884-120">*Length*</span><span class="sxs-lookup"><span data-stu-id="e3884-120">*Length*</span></span>  <br/> |<span data-ttu-id="e3884-121">Число, которое указывает количество удаляемого символа.</span><span class="sxs-lookup"><span data-stu-id="e3884-121">An integer that specifies the number of characters to delete.</span></span> <span data-ttu-id="e3884-122">Если длина превышает длину первого *intoTextExpression,* удаление происходит до последнего символа последнего *intoTextExpression.*</span><span class="sxs-lookup"><span data-stu-id="e3884-122">If length is longer than the first  *IntoTextExpression*  , deletion occurs up to the last character in the last  *IntoTextExpression*  .</span></span>  <br/> |
| <span data-ttu-id="e3884-123">*ThisTextExpression*</span><span class="sxs-lookup"><span data-stu-id="e3884-123">*ThisTextExpression*</span></span>  <br/> |<span data-ttu-id="e3884-124">Текстовое выражение определяет текст, вставляемый в *IntoTextExpression.*</span><span class="sxs-lookup"><span data-stu-id="e3884-124">A text expression hat specifies the text to insert into  *IntoTextExpression*  .</span></span> <span data-ttu-id="e3884-125">Это выражение заменит символы длины *IntoTextExpression, начиная* с *начала.*</span><span class="sxs-lookup"><span data-stu-id="e3884-125">This expression will replace length characters of  *IntoTextExpression*  beginning at  *Start*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3884-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="e3884-126">Remarks</span></span>

<span data-ttu-id="e3884-127">Если  *аргументы Start*  или  *Length*  отрицательные или если начальная позиция больше длины первой строки, возвращается нулевая строка.</span><span class="sxs-lookup"><span data-stu-id="e3884-127">If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned.</span></span> <span data-ttu-id="e3884-128">Если в начале 0, возвращается значение null.</span><span class="sxs-lookup"><span data-stu-id="e3884-128">If the start position is 0, a null value is returned.</span></span> <span data-ttu-id="e3884-129">Если длина, удаляемая, превышает длину первой строки, она удаляется для первого символа в первой строке.</span><span class="sxs-lookup"><span data-stu-id="e3884-129">If the length to delete is longer than the first string, it is deleted to the first character in the first string.</span></span> 
  

