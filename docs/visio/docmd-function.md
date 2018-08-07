---
title: Функция DOCMD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60100
localization_priority: Normal
ms.assetid: 6574edeb-eb6f-afd9-89c4-eb5996dffa30
description: Выполняет указанную команду.
ms.openlocfilehash: e425dd9605c18d4647787c5df7aeaa4fd5f9e4cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813622"
---
# <a name="docmd-function"></a><span data-ttu-id="009fe-103">Функция DOCMD</span><span class="sxs-lookup"><span data-stu-id="009fe-103">DOCMD Function</span></span>

<span data-ttu-id="009fe-104">Выполняет указанную команду.</span><span class="sxs-lookup"><span data-stu-id="009fe-104">Performs the identified command.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="009fe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="009fe-105">Syntax</span></span>

 <span data-ttu-id="009fe-106">**DOCMD** ( _идентификатор команды_)</span><span class="sxs-lookup"><span data-stu-id="009fe-106">**DOCMD**( _commandID_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="009fe-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="009fe-107">Parameters</span></span>

|<span data-ttu-id="009fe-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="009fe-108">**Name**</span></span>|<span data-ttu-id="009fe-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="009fe-109">**Required/Optional**</span></span>|<span data-ttu-id="009fe-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="009fe-110">**Data Type**</span></span>|<span data-ttu-id="009fe-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="009fe-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="009fe-112">_Идентификатор команды_</span><span class="sxs-lookup"><span data-stu-id="009fe-112">_commandID_</span></span> <br/> |<span data-ttu-id="009fe-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="009fe-113">Required</span></span>  <br/> |<span data-ttu-id="009fe-114">**Число**</span><span class="sxs-lookup"><span data-stu-id="009fe-114">**Number**</span></span> <br/> | <span data-ttu-id="009fe-115">Чтобы выполнить команду.</span><span class="sxs-lookup"><span data-stu-id="009fe-115">The command to perform.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="009fe-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="009fe-116">Remarks</span></span>

<span data-ttu-id="009fe-117">Чтобы получить список команды, которые поддерживают функцию DOCMD приведены в разделе «DoCmd/DOCMD команды» в справочник по автоматизации Microsoft Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="009fe-117">For a list of commands that are supported with the DOCMD function, see the topic "DoCmd/DOCMD commands" in the Microsoft Visio 2013 Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="009fe-118">Пример</span><span class="sxs-lookup"><span data-stu-id="009fe-118">Example</span></span>

 `DOCMD (1312)`
  
<span data-ttu-id="009fe-119">Вызывает диалоговое окно " **Данные фигуры** " отображаться в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="009fe-119">Causes the **Shape Data** dialog box to appear in the user interface.</span></span> 
  

