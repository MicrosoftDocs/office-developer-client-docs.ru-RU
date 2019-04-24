---
title: элемент PP (Текст_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Задает начало работы со свойствами абзаца. Выполнение определяется до конца текста или до следующего тега.
ms.openlocfilehash: bb2b0ab7a76c142b810ecd02dbc1b5ba7463520a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356079"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a>элемент PP (Текст_типе complexType) (' Visio XML ')

Задает начало работы со свойствами абзаца. Выполнение определяется до конца текста или до следующего тега.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Пп_типе](pp_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |страница #. XML, Master #. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Текст_типе](text_type-complextypevisio-xml.md) <br/> |Содержит текст фигуры.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|IX  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Индекс элемента абзаца **** , который определяет форматирование, применяемое к данному запуску.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
   

