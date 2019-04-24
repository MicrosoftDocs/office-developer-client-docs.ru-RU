---
title: Элемент PageSheet (Мастер_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: Задает свойства страницы документа, связанной с образцом.
ms.openlocfilehash: 579b2b4f02c79a38842a150b8757329e19e7bb3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361126"
---
# <a name="pagesheet-element-mastertype-complextype-visio-xml"></a>Элемент PageSheet (Мастер_типе complexType) (' Visio XML ')

Задает свойства страницы документа, связанной с образцом.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Пажешит_типе](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Главные. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Master](master-element-masters_type-complextypevisio-xml.md) <br/> |[Мастер_типе](master_type-complextypevisio-xml.md) <br/> |Указывает образец в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Указывает идентификатор таблицы стилей, из которой требуется наследовать форматирование заливки. Он должен быть значением атрибута **ID** , связанным с **стилешит_типе** в документе.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|LineStyle  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Задает идентификатор таблицы стилей, из которой наследуются форматирование линий. Он должен быть значением атрибута **ID** , связанным с **стилешит_типе** в документе.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|TextStyle  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Задает идентификатор таблицы стилей, из которой требуется наследовать форматирование текста. Он должен быть значением атрибута **ID** , связанным с **стилешит_типе** в документе.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|UniqueID  <br/> |XSD: строка  <br/> |необязательный  <br/> |Уникальный идентификатор элемента в родительском элементе.  <br/> |Значения типа String: XSD.  <br/> |
   

