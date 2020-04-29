---
title: Функция FIELDPICTURE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251592
localization_priority: Normal
ms.assetid: df88c55f-c098-dd4c-bf53-c7d7b60cf719
description: Возвращает строку формата изображения, которая соответствует коду внутреннего текстового формата поля Microsoft Visio.
ms.openlocfilehash: 1ab24c602c7975cf6be22a564a8b9ee9aa0d6f46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431458"
---
# <a name="fieldpicture-function"></a>Функция FIELDPICTURE

Возвращает строку формата изображения, которая соответствует коду внутреннего текстового формата поля Microsoft Visio.
  
## <a name="syntax"></a>Синтаксис

FIELDPICTURE (* * *Code* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _code_ <br/> |Обязательна  <br/> |**Number** <br/> | Код формата текстового поля.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Format строки изображений используются в функции FORMAT для определения расширения значений дат, времени, чисел и меток единиц.
  
## <a name="example"></a>Пример

FIELDPICTURE (0) 
  
Возвращает строку изображения "ESC (0)", которая указывает число с одним десятичным разрядом и описанием в нижнем регистре при использовании в функции FORMAT. 
  

