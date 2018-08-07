---
title: Функция ANGLEALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Возвращает тангенс угла пути в данный момент.
ms.openlocfilehash: ec5529037275fc8661972cc7403886cd33150b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813174"
---
# <a name="anglealongpath-function"></a>Функция ANGLEALONGPATH

Возвращает тангенс угла пути в данный момент.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

ANGLEALONGPATH (** *раздел* **, ** *путешествий* ** ** *[, сегмент]* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Обязательный  <br/> |**Строка** <br/> |Раздел геометрии, представляющий путь, указанный с помощью ссылки на его ячейку Path (например, Geometry1.Path).  <br/> |
| _поездки_ <br/> |Обязательный  <br/> |**Double** <br/> |Процент по пути из начальной точки конечную точку. Должен быть в диапазоне от 0 до 1.  <br/> |
| _сегмента_ <br/> |Optional  <br/> |**Integer** <br/> |На основе 1 сегмент путь, на котором для вычисления тангенс угла.  <br/> |
   
### <a name="return-value"></a>������������ ��������

 **Double**
  
## <a name="remarks"></a>Замечания

Если включить значение _сегмента_ ANGLEALONGPATH возвращает значение сегмента только. 
  
При включении значение _сегмента_ ANGLEALONGPATH определяет точку тангенс с помощью _выезжает_ для вычисления percertage по _сегмента_.
  
Если _раздел_ или _Сегмент_ не существует, Microsoft Visio возвращает #REF!. 
  

