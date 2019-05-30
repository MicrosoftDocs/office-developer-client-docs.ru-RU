---
title: Элемент PageSheet (Паже_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Задает свойства страницы документа, связанной со страницей документа.
ms.openlocfilehash: 2f49d152a0fcb30e3f5aea98cdc251d3b65b8f69
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540625"
---
# <a name="pagesheet-element-pagetype-complextype-visio-xml"></a>Элемент PageSheet (Паже_типе complexType) (XML для Visio)

Задает свойства страницы документа, связанной со страницей документа.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Пажешит_типе](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Pages. XML  <br/> |
   
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
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Паже_типе](page_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие страницу в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Указывает идентификатор таблицы стилей, из которой требуется наследовать форматирование заливки. Он должен быть значением атрибута **ID** , связанным с **стилешит_типе** в документе.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|LineStyle  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Задает идентификатор таблицы стилей, из которой наследуются форматирование линий. Он должен быть значением атрибута **ID** , связанным с **стилешит_типе** в документе.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|TextStyle  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Задает идентификатор таблицы стилей, из которой требуется наследовать форматирование текста. Он должен быть значением атрибута **ID** , связанным с **стилешит_типе** в документе.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|UniqueID  <br/> |XSD: строка  <br/> |необязательный  <br/> |Уникальный идентификатор элемента в родительском элементе.  <br/> |Значения типа String: XSD.  <br/> |
   

