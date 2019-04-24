---
title: Функция DOOLEVERB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251421
localization_priority: Normal
ms.assetid: d276c122-6326-75a7-220c-6a78e94e0db0
description: Выполняет команду для объекта OLE.
ms.openlocfilehash: c339d03a00afdf7f777bb0624ddb8fa75f277e05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301493"
---
# <a name="dooleverb-function"></a><span data-ttu-id="fbe31-103">Функция DOOLEVERB</span><span class="sxs-lookup"><span data-stu-id="fbe31-103">DOOLEVERB Function</span></span>

<span data-ttu-id="fbe31-104">Выполняет команду для объекта OLE.</span><span class="sxs-lookup"><span data-stu-id="fbe31-104">Executes a verb for the OLE object.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fbe31-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbe31-105">Syntax</span></span>

<span data-ttu-id="fbe31-106">DOOLEVERB ("\* \* *глагол* \* \*")</span><span class="sxs-lookup"><span data-stu-id="fbe31-106">DOOLEVERB(" \*\* *verb* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fbe31-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fbe31-107">Parameters</span></span>

|<span data-ttu-id="fbe31-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="fbe31-108">**Name**</span></span>|<span data-ttu-id="fbe31-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="fbe31-109">**Required/Optional**</span></span>|<span data-ttu-id="fbe31-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="fbe31-110">**Data Type**</span></span>|<span data-ttu-id="fbe31-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fbe31-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fbe31-112">_команд_</span><span class="sxs-lookup"><span data-stu-id="fbe31-112">_"verb"_</span></span> <br/> |<span data-ttu-id="fbe31-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fbe31-113">Required</span></span>  <br/> |<span data-ttu-id="fbe31-114">**String**</span><span class="sxs-lookup"><span data-stu-id="fbe31-114">**String**</span></span> <br/> |<span data-ttu-id="fbe31-115">Выполняемая команда.</span><span class="sxs-lookup"><span data-stu-id="fbe31-115">The verb to execute.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbe31-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="fbe31-116">Remarks</span></span>

<span data-ttu-id="fbe31-117">В более ранних версиях Visio Эта функция отображается как _ДУЛЕВЕРБ.</span><span class="sxs-lookup"><span data-stu-id="fbe31-117">In earlier versions of Visio, this function appears as _DOOLEVERB.</span></span> <span data-ttu-id="fbe31-118">Visio версии 4,0 и более поздних принимают любой из этих стилей.</span><span class="sxs-lookup"><span data-stu-id="fbe31-118">Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="fbe31-119">Пример</span><span class="sxs-lookup"><span data-stu-id="fbe31-119">Example</span></span>

<span data-ttu-id="fbe31-120">DOOLEVERB ("Правка")</span><span class="sxs-lookup"><span data-stu-id="fbe31-120">DOOLEVERB("edit")</span></span>
  
<span data-ttu-id="fbe31-121">Запускает объектную программу OLE и отображает связанный или внедренный объект, чтобы его можно было редактировать.</span><span class="sxs-lookup"><span data-stu-id="fbe31-121">Runs the OLE object program and displays the linked or embedded object so that it can be edited.</span></span>
  

