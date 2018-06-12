---
title: Функция NEARESTPOINTONPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Возвращает процент расстояния по пути точки, который является ближайшим по указанным координатам как в диапазоне от 0 до 1.
ms.openlocfilehash: d9e9b890033526fec99f04cee30ae93578487652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814289"
---
# <a name="nearestpointonpath-function"></a>Функция NEARESTPOINTONPATH

Возвращает процент расстояния по пути точки, который является ближайшим по указанным координатам как в диапазоне от 0 до 1.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010 
  
## <a name="syntax"></a>Синтаксис

NEARESTPOINTONPATH (** *раздел* **, ** *x* **, ** *y* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Обязательный  <br/> |**Строка** <br/> |Раздел геометрии, представляющий путь, указанный с помощью ссылки на его ячейку Path (например, Geometry1.Path).  <br/> |
| _x_ <br/> |Обязательный  <br/> |**Double** <br/> |_X_-координата указанный момент.  <br/> |
| _y_ <br/> |Обязательный  <br/> |**Double** <br/> |_Y_-координата указанный момент.  <br/> |
   
### <a name="return-value"></a>������������ ��������

 **Double**
  
## <a name="remarks"></a>Замечания

Если _раздел_ не существует, Microsoft Visio возвращает #REF!. 
  

