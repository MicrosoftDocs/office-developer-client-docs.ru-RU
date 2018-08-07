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
description: Возвращает строку формата изображения, соответствующее поле формат Microsoft Visio внутренний текст кода.
ms.openlocfilehash: 1528cefd65ed0c7c1dde02fa390babf26442b4d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813728"
---
# <a name="fieldpicture-function"></a>Функция FIELDPICTURE

Возвращает строку формата изображения, соответствующее поле формат Microsoft Visio внутренний текст кода.
  
## <a name="syntax"></a>Синтаксис

FIELDPICTURE (** *кода* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _code_ <br/> |Обязательный  <br/> |**Число** <br/> | Код формата текстового поля.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Строка
  
## <a name="remarks"></a>Замечания

В функции FORMAT для определения расширения значения даты, времени, чисел и заголовки устройства используются строки изображение формата.
  
## <a name="example"></a>Пример

FIELDPICTURE(0) 
  
Возвращает строку формата рисунок «esc(0)», который указывает номер, который имеет один десятичный и описание строчная единицу при использовании функции FORMAT. 
  

