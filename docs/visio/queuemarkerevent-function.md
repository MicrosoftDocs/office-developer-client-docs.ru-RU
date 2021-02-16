---
title: Функция QUEUEMARKEREVENT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60107
localization_priority: Normal
ms.assetid: b4671715-4209-7774-c174-c19dc9721a02
description: Приложение вызывает событие маркера для вашей надстройки, кода Microsoft Visual Basic для приложений (VBA) или надстройки COM.
ms.openlocfilehash: 841f6acc63497a6f0b8930c89534b5f8b04c0393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418808"
---
# <a name="queuemarkerevent-function"></a><span data-ttu-id="0e418-103">Функция QUEUEMARKEREVENT</span><span class="sxs-lookup"><span data-stu-id="0e418-103">QUEUEMARKEREVENT Function</span></span>

<span data-ttu-id="0e418-104">Приложение вызывает событие маркера для вашей надстройки, кода Microsoft Visual Basic для приложений (VBA) или надстройки COM.</span><span class="sxs-lookup"><span data-stu-id="0e418-104">Causes the application to fire a marker event to your add-on, Microsoft Visual Basic for Applications (VBA) code, or COM add-in.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0e418-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e418-105">Syntax</span></span>

<span data-ttu-id="0e418-106">QUEUEMARKEREVENT (\*\* *event_string* \*\* )</span><span class="sxs-lookup"><span data-stu-id="0e418-106">QUEUEMARKEREVENT (\*\* *event_string* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0e418-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e418-107">Parameters</span></span>

|<span data-ttu-id="0e418-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="0e418-108">**Name**</span></span>|<span data-ttu-id="0e418-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="0e418-109">**Required/Optional**</span></span>|<span data-ttu-id="0e418-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="0e418-110">**Data Type**</span></span>|<span data-ttu-id="0e418-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0e418-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0e418-112">_event_string_</span><span class="sxs-lookup"><span data-stu-id="0e418-112">_event_string_</span></span> <br/> |<span data-ttu-id="0e418-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="0e418-113">Required</span></span>  <br/> |<span data-ttu-id="0e418-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="0e418-114">**String**</span></span> <br/> | <span data-ttu-id="0e418-115">Строка, передаемая обработитее события.</span><span class="sxs-lookup"><span data-stu-id="0e418-115">The string to pass to your event handler.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e418-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="0e418-116">Remarks</span></span>

<span data-ttu-id="0e418-117">Функция QUEUEMARKEREVENT позволяет разработчикам уведомлять код из ячейки ShapeSheet и передавать сведения о решении.</span><span class="sxs-lookup"><span data-stu-id="0e418-117">The QUEUEMARKEREVENT function provides developers with a way to notify their code from a ShapeSheet cell, and pass solution-specific information.</span></span> <span data-ttu-id="0e418-118">При оценке ячейки, содержащей формулу с функцией QUEUEMARKEREVENT, приложение  с помощью события маркера и передает event_string всем обработчикам событий, которые прослушивают событие **MarkerEvent.**</span><span class="sxs-lookup"><span data-stu-id="0e418-118">When the cell containing the formula with the QUEUEMARKEREVENT function is evaluated, the application fires a marker event and passes  _event_string_ to all event handlers that are listening to the **MarkerEvent** event.</span></span> 
  
<span data-ttu-id="0e418-119">Дополнительные сведения о событиях маркеров см. в темах о методе **QueueMarkerEvent** и **MarkerEvent** в справочнике по автоматизации Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="0e418-119">For more information about marker events, see the **QueueMarkerEvent** method and **MarkerEvent** event topics in the Microsoft Visio Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="0e418-120">Пример</span><span class="sxs-lookup"><span data-stu-id="0e418-120">Example</span></span>

<span data-ttu-id="0e418-121">QUEUEMARKEREVENT ("MyCustomNotification")</span><span class="sxs-lookup"><span data-stu-id="0e418-121">QUEUEMARKEREVENT ("MyCustomNotification")</span></span> 
  
<span data-ttu-id="0e418-122">Вызывает событие маркера в приложении и передает строку "MyCustomNotification" обработчику событий, которые прослушивают событие **MarkerEvent.**</span><span class="sxs-lookup"><span data-stu-id="0e418-122">Causes the application to fire a marker event, and passes the string "MyCustomNotification" to event handlers that are listening to the **MarkerEvent** event.</span></span> 
  

