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
ms.openlocfilehash: a7786c3ef2b4039e288596ed367083a4ed3a6c13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813638"
---
# <a name="dooleverb-function"></a><span data-ttu-id="d3237-103">Функция DOOLEVERB</span><span class="sxs-lookup"><span data-stu-id="d3237-103">DOOLEVERB Function</span></span>

<span data-ttu-id="d3237-104">Выполняет команду для объекта OLE.</span><span class="sxs-lookup"><span data-stu-id="d3237-104">Executes a verb for the OLE object.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d3237-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3237-105">Syntax</span></span>

<span data-ttu-id="d3237-106">DOOLEVERB ("** *глаголов* **")</span><span class="sxs-lookup"><span data-stu-id="d3237-106">DOOLEVERB(" ** *verb* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d3237-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3237-107">Parameters</span></span>

|<span data-ttu-id="d3237-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d3237-108">**Name**</span></span>|<span data-ttu-id="d3237-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="d3237-109">**Required/Optional**</span></span>|<span data-ttu-id="d3237-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="d3237-110">**Data Type**</span></span>|<span data-ttu-id="d3237-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d3237-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d3237-112">_«команды»_</span><span class="sxs-lookup"><span data-stu-id="d3237-112">_"verb"_</span></span> <br/> |<span data-ttu-id="d3237-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d3237-113">Required</span></span>  <br/> |<span data-ttu-id="d3237-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="d3237-114">**String**</span></span> <br/> |<span data-ttu-id="d3237-115">Для выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="d3237-115">The verb to execute.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3237-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="d3237-116">Remarks</span></span>

<span data-ttu-id="d3237-117">В более ранних версиях Visio эта функция отображается в виде _DOOLEVERB.</span><span class="sxs-lookup"><span data-stu-id="d3237-117">In earlier versions of Visio, this function appears as _DOOLEVERB.</span></span> <span data-ttu-id="d3237-118">Visio версии 4.0 и более поздних версий принимать любого из стилей.</span><span class="sxs-lookup"><span data-stu-id="d3237-118">Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d3237-119">Пример</span><span class="sxs-lookup"><span data-stu-id="d3237-119">Example</span></span>

<span data-ttu-id="d3237-120">DOOLEVERB("Edit")</span><span class="sxs-lookup"><span data-stu-id="d3237-120">DOOLEVERB("edit")</span></span>
  
<span data-ttu-id="d3237-121">Запускает программу объекта OLE и отображает связанный или внедренный объект, в котором ее можно изменить.</span><span class="sxs-lookup"><span data-stu-id="d3237-121">Runs the OLE object program and displays the linked or embedded object so that it can be edited.</span></span>
  

