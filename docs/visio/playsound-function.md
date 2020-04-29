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
# <a name="playsound-function"></a><span data-ttu-id="964fb-103">Функция PLAYSOUND</span><span class="sxs-lookup"><span data-stu-id="964fb-103">PLAYSOUND Function</span></span>

<span data-ttu-id="964fb-104">Воспроизводит звуковой файл или системный звук.</span><span class="sxs-lookup"><span data-stu-id="964fb-104">Plays a sound file or system sound.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="964fb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="964fb-105">Syntax</span></span>

<span data-ttu-id="964fb-106">PLAYSOUND ("\* \* *имя_файла* \* *" | "* \* *Alias* \* \*", \* \*- *Alias* \* \*, \* \* *Beep* \* \*, \* \* *synch* \* \*)</span><span class="sxs-lookup"><span data-stu-id="964fb-106">PLAYSOUND(" \*\* *filename* \*\* "|" \*\* *alias* \*\* ", \*\* *isAlias* \*\*, \*\* *beep* \*\*, \*\* *synch* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="964fb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="964fb-107">Parameters</span></span>

|<span data-ttu-id="964fb-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="964fb-108">**Name**</span></span>|<span data-ttu-id="964fb-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="964fb-109">**Required/Optional**</span></span>|<span data-ttu-id="964fb-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="964fb-110">**Data Type**</span></span>|<span data-ttu-id="964fb-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="964fb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="964fb-112">_задан_</span><span class="sxs-lookup"><span data-stu-id="964fb-112">_filename_</span></span> <br/> |<span data-ttu-id="964fb-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="964fb-113">Required</span></span>  <br/> |<span data-ttu-id="964fb-114">**String**</span><span class="sxs-lookup"><span data-stu-id="964fb-114">**String**</span></span> <br/> |<span data-ttu-id="964fb-115">Имя звукового файла, который необходимо прослушать.</span><span class="sxs-lookup"><span data-stu-id="964fb-115">The name of the sound file you want to play.</span></span>  <br/> |
| <span data-ttu-id="964fb-116">_alias_</span><span class="sxs-lookup"><span data-stu-id="964fb-116">_alias_</span></span> <br/> |<span data-ttu-id="964fb-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="964fb-117">Required</span></span>  <br/> |<span data-ttu-id="964fb-118">**String**</span><span class="sxs-lookup"><span data-stu-id="964fb-118">**String**</span></span> <br/> | <span data-ttu-id="964fb-119">Системный звук, представленный псевдонимом.</span><span class="sxs-lookup"><span data-stu-id="964fb-119">A system sound represented by an alias.</span></span>  <br/> |
| <span data-ttu-id="964fb-120">_Псевдоним_</span><span class="sxs-lookup"><span data-stu-id="964fb-120">_isAlias_</span></span> <br/> |<span data-ttu-id="964fb-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="964fb-121">Required</span></span>  <br/> |<span data-ttu-id="964fb-122">**Логический**</span><span class="sxs-lookup"><span data-stu-id="964fb-122">**Boolean**</span></span> <br/> | <span data-ttu-id="964fb-123">Указывает, является ли предыдущее выражение псевдонимом или именем файла; Используйте ненулевое значение, чтобы указать псевдоним.</span><span class="sxs-lookup"><span data-stu-id="964fb-123">Specifies whether the preceding expression is an alias or file name; use a non-zero value to specify an alias.</span></span>  <br/> |
| <span data-ttu-id="964fb-124">_гудок_</span><span class="sxs-lookup"><span data-stu-id="964fb-124">_beep_</span></span> <br/> |<span data-ttu-id="964fb-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="964fb-125">Required</span></span>  <br/> |<span data-ttu-id="964fb-126">**Логический**</span><span class="sxs-lookup"><span data-stu-id="964fb-126">**Boolean**</span></span> <br/> |<span data-ttu-id="964fb-127">Указывает, следует ли включать звуковые сигналы при невозможности воспроизведения звукового сигнала в Microsoft Visio. Используйте для звукового сигнала ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="964fb-127">Specifies whether Microsoft Visio beeps when sound can't be played; use a non-zero number to beep.</span></span>  <br/> |
| <span data-ttu-id="964fb-128">_точный_</span><span class="sxs-lookup"><span data-stu-id="964fb-128">_synch_</span></span> <br/> |<span data-ttu-id="964fb-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="964fb-129">Required</span></span>  <br/> |<span data-ttu-id="964fb-130">**Логический**</span><span class="sxs-lookup"><span data-stu-id="964fb-130">**Boolean**</span></span> <br/> |<span data-ttu-id="964fb-131">Определяет, воспроизводится ли звук асинхронно (0) или синхронно (1).</span><span class="sxs-lookup"><span data-stu-id="964fb-131">Determines whether sounds are played asynchronously (0) or synchronously (1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="964fb-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="964fb-132">Remarks</span></span>

<span data-ttu-id="964fb-133">Обычно воспроизводите звуки асинхронно, чтобы Visio мог продолжать обработку при воспроизведении звука.</span><span class="sxs-lookup"><span data-stu-id="964fb-133">You should usually play sounds asynchronously so that Visio can continue processing while it plays the sound.</span></span> <span data-ttu-id="964fb-134">Чтобы объединить несколько звуков, воспроизводить их синхронно, или некоторые из них могут не воспроизводиться.</span><span class="sxs-lookup"><span data-stu-id="964fb-134">To string several sounds together, play them synchronously, or some might fail to play.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="964fb-135">Пример 1</span><span class="sxs-lookup"><span data-stu-id="964fb-135">Example 1</span></span>

<span data-ttu-id="964fb-136">PLAYSOUND ("аккорд. wav", 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="964fb-136">PLAYSOUND("chord.wav", 0, 0, 0)</span></span>
  
<span data-ttu-id="964fb-137">Выполняет асинхронное воспроизведение звукового файла аккорд. WAV без сигнала предупреждения.</span><span class="sxs-lookup"><span data-stu-id="964fb-137">Plays the wave audio file chord.wav asynchronously with no warning beep.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="964fb-138">Пример 2</span><span class="sxs-lookup"><span data-stu-id="964fb-138">Example 2</span></span>

<span data-ttu-id="964fb-139">PLAYSOUND ("Системекскламатион", 1, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="964fb-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span></span>
  
<span data-ttu-id="964fb-140">Выполняет асинхронный звук с желтым восклицательным сигналом без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="964fb-140">Plays the system exclamation sound asynchronously with no warning beep.</span></span>
  

