---
title: Элемент rel (Паже_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d61b1b97-c360-4d9d-217f-e6f45f760e42
description: Задает отношение к части с соответствующим XML-ДОКУМЕНТом страницы.
ms.openlocfilehash: 7a45764817175f670cdb009157e21a1a25f31cc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320001"
---
# <a name="rel-element-pagetype-complextype-visio-xml"></a>Элемент rel (Паже_типе complexType) (' Visio XML ')

Задает отношение к части с соответствующим XML-ДОКУМЕНТом страницы.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Рел_типе](rel_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Pages. XML, Masters. XML, recordsets. XML, Page #. XML, Master #. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Паже_типе](page_type-complextypevisio-xml.md) <br/> |Задает один экземпляр XML-файла страницы, хранящегося в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|р:ИД  <br/> |XSD: строка  <br/> См. раздел "Замечания".  <br/> |Обязательный  <br/> |Задает отношение к части.  <br/> |"rId #"  <br/> См. раздел "Замечания".  <br/> |
   
## <a name="remarks"></a>Замечания

Значение атрибута **р:ИД** должно быть типом **ст_релатионшипид** . Тип **ст_релатионшипид** — это строка, которая должна быть в формате rId #, где конечный символ должен быть числом. Число должно быть уникальным среди всех родственных элементов элемента **rel** . 
  
Для получения дополнительных сведений о типе Ст_релатионшипид, ознакомьтесь со [спецификациЕй ISO/IEC 29500 Part 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).
  

