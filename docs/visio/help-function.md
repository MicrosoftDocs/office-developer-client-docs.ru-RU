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
description: Открывает HTML-файл справки с указанным ключевым словом в поле поиска.
ms.openlocfilehash: 639d10bf489d1ad09aef1522d3cbc743bbe66f6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329976"
---
# <a name="help-function"></a><span data-ttu-id="ffbfb-103">Функция HELP</span><span class="sxs-lookup"><span data-stu-id="ffbfb-103">HELP Function</span></span>

<span data-ttu-id="ffbfb-104">Открывает HTML-файл справки с указанным *ключевым словом* в поле **поиска** .</span><span class="sxs-lookup"><span data-stu-id="ffbfb-104">Opens an HTML Help file with the specifed  *keyword*  in the **Search** box.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ffbfb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffbfb-105">Syntax</span></span>

<span data-ttu-id="ffbfb-106">Справка ("\* \* *имя_файла. chm! ключевое слово* \* \*")</span><span class="sxs-lookup"><span data-stu-id="ffbfb-106">HELP(" \*\* *filename.chm!keyword* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ffbfb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ffbfb-107">Parameters</span></span>

|<span data-ttu-id="ffbfb-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ffbfb-108">**Name**</span></span>|<span data-ttu-id="ffbfb-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="ffbfb-109">**Required/Optional**</span></span>|<span data-ttu-id="ffbfb-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ffbfb-110">**Data Type**</span></span>|<span data-ttu-id="ffbfb-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ffbfb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ffbfb-112">_filename. chm! ключевое слово_</span><span class="sxs-lookup"><span data-stu-id="ffbfb-112">_filename.chm!keyword_</span></span> <br/> |<span data-ttu-id="ffbfb-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ffbfb-113">Required</span></span>  <br/> |<span data-ttu-id="ffbfb-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ffbfb-114">**String**</span></span> <br/> | <span data-ttu-id="ffbfb-115">Имя файла справки и ключевое слово для поиска.</span><span class="sxs-lookup"><span data-stu-id="ffbfb-115">The filename of the Help file and the keyword to search for.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffbfb-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ffbfb-116">Remarks</span></span>

<span data-ttu-id="ffbfb-117">Если *ключевое слово* не указано, функция Help открывает страницу содержимое файла справки.</span><span class="sxs-lookup"><span data-stu-id="ffbfb-117">If no  *keyword*  is specified, the HELP function opens the contents page of the Help file.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ffbfb-118">Пример</span><span class="sxs-lookup"><span data-stu-id="ffbfb-118">Example</span></span>

<span data-ttu-id="ffbfb-119">Справка ("Visio. chm! для таблицы свойств фигуры")</span><span class="sxs-lookup"><span data-stu-id="ffbfb-119">HELP("visio.chm!shapesheet")</span></span> 
  
<span data-ttu-id="ffbfb-120">Открывает файл справки по Visio и отображает список разделов с ключевым словом "Таблица свойств фигуры".</span><span class="sxs-lookup"><span data-stu-id="ffbfb-120">Opens the Visio Help file and displays a list of the topic(s) whose keyword is "shapesheet."</span></span> 
  

