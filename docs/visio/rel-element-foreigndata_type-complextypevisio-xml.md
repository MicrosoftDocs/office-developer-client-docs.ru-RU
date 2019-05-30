---
title: Элемент rel (Фореигндата_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: Указывает связь между фигурой и частью документа, которая содержит данные изображения, связанные с фигурой.
ms.openlocfilehash: 5836fd306670600f65eda1f3a998ef4c5479114b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542809"
---
# <a name="rel-element-foreigndatatype-complextype-visio-xml"></a>Элемент rel (Фореигндата_типе complexType) (XML для Visio)

Указывает связь между фигурой и частью документа, которая содержит данные изображения, связанные с фигурой.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Рел_типе](rel_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Фореигндата_типе](foreigndata_type-complextypevisio-xml.md) <br/> |Указывает один экземпляр графических данных, хранящихся в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|р:ИД  <br/> |XSD: строка  <br/> См. раздел "Замечания".  <br/> |Обязательный  <br/> |Задает отношение к части.  <br/> |"rId #"  <br/> См. раздел "Замечания".  <br/> |
   
## <a name="remarks"></a>Примечания

Значение атрибута **р:ИД** должно быть типом **ст_релатионшипид** . Тип **ст_релатионшипид** — это строка, которая должна быть в формате rId #, где конечный символ должен быть числом. Число должно быть уникальным среди всех родственных элементов элемента **rel** . 
  
Для получения дополнительных сведений о типе Ст_релатионшипид, ознакомьтесь со [спецификацией ISO/IEC 29500 Part 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).
  

