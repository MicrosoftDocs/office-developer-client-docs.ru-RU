---
title: Функция PLAYSOUND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251479
localization_priority: Normal
ms.assetid: 098d216f-e699-0e74-f702-ccfa7809c19b
description: Воспроизводит звуковой файл или системный звук.
ms.openlocfilehash: 752412aab6584d2b01235fe88644e3ec3fa5daee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435841"
---
# <a name="playsound-function"></a><span data-ttu-id="ef3c7-103">Функция PLAYSOUND</span><span class="sxs-lookup"><span data-stu-id="ef3c7-103">PLAYSOUND Function</span></span>

<span data-ttu-id="ef3c7-104">Воспроизводит звуковой файл или системный звук.</span><span class="sxs-lookup"><span data-stu-id="ef3c7-104">Plays a sound file or system sound.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ef3c7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef3c7-105">Syntax</span></span>

<span data-ttu-id="ef3c7-106">PLAYSOUND(" \*\* *filename* \*\* "|" \*\* *alias* \*\* ", \*\* *isAlias* \*\*, \*\* *beep* \*\*, \*\* *synch* \*\* )</span><span class="sxs-lookup"><span data-stu-id="ef3c7-106">PLAYSOUND(" \*\* *filename* \*\* "|" \*\* *alias* \*\* ", \*\* *isAlias* \*\*, \*\* *beep* \*\*, \*\* *synch* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ef3c7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef3c7-107">Parameters</span></span>

|<span data-ttu-id="ef3c7-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ef3c7-108">**Name**</span></span>|<span data-ttu-id="ef3c7-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="ef3c7-109">**Required/Optional**</span></span>|<span data-ttu-id="ef3c7-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ef3c7-110">**Data Type**</span></span>|<span data-ttu-id="ef3c7-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ef3c7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ef3c7-112">_filename_</span><span class="sxs-lookup"><span data-stu-id="ef3c7-112">_filename_</span></span> <br/> |<span data-ttu-id="ef3c7-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="ef3c7-113">Required</span></span>  <br/> |<span data-ttu-id="ef3c7-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="ef3c7-114">**String**</span></span> <br/> |<span data-ttu-id="ef3c7-115">Имя звукового файла, который вы хотите воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ef3c7-115">The name of the sound file you want to play.</span></span>  <br/> |
| <span data-ttu-id="ef3c7-116">_alias_</span><span class="sxs-lookup"><span data-stu-id="ef3c7-116">_alias_</span></span> <br/> |<span data-ttu-id="ef3c7-117">Обязательно</span><span class="sxs-lookup"><span data-stu-id="ef3c7-117">Required</span></span>  <br/> |<span data-ttu-id="ef3c7-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="ef3c7-118">**String**</span></span> <br/> | <span data-ttu-id="ef3c7-119">Системный звук, представленный псевдонимом.</span><span class="sxs-lookup"><span data-stu-id="ef3c7-119">A system sound represented by an alias.</span></span>  <br/> |
| <span data-ttu-id="ef3c7-120">_isAlias_</span><span class="sxs-lookup"><span data-stu-id="ef3c7-120">_isAlias_</span></span> <br/> |<span data-ttu-id="ef3c7-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ef3c7-121">Required</span></span>  <br/> |<span data-ttu-id="ef3c7-122">**Логический**</span><span class="sxs-lookup"><span data-stu-id="ef3c7-122">**Boolean**</span></span> <br/> | <span data-ttu-id="ef3c7-123">Указывает, является ли предыдущее выражение псевдонимом или именем файла; для указания псевдонима используйте ненулевую величину.</span><span class="sxs-lookup"><span data-stu-id="ef3c7-123">Specifies whether the preceding expression is an alias or file name; use a non-zero value to specify an alias.</span></span>  <br/> |
| <span data-ttu-id="ef3c7-124">_beep_</span><span class="sxs-lookup"><span data-stu-id="ef3c7-124">_beep_</span></span> <br/> |<span data-ttu-id="ef3c7-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ef3c7-125">Required</span></span>  <br/> |<span data-ttu-id="ef3c7-126">**Логический**</span><span class="sxs-lookup"><span data-stu-id="ef3c7-126">**Boolean**</span></span> <br/> |<span data-ttu-id="ef3c7-127">Указывает, должен ли Microsoft Visio сигналить, когда не может быть установлен звук; используйте для звукового сигнала ненульное число.</span><span class="sxs-lookup"><span data-stu-id="ef3c7-127">Specifies whether Microsoft Visio beeps when sound can't be played; use a non-zero number to beep.</span></span>  <br/> |
| <span data-ttu-id="ef3c7-128">_synch_</span><span class="sxs-lookup"><span data-stu-id="ef3c7-128">_synch_</span></span> <br/> |<span data-ttu-id="ef3c7-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ef3c7-129">Required</span></span>  <br/> |<span data-ttu-id="ef3c7-130">**Логический**</span><span class="sxs-lookup"><span data-stu-id="ef3c7-130">**Boolean**</span></span> <br/> |<span data-ttu-id="ef3c7-131">Определяет, будут ли звуки играть асинхронно (0) или синхронно (1).</span><span class="sxs-lookup"><span data-stu-id="ef3c7-131">Determines whether sounds are played asynchronously (0) or synchronously (1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef3c7-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="ef3c7-132">Remarks</span></span>

<span data-ttu-id="ef3c7-133">Обычно звуки следует воспроизводить асинхронно, чтобы Visio можно было продолжать обработку во время воспроизведения звука.</span><span class="sxs-lookup"><span data-stu-id="ef3c7-133">You should usually play sounds asynchronously so that Visio can continue processing while it plays the sound.</span></span> <span data-ttu-id="ef3c7-134">Чтобы совмедить несколько звуков, синхронно их можно использовать, или некоторые из них могут не играть.</span><span class="sxs-lookup"><span data-stu-id="ef3c7-134">To string several sounds together, play them synchronously, or some might fail to play.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ef3c7-135">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ef3c7-135">Example 1</span></span>

<span data-ttu-id="ef3c7-136">PLAYSOUND("т.wav", 0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="ef3c7-136">PLAYSOUND("chord.wav", 0, 0, 0)</span></span>
  
<span data-ttu-id="ef3c7-137">Асинхронно воспроизводит звуковой файл wave,wav без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="ef3c7-137">Plays the wave audio file chord.wav asynchronously with no warning beep.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ef3c7-138">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ef3c7-138">Example 2</span></span>

<span data-ttu-id="ef3c7-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="ef3c7-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span></span>
  
<span data-ttu-id="ef3c7-140">Воспроизводит системный восклицательный звук асинхронно без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="ef3c7-140">Plays the system exclamation sound asynchronously with no warning beep.</span></span>
  

