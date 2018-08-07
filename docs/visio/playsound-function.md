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
ms.openlocfilehash: ca54b749b764e9ea2c7db71d41268303542417f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814407"
---
# <a name="playsound-function"></a><span data-ttu-id="daa7f-103">Функция PLAYSOUND</span><span class="sxs-lookup"><span data-stu-id="daa7f-103">PLAYSOUND Function</span></span>

<span data-ttu-id="daa7f-104">Воспроизводит звуковой файл или системный звук.</span><span class="sxs-lookup"><span data-stu-id="daa7f-104">Plays a sound file or system sound.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="daa7f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="daa7f-105">Syntax</span></span>

<span data-ttu-id="daa7f-106">PLAYSOUND ("** *filename* **" | "** *псевдоним* **", ** *isAlias* **, ** *Звуковые* **, ** *synch* **)</span><span class="sxs-lookup"><span data-stu-id="daa7f-106">PLAYSOUND(" ** *filename* ** "|" ** *alias* ** ", ** *isAlias* **, ** *beep* **, ** *synch* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="daa7f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="daa7f-107">Parameters</span></span>

|<span data-ttu-id="daa7f-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="daa7f-108">**Name**</span></span>|<span data-ttu-id="daa7f-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="daa7f-109">**Required/Optional**</span></span>|<span data-ttu-id="daa7f-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="daa7f-110">**Data Type**</span></span>|<span data-ttu-id="daa7f-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="daa7f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="daa7f-112">_Имя файла_</span><span class="sxs-lookup"><span data-stu-id="daa7f-112">_filename_</span></span> <br/> |<span data-ttu-id="daa7f-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="daa7f-113">Required</span></span>  <br/> |<span data-ttu-id="daa7f-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="daa7f-114">**String**</span></span> <br/> |<span data-ttu-id="daa7f-115">Имя звукового файла, которые необходимо воспроизвести.</span><span class="sxs-lookup"><span data-stu-id="daa7f-115">The name of the sound file you want to play.</span></span>  <br/> |
| <span data-ttu-id="daa7f-116">_alias_</span><span class="sxs-lookup"><span data-stu-id="daa7f-116">_alias_</span></span> <br/> |<span data-ttu-id="daa7f-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="daa7f-117">Required</span></span>  <br/> |<span data-ttu-id="daa7f-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="daa7f-118">**String**</span></span> <br/> | <span data-ttu-id="daa7f-119">Система звуковой представленный псевдоним.</span><span class="sxs-lookup"><span data-stu-id="daa7f-119">A system sound represented by an alias.</span></span>  <br/> |
| <span data-ttu-id="daa7f-120">_isAlias_</span><span class="sxs-lookup"><span data-stu-id="daa7f-120">_isAlias_</span></span> <br/> |<span data-ttu-id="daa7f-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="daa7f-121">Required</span></span>  <br/> |<span data-ttu-id="daa7f-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="daa7f-122">**Boolean**</span></span> <br/> | <span data-ttu-id="daa7f-123">Указывает, является ли предыдущего выражения псевдоним или имя; Используйте ненулевое значение, чтобы указать псевдоним.</span><span class="sxs-lookup"><span data-stu-id="daa7f-123">Specifies whether the preceding expression is an alias or file name; use a non-zero value to specify an alias.</span></span>  <br/> |
| <span data-ttu-id="daa7f-124">_звуковой сигнал_</span><span class="sxs-lookup"><span data-stu-id="daa7f-124">_beep_</span></span> <br/> |<span data-ttu-id="daa7f-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="daa7f-125">Required</span></span>  <br/> |<span data-ttu-id="daa7f-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="daa7f-126">**Boolean**</span></span> <br/> |<span data-ttu-id="daa7f-127">Указывает, будет ли Microsoft Visio издает звуковые сигналы при не может воспроизводиться звук; Используйте ненулевое число звуковые сигналы.</span><span class="sxs-lookup"><span data-stu-id="daa7f-127">Specifies whether Microsoft Visio beeps when sound can't be played; use a non-zero number to beep.</span></span>  <br/> |
| <span data-ttu-id="daa7f-128">_Синхронизация_</span><span class="sxs-lookup"><span data-stu-id="daa7f-128">_synch_</span></span> <br/> |<span data-ttu-id="daa7f-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="daa7f-129">Required</span></span>  <br/> |<span data-ttu-id="daa7f-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="daa7f-130">**Boolean**</span></span> <br/> |<span data-ttu-id="daa7f-131">Определяет, будут ли асинхронно воспроизводиться звуки (0) или синхронно (1).</span><span class="sxs-lookup"><span data-stu-id="daa7f-131">Determines whether sounds are played asynchronously (0) or synchronously (1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="daa7f-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="daa7f-132">Remarks</span></span>

<span data-ttu-id="daa7f-133">Вы должны обычно воспроизведения звуков асинхронно, чтобы Visio можно продолжить обработку во время воспроизведения звука.</span><span class="sxs-lookup"><span data-stu-id="daa7f-133">You should usually play sounds asynchronously so that Visio can continue processing while it plays the sound.</span></span> <span data-ttu-id="daa7f-134">Чтобы строка несколько звуков друг с другом, их воспроизведения синхронно или некоторые не удается воспроизвести.</span><span class="sxs-lookup"><span data-stu-id="daa7f-134">To string several sounds together, play them synchronously, or some might fail to play.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="daa7f-135">Пример 1</span><span class="sxs-lookup"><span data-stu-id="daa7f-135">Example 1</span></span>

<span data-ttu-id="daa7f-136">PLAYSOUND ("chord.wav", 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="daa7f-136">PLAYSOUND("chord.wav", 0, 0, 0)</span></span>
  
<span data-ttu-id="daa7f-137">Воспроизводит chord.wav звукового файла звукозаписи асинхронно с не сигнал.</span><span class="sxs-lookup"><span data-stu-id="daa7f-137">Plays the wave audio file chord.wav asynchronously with no warning beep.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="daa7f-138">Пример 2</span><span class="sxs-lookup"><span data-stu-id="daa7f-138">Example 2</span></span>

<span data-ttu-id="daa7f-139">PLAYSOUND ("SystemExclamation", 1, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="daa7f-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span></span>
  
<span data-ttu-id="daa7f-140">Воспроизведение звука асинхронно с не сигнал восклицательный знак системы.</span><span class="sxs-lookup"><span data-stu-id="daa7f-140">Plays the system exclamation sound asynchronously with no warning beep.</span></span>
  

