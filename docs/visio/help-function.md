---
title: Функция HELP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251436
localization_priority: Normal
ms.assetid: 5b358c38-6ed1-3fbe-c1d1-1a56ebbaa870
description: Открывает файл HTML-справки с ключевым словом указан в поле «Поиск».
ms.openlocfilehash: 4671b18333bdae953c487662cd880849233df7f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813899"
---
# <a name="help-function"></a><span data-ttu-id="44dd7-103">Функция HELP</span><span class="sxs-lookup"><span data-stu-id="44dd7-103">HELP Function</span></span>

<span data-ttu-id="44dd7-104">Открывает файл HTML-справки с указанной *ключевое слово* в поле « **Поиск** ».</span><span class="sxs-lookup"><span data-stu-id="44dd7-104">Opens an HTML Help file with the specifed  *keyword*  in the **Search** box.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="44dd7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44dd7-105">Syntax</span></span>

<span data-ttu-id="44dd7-106">СПРАВКА ("** *filename.chm!keyword* **")</span><span class="sxs-lookup"><span data-stu-id="44dd7-106">HELP(" ** *filename.chm!keyword* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="44dd7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="44dd7-107">Parameters</span></span>

|<span data-ttu-id="44dd7-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="44dd7-108">**Name**</span></span>|<span data-ttu-id="44dd7-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="44dd7-109">**Required/Optional**</span></span>|<span data-ttu-id="44dd7-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="44dd7-110">**Data Type**</span></span>|<span data-ttu-id="44dd7-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="44dd7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="44dd7-112">_filename.chm!Keyword_</span><span class="sxs-lookup"><span data-stu-id="44dd7-112">_filename.chm!keyword_</span></span> <br/> |<span data-ttu-id="44dd7-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="44dd7-113">Required</span></span>  <br/> |<span data-ttu-id="44dd7-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="44dd7-114">**String**</span></span> <br/> | <span data-ttu-id="44dd7-115">Имя файла файл справки и ключевое слово для поиска.</span><span class="sxs-lookup"><span data-stu-id="44dd7-115">The filename of the Help file and the keyword to search for.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44dd7-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="44dd7-116">Remarks</span></span>

<span data-ttu-id="44dd7-117">Если нет *ключевых слов* не указан, то функция справки открывает страницу содержимое файла справки.</span><span class="sxs-lookup"><span data-stu-id="44dd7-117">If no  *keyword*  is specified, the HELP function opens the contents page of the Help file.</span></span> 
  
## <a name="example"></a><span data-ttu-id="44dd7-118">Пример</span><span class="sxs-lookup"><span data-stu-id="44dd7-118">Example</span></span>

<span data-ttu-id="44dd7-119">Help("Visio.chm!ShapeSheet")</span><span class="sxs-lookup"><span data-stu-id="44dd7-119">HELP("visio.chm!shapesheet")</span></span> 
  
<span data-ttu-id="44dd7-120">Открывает файл справки Visio и отображает список помеченным, чьи ключевое слово является «фигуры».</span><span class="sxs-lookup"><span data-stu-id="44dd7-120">Opens the Visio Help file and displays a list of the topic(s) whose keyword is "shapesheet."</span></span> 
  

