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
description: Открывает файл HTML-справки с засвечиваемой ключевой фразой в поле Поиск.
ms.openlocfilehash: 639d10bf489d1ad09aef1522d3cbc743bbe66f6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431339"
---
# <a name="help-function"></a><span data-ttu-id="8cb03-103">Функция HELP</span><span class="sxs-lookup"><span data-stu-id="8cb03-103">HELP Function</span></span>

<span data-ttu-id="8cb03-104">Открывает файл HTML-справки с  засвечиваемой ключевой фразой в поле **Поиск.**</span><span class="sxs-lookup"><span data-stu-id="8cb03-104">Opens an HTML Help file with the specifed  *keyword*  in the **Search** box.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8cb03-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8cb03-105">Syntax</span></span>

<span data-ttu-id="8cb03-106">СПРАВКА(" \*\* *filename.chm!keyword* \*\* ")</span><span class="sxs-lookup"><span data-stu-id="8cb03-106">HELP(" \*\* *filename.chm!keyword* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8cb03-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8cb03-107">Parameters</span></span>

|<span data-ttu-id="8cb03-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8cb03-108">**Name**</span></span>|<span data-ttu-id="8cb03-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="8cb03-109">**Required/Optional**</span></span>|<span data-ttu-id="8cb03-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="8cb03-110">**Data Type**</span></span>|<span data-ttu-id="8cb03-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8cb03-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8cb03-112">_filename.chm!keyword_</span><span class="sxs-lookup"><span data-stu-id="8cb03-112">_filename.chm!keyword_</span></span> <br/> |<span data-ttu-id="8cb03-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8cb03-113">Required</span></span>  <br/> |<span data-ttu-id="8cb03-114">**String**</span><span class="sxs-lookup"><span data-stu-id="8cb03-114">**String**</span></span> <br/> | <span data-ttu-id="8cb03-115">Имя файла файла справки и ключевое слово для поиска.</span><span class="sxs-lookup"><span data-stu-id="8cb03-115">The filename of the Help file and the keyword to search for.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8cb03-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="8cb03-116">Remarks</span></span>

<span data-ttu-id="8cb03-117">Если  *ключевое*  слово не указано, функция HELP открывает страницу содержимого файла справки.</span><span class="sxs-lookup"><span data-stu-id="8cb03-117">If no  *keyword*  is specified, the HELP function opens the contents page of the Help file.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8cb03-118">Пример</span><span class="sxs-lookup"><span data-stu-id="8cb03-118">Example</span></span>

<span data-ttu-id="8cb03-119">HELP ("visio.chm!shapesheet")</span><span class="sxs-lookup"><span data-stu-id="8cb03-119">HELP("visio.chm!shapesheet")</span></span> 
  
<span data-ttu-id="8cb03-120">Открывает файл Visio справки и отображает список темы(ы), ключевое слово которой — "таблица форм".</span><span class="sxs-lookup"><span data-stu-id="8cb03-120">Opens the Visio Help file and displays a list of the topic(s) whose keyword is "shapesheet."</span></span> 
  

