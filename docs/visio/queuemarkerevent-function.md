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
# <a name="queuemarkerevent-function"></a>Функция QUEUEMARKEREVENT

Указывает приложение должно срабатывать событие маркер для надстроек, Microsoft Visual Basic для приложений (VBA) или надстройки COM. 
  
## <a name="syntax"></a>Синтаксис

QUEUEMARKEREVENT (** *event_string* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _event_string_ <br/> |Обязательный  <br/> |**Строка** <br/> | Строка для передачи обработчику событий.  <br/> |
   
## <a name="remarks"></a>Замечания

Функция QUEUEMARKEREVENT предоставляет разработчикам способ для уведомления кода из ячейки таблицы свойств фигуры и передавать сведения о конкретных решений. При вычислении ячеек, содержащий формулу, с помощью функции QUEUEMARKEREVENT приложение вызывает событие маркера и передает _event_string_ все обработчики событий, которые прослушивание события **MarkerEvent** . 
  
Дополнительные сведения о событиях маркер можно метод **QueueMarkerEvent** и **MarkerEvent** события подразделы Справочник по автоматизации Microsoft Visio. 
  
## <a name="example"></a>Пример

QUEUEMARKEREVENT («MyCustomNotification») 
  
Приводит к событие маркер приложения и передает строку «MyCustomNotification» обработчиков событий, которые прослушивание события **MarkerEvent** . 
  

