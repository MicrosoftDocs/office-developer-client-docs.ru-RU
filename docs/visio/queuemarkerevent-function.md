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
# <a name="queuemarkerevent-function"></a>Функция QUEUEMARKEREVENT

Заставляет приложение вызывать событие маркера для надстройки, кода Microsoft Visual Basic для приложений (VBA) или надстройки COM. 
  
## <a name="syntax"></a>Синтаксис

QUEUEMARKEREVENT (* * *евент_стринг* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _евент_стринг_ <br/> |Обязательный  <br/> |**String** <br/> | Строка, которая передается обработчику событий.  <br/> |
   
## <a name="remarks"></a>Примечания

Функция QUEUEMARKEREVENT предоставляет разработчикам способ уведомления кода из ячейки таблицы свойств фигуры и передачи сведений, относящихся к решению. Когда вычисляется ячейка, содержащая формулу с функцией QUEUEMARKEREVENT, приложение запускает событие метки и передает _евент_стринг_ всем обработчикам событий, которые ожидают события **маркеревент** . 
  
Для получения дополнительных сведений о событиях маркеров ознакомьтесь со статьей **QueueMarkerEvent** Method and **маркеревент** Events in the Microsoft Visio Automation Reference. 
  
## <a name="example"></a>Пример

QUEUEMARKEREVENT ("Микустомнотификатион") 
  
Заставляет приложение инициировать событие маркера и передавать строку "Микустомнотификатион" обработчикам событий, которые ожидают события **маркеревент** . 
  

