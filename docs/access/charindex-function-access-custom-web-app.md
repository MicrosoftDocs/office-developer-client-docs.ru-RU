---
title: Функция CharIndex (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Поиск выражения текст для другого выражения текста и возвращает его запуск позиция, если найти.
ms.openlocfilehash: 86a46f57c64028530217326127eece887127c4c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806968"
---
# <a name="charindex-function-access-custom-web-app"></a><span data-ttu-id="62fb8-103">Функция CharIndex (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="62fb8-103">CharIndex function (Access custom web app)</span></span>

<span data-ttu-id="62fb8-104">Поиск выражения текст для другого выражения текста и возвращает его запуск позиция, если найти.</span><span class="sxs-lookup"><span data-stu-id="62fb8-104">Searches a text expression for another text expression and returns its starting position if found.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="62fb8-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="62fb8-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="62fb8-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="62fb8-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="62fb8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62fb8-107">Syntax</span></span>

<span data-ttu-id="62fb8-108">**CharIndex** (*TextExpression*, *WithinText*[*Пуск*])</span><span class="sxs-lookup"><span data-stu-id="62fb8-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span></span> 
  
|<span data-ttu-id="62fb8-109">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="62fb8-109">**Argument Name**</span></span>|<span data-ttu-id="62fb8-110">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="62fb8-110">**Required**</span></span>|<span data-ttu-id="62fb8-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="62fb8-111">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="62fb8-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="62fb8-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="62fb8-113">Да</span><span class="sxs-lookup"><span data-stu-id="62fb8-113">Yes</span></span>  <br/> |<span data-ttu-id="62fb8-114">Выражение текст, который содержит текст для поиска.</span><span class="sxs-lookup"><span data-stu-id="62fb8-114">A text expression that contains the text to be found.</span></span>  <br/> |
| <span data-ttu-id="62fb8-115">*WithinText*</span><span class="sxs-lookup"><span data-stu-id="62fb8-115">*WithinText*</span></span>  <br/> |<span data-ttu-id="62fb8-116">Да</span><span class="sxs-lookup"><span data-stu-id="62fb8-116">Yes</span></span>  <br/> |<span data-ttu-id="62fb8-117">Выражения текст для поиска.</span><span class="sxs-lookup"><span data-stu-id="62fb8-117">The text expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="62fb8-118">*Start*</span><span class="sxs-lookup"><span data-stu-id="62fb8-118">*Start*</span></span>  <br/> |<span data-ttu-id="62fb8-119">Нет</span><span class="sxs-lookup"><span data-stu-id="62fb8-119">No</span></span>  <br/> |<span data-ttu-id="62fb8-120">Целое число, задающее расположение в *WithinText* , чтобы начать поиск.</span><span class="sxs-lookup"><span data-stu-id="62fb8-120">An integer that specifies the location in  *WithinText*  to begin the search.</span></span> <span data-ttu-id="62fb8-121">Если *запустить* не указан, имеет отрицательное значение или равен 0, поиск начинается в начале *WithinText* .</span><span class="sxs-lookup"><span data-stu-id="62fb8-121">If  *Start*  is not specified, is a negative number, or is 0, the search starts at the beginning of  *WithinText*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62fb8-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="62fb8-122">Remarks</span></span>

<span data-ttu-id="62fb8-123">Если *TextExpression* или *WithinText* имеет значение NULL, *CharIndex* возвращает NULL.</span><span class="sxs-lookup"><span data-stu-id="62fb8-123">If either  *TextExpression*  or  *WithinText*  is NULL,  *CharIndex*  returns NULL.</span></span> 
  
<span data-ttu-id="62fb8-124">Если *TextExpression* не найден в *WithinText*, *CharIndex* возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="62fb8-124">If  *TextExpression*  is not found within  *WithinText*,  *CharIndex*  returns 0.</span></span> 
  
<span data-ttu-id="62fb8-125">Позицию возвращаемой 1, а не от нуля.</span><span class="sxs-lookup"><span data-stu-id="62fb8-125">The starting position returned is 1-based, not 0-based.</span></span>
  

