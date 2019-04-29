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
description: Заставляет приложение вызывать событие маркера для надстройки, кода Microsoft Visual Basic для приложений (VBA) или надстройки COM.
ms.openlocfilehash: 841f6acc63497a6f0b8930c89534b5f8b04c0393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418808"
---
# <a name="queuemarkerevent-function"></a><span data-ttu-id="5c20e-103">Функция QUEUEMARKEREVENT</span><span class="sxs-lookup"><span data-stu-id="5c20e-103">QUEUEMARKEREVENT Function</span></span>

<span data-ttu-id="5c20e-104">Заставляет приложение вызывать событие маркера для надстройки, кода Microsoft Visual Basic для приложений (VBA) или надстройки COM.</span><span class="sxs-lookup"><span data-stu-id="5c20e-104">Causes the application to fire a marker event to your add-on, Microsoft Visual Basic for Applications (VBA) code, or COM add-in.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5c20e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c20e-105">Syntax</span></span>

<span data-ttu-id="5c20e-106">QUEUEMARKEREVENT (\* \* *евент_стринг* \* \*)</span><span class="sxs-lookup"><span data-stu-id="5c20e-106">QUEUEMARKEREVENT (\*\* *event_string* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5c20e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c20e-107">Parameters</span></span>

|<span data-ttu-id="5c20e-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5c20e-108">**Name**</span></span>|<span data-ttu-id="5c20e-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="5c20e-109">**Required/Optional**</span></span>|<span data-ttu-id="5c20e-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="5c20e-110">**Data Type**</span></span>|<span data-ttu-id="5c20e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5c20e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5c20e-112">_евент_стринг_</span><span class="sxs-lookup"><span data-stu-id="5c20e-112">_event_string_</span></span> <br/> |<span data-ttu-id="5c20e-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5c20e-113">Required</span></span>  <br/> |<span data-ttu-id="5c20e-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5c20e-114">**String**</span></span> <br/> | <span data-ttu-id="5c20e-115">Строка, которая передается обработчику событий.</span><span class="sxs-lookup"><span data-stu-id="5c20e-115">The string to pass to your event handler.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c20e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c20e-116">Remarks</span></span>

<span data-ttu-id="5c20e-117">Функция QUEUEMARKEREVENT предоставляет разработчикам способ уведомления кода из ячейки таблицы свойств фигуры и передачи сведений, относящихся к решению.</span><span class="sxs-lookup"><span data-stu-id="5c20e-117">The QUEUEMARKEREVENT function provides developers with a way to notify their code from a ShapeSheet cell, and pass solution-specific information.</span></span> <span data-ttu-id="5c20e-118">Когда вычисляется ячейка, содержащая формулу с функцией QUEUEMARKEREVENT, приложение запускает событие метки и передает _евент_стринг_ всем обработчикам событий, которые ожидают события **маркеревент** .</span><span class="sxs-lookup"><span data-stu-id="5c20e-118">When the cell containing the formula with the QUEUEMARKEREVENT function is evaluated, the application fires a marker event and passes  _event_string_ to all event handlers that are listening to the **MarkerEvent** event.</span></span> 
  
<span data-ttu-id="5c20e-119">Для получения дополнительных сведений о событиях маркеров ознакомьтесь со статьей **QueueMarkerEvent** Method and **маркеревент** Events in the Microsoft Visio Automation Reference.</span><span class="sxs-lookup"><span data-stu-id="5c20e-119">For more information about marker events, see the **QueueMarkerEvent** method and **MarkerEvent** event topics in the Microsoft Visio Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5c20e-120">Пример</span><span class="sxs-lookup"><span data-stu-id="5c20e-120">Example</span></span>

<span data-ttu-id="5c20e-121">QUEUEMARKEREVENT ("Микустомнотификатион")</span><span class="sxs-lookup"><span data-stu-id="5c20e-121">QUEUEMARKEREVENT ("MyCustomNotification")</span></span> 
  
<span data-ttu-id="5c20e-122">Заставляет приложение инициировать событие маркера и передавать строку "Микустомнотификатион" обработчикам событий, которые ожидают события **маркеревент** .</span><span class="sxs-lookup"><span data-stu-id="5c20e-122">Causes the application to fire a marker event, and passes the string "MyCustomNotification" to event handlers that are listening to the **MarkerEvent** event.</span></span> 
  

