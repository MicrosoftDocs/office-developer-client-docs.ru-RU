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
description: Указывает приложение должно срабатывать событие маркер для надстроек, Microsoft Visual Basic для приложений (VBA) или надстройки COM.
ms.openlocfilehash: b9175caf0845530c93f6db15e286f3eae21ea415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814511"
---
# <a name="queuemarkerevent-function"></a><span data-ttu-id="50c65-103">Функция QUEUEMARKEREVENT</span><span class="sxs-lookup"><span data-stu-id="50c65-103">QUEUEMARKEREVENT Function</span></span>

<span data-ttu-id="50c65-104">Указывает приложение должно срабатывать событие маркер для надстроек, Microsoft Visual Basic для приложений (VBA) или надстройки COM.</span><span class="sxs-lookup"><span data-stu-id="50c65-104">Causes the application to fire a marker event to your add-on, Microsoft Visual Basic for Applications (VBA) code, or COM add-in.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="50c65-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50c65-105">Syntax</span></span>

<span data-ttu-id="50c65-106">QUEUEMARKEREVENT (** *event_string* **)</span><span class="sxs-lookup"><span data-stu-id="50c65-106">QUEUEMARKEREVENT (** *event_string* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="50c65-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="50c65-107">Parameters</span></span>

|<span data-ttu-id="50c65-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="50c65-108">**Name**</span></span>|<span data-ttu-id="50c65-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="50c65-109">**Required/Optional**</span></span>|<span data-ttu-id="50c65-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="50c65-110">**Data Type**</span></span>|<span data-ttu-id="50c65-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="50c65-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="50c65-112">_event_string_</span><span class="sxs-lookup"><span data-stu-id="50c65-112">_event_string_</span></span> <br/> |<span data-ttu-id="50c65-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="50c65-113">Required</span></span>  <br/> |<span data-ttu-id="50c65-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="50c65-114">**String**</span></span> <br/> | <span data-ttu-id="50c65-115">Строка для передачи обработчику событий.</span><span class="sxs-lookup"><span data-stu-id="50c65-115">The string to pass to your event handler.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50c65-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="50c65-116">Remarks</span></span>

<span data-ttu-id="50c65-117">Функция QUEUEMARKEREVENT предоставляет разработчикам способ для уведомления кода из ячейки таблицы свойств фигуры и передавать сведения о конкретных решений.</span><span class="sxs-lookup"><span data-stu-id="50c65-117">The QUEUEMARKEREVENT function provides developers with a way to notify their code from a ShapeSheet cell, and pass solution-specific information.</span></span> <span data-ttu-id="50c65-118">При вычислении ячеек, содержащий формулу, с помощью функции QUEUEMARKEREVENT приложение вызывает событие маркера и передает _event_string_ все обработчики событий, которые прослушивание события **MarkerEvent** .</span><span class="sxs-lookup"><span data-stu-id="50c65-118">When the cell containing the formula with the QUEUEMARKEREVENT function is evaluated, the application fires a marker event and passes  _event_string_ to all event handlers that are listening to the **MarkerEvent** event.</span></span> 
  
<span data-ttu-id="50c65-119">Дополнительные сведения о событиях маркер можно метод **QueueMarkerEvent** и **MarkerEvent** события подразделы Справочник по автоматизации Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="50c65-119">For more information about marker events, see the **QueueMarkerEvent** method and **MarkerEvent** event topics in the Microsoft Visio Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="50c65-120">Пример</span><span class="sxs-lookup"><span data-stu-id="50c65-120">Example</span></span>

<span data-ttu-id="50c65-121">QUEUEMARKEREVENT («MyCustomNotification»)</span><span class="sxs-lookup"><span data-stu-id="50c65-121">QUEUEMARKEREVENT ("MyCustomNotification")</span></span> 
  
<span data-ttu-id="50c65-122">Приводит к событие маркер приложения и передает строку «MyCustomNotification» обработчиков событий, которые прослушивание события **MarkerEvent** .</span><span class="sxs-lookup"><span data-stu-id="50c65-122">Causes the application to fire a marker event, and passes the string "MyCustomNotification" to event handlers that are listening to the **MarkerEvent** event.</span></span> 
  

