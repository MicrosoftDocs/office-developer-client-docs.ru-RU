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
description: Вызывает, что приложение вызывает событие маркера для надстройки, кода Microsoft Visual Basic для приложений (VBA) или надстройки COM.
ms.openlocfilehash: 841f6acc63497a6f0b8930c89534b5f8b04c0393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418808"
---
# <a name="queuemarkerevent-function"></a>Функция QUEUEMARKEREVENT

Вызывает, что приложение вызывает событие маркера для надстройки, кода Microsoft Visual Basic для приложений (VBA) или надстройки COM. 
  
## <a name="syntax"></a>Синтаксис

QUEUEMARKEREVENT (** *event_string* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _event_string_ <br/> |Обязательный  <br/> |**String** <br/> | Строка, которая передается обработители события.  <br/> |
   
## <a name="remarks"></a>Примечания

Функция QUEUEMARKEREVENT предоставляет разработчикам возможность уведомлять о своем коде из ячейки ShapeSheet и передавать сведения, специфические для решения. При оценке ячейки, _содержащей_ формулу с функцией QUEUEMARKEREVENT, приложение загорелось событие маркера и передает event_string всем обработчикам событий, прослушивающих событие **MarkerEvent.** 
  
Дополнительные сведения о событиях маркеров см. в **разделе QueueMarkerEvent** и **разделы событий MarkerEvent** в справочной Visio автоматизации Майкрософт. 
  
## <a name="example"></a>Пример

QUEUEMARKEREVENT ("MyCustomNotification") 
  
Вызывает событие маркера и передает строку "MyCustomNotification" обработчику событий, которые прослушивают событие **MarkerEvent.** 
  

