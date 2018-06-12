---
title: Функция СЖПРОБЕЛЫ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
localization_priority: Normal
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: Удаляет все пространство из текста, за исключением одиночных пробелов между словами.
ms.openlocfilehash: b396572041e880451ceb1ec6f0508528c0807bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815073"
---
# <a name="trim-function"></a><span data-ttu-id="5df40-103">Функция СЖПРОБЕЛЫ</span><span class="sxs-lookup"><span data-stu-id="5df40-103">TRIM Function</span></span>

<span data-ttu-id="5df40-104">Удаляет все пространство из текста, за исключением одиночных пробелов между словами.</span><span class="sxs-lookup"><span data-stu-id="5df40-104">Removes all space from text, except for single spaces between words.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5df40-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5df40-105">Syntax</span></span>

<span data-ttu-id="5df40-106">ОБРЕЗКА (** *текст* **)</span><span class="sxs-lookup"><span data-stu-id="5df40-106">TRIM (** *text* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5df40-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5df40-107">Parameters</span></span>

|<span data-ttu-id="5df40-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5df40-108">**Name**</span></span>|<span data-ttu-id="5df40-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="5df40-109">**Required/Optional**</span></span>|<span data-ttu-id="5df40-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="5df40-110">**Data Type**</span></span>|<span data-ttu-id="5df40-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5df40-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5df40-112">_text_</span><span class="sxs-lookup"><span data-stu-id="5df40-112">_text_</span></span> <br/> |<span data-ttu-id="5df40-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5df40-113">Required</span></span>  <br/> |<span data-ttu-id="5df40-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="5df40-114">**String**</span></span> <br/> |<span data-ttu-id="5df40-115">Текст, из которого требуется удалить пробелы.</span><span class="sxs-lookup"><span data-stu-id="5df40-115">The text from which you want to remove spaces.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5df40-116">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="5df40-116">Return value</span></span>

<span data-ttu-id="5df40-117">Строка</span><span class="sxs-lookup"><span data-stu-id="5df40-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5df40-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="5df40-118">Remarks</span></span>

<span data-ttu-id="5df40-119">Можно использовать функцию СЖПРОБЕЛЫ на текст, полученный из другого приложения, которое может содержать избыточные пробелы.</span><span class="sxs-lookup"><span data-stu-id="5df40-119">You can use the TRIM function on text that you have received from another application that may have irregular spacing.</span></span>
  
## <a name="example"></a><span data-ttu-id="5df40-120">Пример</span><span class="sxs-lookup"><span data-stu-id="5df40-120">Example</span></span>

<span data-ttu-id="5df40-121">ИСПОЛНЕНИЕ («1 января 2003»)</span><span class="sxs-lookup"><span data-stu-id="5df40-121">TRIM ("January 1, 2003 ")</span></span> 
  
<span data-ttu-id="5df40-122">Возвращает «1 января 2003».</span><span class="sxs-lookup"><span data-stu-id="5df40-122">Returns "January 1, 2003".</span></span> 
  

