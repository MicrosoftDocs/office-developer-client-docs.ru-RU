---
title: Функция PATHLENGTH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Возвращает длину пути, который определен в указанном раздел геометрии.
ms.openlocfilehash: 37cabbde9fc0782bc1fde46f3065d0c945c9dada
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814358"
---
# <a name="pathlength-function"></a>Функция PATHLENGTH

Возвращает длину пути, который определен в указанном раздел геометрии.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010 
  
## <a name="syntax"></a>Синтаксис

PATHLENGTH (** *раздел* ** ** *[, сегмент]* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Обязательный  <br/> |**Строка** <br/> |Раздел геометрии, представляющий путь, указанный с помощью ссылки на его ячейку Path (например, Geometry1.Path).  <br/> |
| _сегмента_ <br/> |Optional  <br/> |**Integer** <br/> |На основе 1 сегментом пути для измерения.  <br/> |
   
### <a name="return-value"></a>������������ ��������

 **Double**
  
## <a name="remarks"></a>Замечания

Если _раздел_ или _Сегмент_ не существует, Microsoft Visio возвращает #REF!. 
  
Если включить значение _сегмента_ PATHLENGTH возвращает длина сегмента только. 
  

