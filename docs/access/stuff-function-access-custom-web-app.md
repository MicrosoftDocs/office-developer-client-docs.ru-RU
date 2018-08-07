---
title: Функция (en) (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Вставляет строку текста в другую текстовую строку. Его удаляет указанное количество символов в первой строке в положении начала и вставляет вторую строку в первой строки в начальной позиции.
ms.openlocfilehash: 5540bb5936803370835a0c3d80b420edc13d0de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807117"
---
# <a name="stuff-function-access-custom-web-app"></a><span data-ttu-id="be27f-104">Функция (en) (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="be27f-104">Stuff Function (Access custom web app)</span></span>

<span data-ttu-id="be27f-105">Вставляет строку текста в другую текстовую строку.</span><span class="sxs-lookup"><span data-stu-id="be27f-105">Inserts a text string into another text string.</span></span> <span data-ttu-id="be27f-106">Его удаляет указанное количество символов в первой строке в положении начала и вставляет вторую строку в первой строки в начальной позиции.</span><span class="sxs-lookup"><span data-stu-id="be27f-106">It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="be27f-107">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="be27f-107">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="be27f-108">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="be27f-108">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="be27f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be27f-109">Syntax</span></span>

 <span data-ttu-id="be27f-110">**(En)** (*IntoTextExpression*, *запустите*, *длины*, *ThisTextExpression*)</span><span class="sxs-lookup"><span data-stu-id="be27f-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span></span> 
  
<span data-ttu-id="be27f-111">Функция **(en)** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="be27f-111">The **Stuff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="be27f-112">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="be27f-112">**Argument name**</span></span>|<span data-ttu-id="be27f-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="be27f-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="be27f-114">*IntoTextExpression*</span><span class="sxs-lookup"><span data-stu-id="be27f-114">*IntoTextExpression*</span></span>  <br/> |<span data-ttu-id="be27f-115">Выражение текст, текст, в котором будет вставлен текст, заданный параметром *ThisTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="be27f-115">A text expression that specifies the text into which the text specified by the  *ThisTextExpression*  will be inserted.</span></span>  <br/> |
| <span data-ttu-id="be27f-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="be27f-116">*Start*</span></span>  <br/> |<span data-ttu-id="be27f-117">Целое число, указывающее место начала удаления и вставки.</span><span class="sxs-lookup"><span data-stu-id="be27f-117">An integer value that specifies the location to start deletion and insertion.</span></span> <span data-ttu-id="be27f-118">Если запустить или длина отрицательно, возвращается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="be27f-118">If start or length is negative, a null string is returned.</span></span> <span data-ttu-id="be27f-119">Если запустить длиннее первого *IntoTextExpression* , возвращается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="be27f-119">If start is longer than the first  *IntoTextExpression*  , a null string is returned.</span></span>  <br/> |
| <span data-ttu-id="be27f-120">*Длина*</span><span class="sxs-lookup"><span data-stu-id="be27f-120">*Length*</span></span>  <br/> |<span data-ttu-id="be27f-121">Целое число, указывающее число символов для удаления.</span><span class="sxs-lookup"><span data-stu-id="be27f-121">An integer that specifies the number of characters to delete.</span></span> <span data-ttu-id="be27f-122">Если длина длиннее первого *IntoTextExpression* , удаление выполняется до последнего символа в последней *IntoTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="be27f-122">If length is longer than the first  *IntoTextExpression*  , deletion occurs up to the last character in the last  *IntoTextExpression*  .</span></span>  <br/> |
| <span data-ttu-id="be27f-123">*ThisTextExpression*</span><span class="sxs-lookup"><span data-stu-id="be27f-123">*ThisTextExpression*</span></span>  <br/> |<span data-ttu-id="be27f-124">Шапка выражение текст текст для вставки в *IntoTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="be27f-124">A text expression hat specifies the text to insert into  *IntoTextExpression*  .</span></span> <span data-ttu-id="be27f-125">Это выражение заменит длина символов *IntoTextExpression* , начиная с *запуска* .</span><span class="sxs-lookup"><span data-stu-id="be27f-125">This expression will replace length characters of  *IntoTextExpression*  beginning at  *Start*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be27f-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="be27f-126">Remarks</span></span>

<span data-ttu-id="be27f-127">Если *запустить* или *Длина* аргументов отрицательные или позицию больше, чем длина первой строки, возвращается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="be27f-127">If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned.</span></span> <span data-ttu-id="be27f-128">Если начальное положение равно 0, возвращается значение null.</span><span class="sxs-lookup"><span data-stu-id="be27f-128">If the start position is 0, a null value is returned.</span></span> <span data-ttu-id="be27f-129">Если длина удаление содержит более первой строки, она удаляется первый символ в первой строке.</span><span class="sxs-lookup"><span data-stu-id="be27f-129">If the length to delete is longer than the first string, it is deleted to the first character in the first string.</span></span> 
  

