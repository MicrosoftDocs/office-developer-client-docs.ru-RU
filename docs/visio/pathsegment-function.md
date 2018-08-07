---
title: Функция PATHSEGMENT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Возвращает номер 1-based сегмента в указанную часть пометить по указанному пути.
ms.openlocfilehash: b25f43ffa3c719cfc5ffbd1e417f2da9640e483b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814363"
---
# <a name="pathsegment-function"></a>Функция PATHSEGMENT

Возвращает номер 1-based сегмента в указанную часть пометить по указанному пути.
  
## <a name="syntax"></a>Синтаксис

PATHSEGMENT (** *раздел* **, ** *путешествий* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Обязательный  <br/> |**Строка** <br/> |Раздел геометрии, представляющий путь, указанный с помощью ссылки на его ячейку Path (например, Geometry1.Path).  <br/> |
| _поездки_ <br/> |Обязательный  <br/> |**Double** <br/> |Процент путь, начиная с начальной точки в конечную точку. Должен быть в диапазоне от 0 до 1.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Целое число
  

